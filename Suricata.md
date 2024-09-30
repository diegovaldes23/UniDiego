Suricata es una herramienta avanzada de detección de intrusiones y análisis de tráfico de red en tiempo real. Su función principal es identificar actividades maliciosas, como intentos de hackeo, escaneos de red, o tráfico inusual, proporcionando una capa adicional de seguridad a las redes informáticas. Es un IDS/IPS (Intrusion Detection System/Intrusion Prevention System), lo que significa que puede tanto detectar como bloquear amenazas.

### ¿Para qué sirve Suricata?

1. **Monitoreo de tráfico de red:** Suricata examina todo el tráfico que pasa a través de la red y lo analiza en busca de patrones sospechosos.
2. **Detección de intrusiones:** Mediante el uso de reglas predefinidas o personalizadas, puede identificar intentos de intrusión o actividades maliciosas.
3. **Prevención de intrusiones:** Cuando está en modo IPS, Suricata no solo detecta, sino que también puede bloquear el tráfico que considere peligroso.
4. **Generación de alertas:** Cuando se detecta una amenaza, genera alertas que pueden ser analizadas por los administradores de seguridad.
5. **Análisis de protocolo profundo (DPI):** Inspecciona los paquetes en todos los niveles del modelo OSI para identificar cualquier vulnerabilidad o comportamiento extraño.
6. **Registro y auditoría:** Guarda información detallada sobre el tráfico de red, lo que es útil para auditorías y análisis forense.

### ¿Cómo se usa Suricata?

El proceso para utilizar Suricata generalmente sigue estos pasos:

1. **Instalación:**
    
    - Puede instalarse en una máquina o servidor que esté en una posición estratégica dentro de la red (por ejemplo, en la puerta de enlace o entre las subredes).
    - Existen varias formas de instalarlo: mediante paquetes para sistemas Linux (Debian, Ubuntu, CentOS), o bien compilándolo desde el código fuente.
2. **Configuración:**
    
    - Suricata requiere una configuración inicial donde se define el tráfico que va a monitorear, las interfaces de red y el modo de operación (solo detección o también prevención).
    - Se cargan reglas, que son el conjunto de condiciones que Suricata utilizará para determinar si el tráfico es sospechoso o malicioso. Estas reglas pueden ser preexistentes o personalizadas según las necesidades de la red.
3. **Monitoreo de tráfico:**
    
    - Una vez configurado, Suricata comienza a monitorear el tráfico de red en tiempo real. Dependiendo de su configuración, puede simplemente generar alertas o bloquear activamente el tráfico que identifique como peligroso.
4. **Generación de logs:**
    
    - Los resultados del análisis se guardan en archivos de log. Estos logs contienen detalles sobre el tráfico analizado, alertas generadas, y eventos de bloqueo si se usa en modo IPS.
5. **Análisis y respuesta:**
    
    - Los administradores de seguridad revisan los logs y alertas generadas para identificar posibles amenazas y tomar acciones correctivas, como bloquear ciertas IPs, ajustar las reglas de firewall, o investigar más a fondo los eventos reportados.

Suricata también se integra bien con otras herramientas de análisis de seguridad como **ELK Stack (Elasticsearch, Logstash, Kibana)** para almacenar y visualizar los datos de manera efectiva. Esto facilita la correlación de eventos de seguridad con otros logs de la infraestructura.

---


![[Pasted image 20240929133416.png]]

Lo que tienes en la pantalla es una parte del archivo de configuración `suricata.yaml`. Este archivo define cómo Suricata se comportará y qué redes debe monitorear. En la parte que estás viendo, se están configurando los grupos de direcciones (`address-groups`), que definen las redes internas y externas que Suricata debe analizar.

### ¿Qué es lo que ves en esta sección?

1. **`HOME_NET`**: Este es el grupo de direcciones que define las redes que consideras "internas" o de confianza. Esto es importante porque Suricata utiliza esta información para diferenciar entre tráfico interno y externo, lo que le ayuda a identificar mejor las amenazas. Por ejemplo, en tu caso, `HOME_NET` está configurado para las redes `192.168.0.0/16`, `10.0.0.0/8`, y `172.16.0.0/12`, que son redes privadas típicas.
    
    - **Sugerencia**: Asegúrate de que el rango de red en `HOME_NET` coincida con tu red local para que Suricata sepa qué monitorear.
2. **`EXTERNAL_NET`**: Este grupo de direcciones define las redes que consideras "externas", es decir, cualquier tráfico que no provenga de tu red interna. En este caso, está configurado como `!$HOME_NET`, lo que significa que cualquier tráfico que no provenga de tu red interna será considerado externo.
    
3. **Otros grupos (HTTP_SERVERS, SMTP_SERVERS, etc.)**: Estos definen qué servidores o servicios dentro de tu red deben ser monitoreados para tráfico HTTP, SMTP, SQL, DNS, etc. En este caso, todos están configurados para coincidir con `HOME_NET`, lo que significa que Suricata está monitoreando estos servicios en tu red interna.
    
4. **`port-groups`**: Aquí se definen puertos específicos que deben ser monitoreados para determinados servicios. En este caso, el puerto 80 (HTTP) está en el grupo de `HTTP_PORTS`, y `SHELLCODE_PORTS` parece estar también configurado, probablemente para detección de ataques tipo shellcode.
    

### ¿Qué puedes cambiar aquí?

- **Ajuste de redes internas (HOME_NET):**
    
    - Asegúrate de que las redes especificadas en `HOME_NET` son correctas para tu entorno. Por ejemplo, si tu red local es `192.168.1.0/24`, debes cambiar la línea a:
        
        yaml
        
        Copiar código
        
        `HOME_NET: "[192.168.1.0/24]"`
        
- **Ajuste de servicios internos (HTTP_SERVERS, SMTP_SERVERS, etc.):**
    
    - Si tienes servidores específicos que quieres monitorear, puedes ajustarlos aquí. Por ejemplo, si tienes un servidor web específico en tu red, podrías definir algo como:
        
        yaml
        
        Copiar código
        
        `HTTP_SERVERS: "[192.168.1.100]"`
        
        Esto hará que Suricata solo monitoree ese servidor para tráfico HTTP en lugar de toda la red `HOME_NET`.
        
- **Puertos a monitorear:**
    
    - Si tienes otros puertos que te interesan (por ejemplo, si tienes servidores corriendo en puertos no convencionales), puedes añadirlos a los grupos de puertos. Por ejemplo, si tu servidor web está en el puerto 8080, podrías modificar la línea de `HTTP_PORTS` para incluirlo:
        
        yaml
        
        Copiar código
        
        `HTTP_PORTS: "80,8080"`
        

### Resumen de acciones:

1. **Revisa y ajusta el `HOME_NET`** para que coincida con la red local que estás monitoreando.
2. **Configura `EXTERNAL_NET`** correctamente, aunque la configuración actual `!$HOME_NET` suele ser la correcta, ya que excluye todo el tráfico interno.
3. **Ajusta los grupos de servidores y puertos** para reflejar correctamente los servicios y puertos que quieras monitorear dentro de tu red.

Si haces cambios en este archivo, asegúrate de guardar los cambios y reiniciar Suricata para que los cambios tengan efecto:

bash

Copiar código

`sudo systemctl restart suricata`



---
Aquí tienes una lista explicando cada componente de la pila ELK (Elasticsearch, Logstash, Kibana), con una descripción de qué es, para qué sirve, y un ejemplo de uso práctico:

### 1. **ELK Stack**

- **¿Qué es?** La pila ELK es un conjunto de herramientas compuesto por Elasticsearch, Logstash y Kibana, diseñadas para gestionar y analizar grandes cantidades de datos en tiempo real. A menudo se utiliza para el análisis de logs, monitoreo de seguridad, análisis de rendimiento y visualización de datos.
- **¿Para qué sirve?** ELK Stack permite centralizar y procesar datos de diferentes fuentes (como logs de aplicaciones, servidores, dispositivos de red), indexarlos para hacer búsquedas rápidas y visualizarlos en gráficos interactivos.
- **Ejemplo de uso:** Una empresa puede utilizar ELK Stack para analizar todos los logs de sus aplicaciones web y servidores. Al centralizar los logs en ELK, el equipo de operaciones puede identificar problemas como errores, tiempo de respuesta lento o intentos de intrusión de manera rápida y eficiente.

### 2. **Elasticsearch**

- **¿Qué es?** Elasticsearch es un motor de búsqueda y análisis distribuido, altamente escalable y de alto rendimiento. Es la pieza central de la pila ELK y se encarga de indexar y almacenar los datos para que se puedan realizar búsquedas rápidas y análisis complejos.
- **¿Para qué sirve?** Elasticsearch se utiliza para almacenar datos estructurados y no estructurados, realizar búsquedas en tiempo real y análisis sobre grandes volúmenes de datos. Su capacidad de búsqueda es muy poderosa, lo que permite hacer consultas detalladas sobre los datos.
- **Ejemplo de uso:** Una empresa de comercio electrónico puede usar Elasticsearch para realizar búsquedas de productos en su sitio web. Los usuarios pueden buscar por nombre de producto, categoría o cualquier característica, y Elasticsearch devolverá los resultados en milisegundos, mejorando la experiencia del usuario.

### 3. **Logstash**

- **¿Qué es?** Logstash es una herramienta de procesamiento de datos en tiempo real que recoge, transforma y envía los datos a Elasticsearch (u otros destinos). Puede procesar datos de múltiples fuentes simultáneamente, como logs de servidores, métricas de sistemas y eventos de red.
- **¿Para qué sirve?** Logstash actúa como un intermediario entre las fuentes de datos (como Suricata, bases de datos, archivos de log) y Elasticsearch. Su función es filtrar, transformar y enriquecer los datos antes de enviarlos a su destino.
- **Ejemplo de uso:** Una empresa puede utilizar Logstash para recoger logs de servidores web, filtrar la información irrelevante (como mensajes de depuración) y transformar los logs en un formato más útil antes de enviarlos a Elasticsearch para análisis.

### 4. **Kibana**

- **¿Qué es?** Kibana es una herramienta de visualización de datos que se integra con Elasticsearch. Proporciona una interfaz gráfica para consultar, analizar y visualizar los datos almacenados en Elasticsearch. Se pueden crear gráficos, dashboards y alertas en tiempo real.
- **¿Para qué sirve?** Kibana es utilizada para visualizar los datos procesados por Elasticsearch. Permite a los usuarios realizar consultas complejas de los datos, crear dashboards interactivos y alertas para supervisar el estado de sistemas y aplicaciones.
- **Ejemplo de uso:** El equipo de seguridad de una empresa puede usar Kibana para visualizar las alertas generadas por Suricata (integrado con Elasticsearch) en tiempo real, ver gráficos que muestren las tendencias de ataques de red y configurar alertas visuales para detectar patrones de actividad maliciosa.

### Resumen:

|Componente|¿Qué es?|¿Para qué sirve?|Ejemplo de uso|
|---|---|---|---|
|**ELK Stack**|Conjunto de herramientas (Elasticsearch, Logstash, Kibana) para análisis de datos.|Centralización y análisis de grandes volúmenes de datos en tiempo real.|Análisis de logs en tiempo real para detectar errores y amenazas.|
|**Elasticsearch**|Motor de búsqueda y análisis distribuido.|Indexación y búsqueda rápida de grandes volúmenes de datos estructurados y no estructurados.|Búsquedas rápidas en un sitio web de comercio electrónico.|
|**Logstash**|Herramienta de procesamiento de datos en tiempo real.|Recoge, transforma y envía datos a Elasticsearch.|Procesamiento de logs de servidores para su posterior análisis en Elasticsearch.|
|**Kibana**|Herramienta de visualización de datos que se integra con Elasticsearch.|Visualización y análisis interactivo de datos mediante dashboards y gráficos.|Creación de dashboards en tiempo real para visualizar las alertas de seguridad de una red.|

Cada componente de la pila ELK juega un papel clave en la recolección, almacenamiento, análisis y visualización de datos, lo que permite a las organizaciones tomar decisiones informadas en tiempo real basadas en los datos.


---
### Verifica los servicios que están corriendo:

Para verificar si Elasticsearch, Logstash o Kibana están corriendo, puedes usar los siguientes comandos:

1. **Verificar si Elasticsearch está corriendo:**
    
    bash
    
    Copiar código
    
    `sudo systemctl status elasticsearch`
    
2. **Verificar si Logstash está corriendo:**
    
    bash
    
    Copiar código
    
    `sudo systemctl status logstash`
    
3. **Verificar si Kibana está corriendo:**
    
    bash
    
    Copiar código
    
    `sudo systemctl status kibana`
    

Si alguno de estos servicios está "active (running)", significa que están ejecutándose de forma constante.

### Detener los servicios cuando no los necesites:

Si no necesitas que los servicios estén activos todo el tiempo, puedes detenerlos temporalmente. Aquí te explico cómo detener cada uno:

1. **Detener Elasticsearch:**
    
    bash
    
    Copiar código
    
    `sudo systemctl stop elasticsearch`
    
2. **Detener Logstash:**
    
    bash
    
    Copiar código
    
    `sudo systemctl stop logstash`
    
3. **Detener Kibana:**
    
    bash
    
    Copiar código
    
    `sudo systemctl stop kibana`
    

### Reiniciar los servicios cuando los necesites:

Cuando necesites utilizar alguno de estos servicios nuevamente, puedes reiniciarlos con estos comandos:

1. **Iniciar Elasticsearch:**
    
    bash
    
    Copiar código
    
    `sudo systemctl start elasticsearch`
    
2. **Iniciar Logstash:**
    
    bash
    
    Copiar código
    
    `sudo systemctl start logstash`
    
3. **Iniciar Kibana:**
    
    bash
    
    Copiar código
    
    `sudo systemctl start kibana`