
Control 1

### **Pregunta 1:**

¿Qué control de los siguientes asegura la integridad?

- a. Encriptación simétrica
- b. Encriptación asimétrica
- c. Algoritmo de hash (ej. SHA2)
- d. Autentificación
- e. AES

**Respuesta:** 
	c. Algoritmo de hash (ej. SHA2)

---
### **Pregunta 2:**

Usted se encuentra desarrollando el sistema web de una aplicación para e-commerce. Al revisar las buenas prácticas de seguridad, advierte que es necesario incorporar los siguientes requerimientos. Indique qué propiedad se quiere lograr con dichas funcionalidades:

- Una funcionalidad que me permita identificar si una transacción crítica fue modificada.
- Una funcionalidad que corrobore que el usuario realizó una compra.
- Una funcionalidad de notificación cuando alguna acción en el sistema no se complete correctamente.
- Una funcionalidad que me permita visualizar las acciones del usuario en el sistema.
- Una funcionalidad que me permita saber que la persona que ingresó a la web es quien dice ser.
- Una funcionalidad para que solamente el jefe de finanzas de la cuenta pueda ver datos privados del cliente.

**Respuestas:**
	
	- Identificar si una transacción fue modificada → Integridad
	- Corroborar que el usuario realizó una compra → No repudio
	- Notificación cuando alguna acción no se complete → Disponibilidad
	- Visualizar las acciones del usuario → Accountability (Rendición de cuentas)
	- Saber que la persona es quien dice ser → Autenticidad
	- Solo el jefe de finanzas puede ver datos → Confidencialidad

---

### **Pregunta 3:**

Relacione el objetivo de ciberseguridad con su definición correspondiente:

- La propiedad de que los datos no se divulgan a las entidades del sistema a menos que hayan sido autorizados para conocer los datos.
- La propiedad de ser genuino y poder ser verificado y confiable.
- La propiedad de que los datos no se han cambiado, destruido o perdido de manera no autorizada o accidental.
- La propiedad de un sistema que es accesible o utilizable bajo demanda, por una entidad autorizada del sistema.
- Garantía de que el remitente de la información es provisto con una prueba de entrega y el destinatario recibe la prueba de la identidad del remitente.
- La propiedad que garantiza que las acciones de una entidad del sistema puedan rastrearse de forma exclusiva a esa entidad.

**Respuestas:**
	- No divulgación de datos → Confidencialidad
	- Ser genuino y verificable → Autenticidad
	- Datos no modificados o destruidos → Integridad
	- Accesible bajo demanda → Disponibilidad
	- Prueba de entrega y origen → No repudio
	- Acciones rastreables → Accountability (Rendición de cuentas)

---

### **Pregunta 4:**

Relacione los conceptos con su definición o ejemplo:

- Capacidad para corroborar que es cierta la reivindicación de que ocurrió un cierto suceso o se realizó una cierta acción.
- Conservación de la confidencialidad, integridad y disponibilidad de la información en el ciberespacio.
- En un documento electrónico, puedo obtener esta propiedad mediante técnicas de encriptación asimétrica y simétrica.
- Si instalo aplicaciones de terceros en mi smartphone, sin preocuparme por su origen, es probable que tenga una...
- Cuando necesito iniciar sesión en un sitio web y este me solicita mi clave y un código enviado a mi celular.
- Un Datacenter TIER IV tiene un 99.995% de...

**Respuestas:**

	- Corroborar que ocurrió un suceso → No repudio
	- Confidencialidad, integridad y disponibilidad en el ciberespacio → Ciberprotección
	- Encriptación en un documento electrónico → Confidencialidad
	- Instalación de apps sin verificar origen → Vulnerabilidad
	- Solicitud de clave y código en web → Autenticidad
	- Disponibilidad del 99.995% en Datacenter → Disponibilidad

---

### **Pregunta 5:**

Una organización busca asegurar que un empleado autorizado pueda acceder a sus recursos durante las horas normales de operación del negocio. ¿Qué concepto de seguridad se encuentra involucrado?

- a. Disponibilidad
- b. Confidencialidad
- c. No repudio
- d. Rendición de cuentas
- e. Integridad

**Respuesta:**
	a. Disponibilidad

---

### **Pregunta 6:**

Indique el concepto de acuerdo a la definición entregada:

- Camino o medios por los cuales un atacante puede obtener acceso a un servidor o red para entregar un resultado malicioso.
- Persona o grupo en quienes los órganos de gobierno han delegado la responsabilidad de implementar estrategias.
- Riesgo remanente después del tratamiento del riesgo.
- Medios para asegurar que el acceso a los activos está autorizado.
- Declaración que describe lo que se quiere lograr como resultado de los controles.
- Intenciones y dirección de una organización, como las expresa formalmente su alta dirección.
- Persona o grupo que dirige una organización al más alto nivel.
- Evento inesperado que tiene una probabilidad significativa de comprometer las operaciones del negocio.
- Software de control remoto, específicamente una colección de bots maliciosos que corren de manera automática en computadoras comprometidas.

**Respuestas:**
	
	- Camino de ataque → Vector de ataque
	- Implementar estrategias → Dirección ejecutiva
	- Riesgo después del tratamiento → Riesgo residual
	- Acceso autorizado a activos → Control de acceso
	- Declaración de lo que se quiere lograr → Objetivo de control
	- Intenciones y dirección de la organización → Política
	- Dirige la organización → Alta dirección
	- Evento inesperado → Incidente de seguridad de la información
	- Colección de bots maliciosos → Botnet

---

### **Pregunta 7:**

Un control se gestiona para mitigar el riesgo inherente.

- a. Verdadero
- b. Falso

**Respuesta:** 
	a. Verdadero

---
### **Pregunta 8:**

¿Cómo afecta el ransomware a la triada de la seguridad de la información?

- a. Amenaza la filtración de datos hacia internet para asegurar el pago del rescate.
- b. Modificación y alteración de la información, por lo que ahora se encuentra alterada.
- c. Datos cifrados, no se puede acceder.

**Respuesta:**
	
	- **Confidencialidad:** Amenaza la filtración de datos hacia internet para asegurar el pago del rescate.
	- **Integridad:** Modificación y alteración de la información, por lo que ahora se encuentra alterada.
	- **Disponibilidad:** Datos cifrados, no se puede acceder.

---

### **Pregunta 9:**

Una APT (Advanced Persistent Threat) se refiere a un ciberataque altamente sofisticado y preciso desde múltiples frentes, ejecutado por grupos que a menudo son apoyados o financiados por entidades externas, cuyas principales características son:

-  Acuciosidad en la seguridad de sus operaciones.
    
-  Bajas tasas de detección.
    
-  Altas probabilidades de éxito en el cumplimiento de sus objetivos.

Seleccione.
- a. Verdadero
    
- b. Falso
    

**Respuesta:**
	a. Verdadero

---

### **Pregunta 10:**

Entre los desafíos de la seguridad tenemos los siguientes:

- i. El cambio constante en la tecnología supone una actualización continua de las medidas de seguridad.
- ii. La gran cantidad de dispositivos de diferentes tipos requiere acceso a recursos, lo que debe ser controlado con medidas de seguridad.
- iii. Las amenazas vienen de pocos actores y son constantes en el tiempo.
- iv. El usuario requiere de la habilitación de nuevas funcionalidades y tecnologías cada vez más potentes, lo cual debe estar acompañado de seguridad robusta.
- v. Los costos de la seguridad en general son elevados, pero los beneficios son difíciles de calcular.

¿Cuál(es) son correctas?

- a. i, ii, iii, iv y v
- b. i y ii
- c. i, ii, iv y v
- d. i, ii, iii y iv
- e. i, ii, iii

**Respuesta:**
	c. i, ii, iv y v

---

### **Pregunta 11:**

Indique si las siguientes afirmaciones sobre seguridad son verdaderas:

 i) En general, cuanto más simple es el sistema y cuanto más aislados están sus elementos individuales, más fácil es implementar una seguridad efectiva.

 ii) A mayor complejidad, los sistemas son menos seguros.

 iii) Los usuarios que se sienten incómodos con los mecanismos de seguridad buscarán formas de evitarlos.

 iv) La funcionalidad de los sistemas debe ir de la mano con la seguridad. No se debe poner una sobre la otra.

 v) Los usuarios podrían exigir la relajación de los requisitos de seguridad si esta obstaculiza su trabajo.

- a. i y iii

- b. Todas las afirmaciones son falsas

- c. Todas las afirmaciones son verdaderas

- d. i, ii, iii y v

- e. i, ii y iii


**Respuesta:** 
	c. Todas las afirmaciones son verdaderas

---

### **Pregunta 12:**

¿Cuál de las siguientes corresponde a la definición de Ciberseguridad?

- i. Estado de protección en el ciberespacio contra consecuencias sociales, psicológicas, financieras, emocionales, ocupacionales, espirituales, físicas, educacionales o de otro tipo que resultan de daños, fallos, errores, accidentes, menoscabos o cualquier otro suceso no deseable.

- ii. El proceso de proteger la información mediante la prevención, detección y respuesta a los ataques.

- iii. Protección de todos los activos físicos de la organización.

- iv. Preservación de la confidencialidad de los datos digitales.

- v. Conjunto de políticas, conceptos, medidas, mejores prácticas, aseguramiento, gestión de riesgos, pautas, herramientas y tecnologías que se utilizan para proteger el entorno del ciberespacio y los activos de los usuarios.

- a. i, ii y iii

- b. i, ii y v

- c. ii, iii, iv y v

- d. i, ii, iii y iv

- e. i, iii y v


**Respuesta:**
	b. i, ii y v

---
### **Pregunta 13:**

Indique cuál de las siguientes afirmaciones sobre seguridad es incorrecta:

- a. Un sistema con más funcionalidades tiende a ser menos seguro.
- b. Los sistemas aislados son generalmente más seguros que los sistemas interconectados.
- c. Un sistema menos complejo tiene menos vulnerabilidades.
- d. La seguridad en un sistema sólo es responsabilidad del equipo de TI.
- e. La funcionalidad de un sistema no debe comprometer su seguridad.

**Respuesta:** 
	d. La seguridad en un sistema sólo es responsabilidad del equipo de TI.

---

### **Pregunta 14:**

¿Qué se busca con la **seguridad de la información**?

- a. Confidencialidad, integridad y disponibilidad.
- b. Autenticidad, confidencialidad y autorización.
- c. Integridad, no repudio y disponibilidad.
- d. Autenticación, autorización y auditoría.

**Respuesta:** 
	a. Confidencialidad, integridad y disponibilidad.

---
![[Pasted image 20240919211737.png]]
---

### **Pregunta 16:**

¿Cuál de las siguientes técnicas se utiliza para proteger la **confidencialidad** de la información?

- a. Algoritmos de hash.
- b. Encriptación.
- c. Firma digital.
- d. Sistema de autenticación.

**Respuesta:** 
	b. Encriptación.

---

### **Pregunta 17:**

¿Qué concepto de seguridad busca garantizar que la información solo sea accesible por personas autorizadas?

- a. Disponibilidad.
- b. Confidencialidad.
- c. Integridad.
- d. Autenticidad.

**Respuesta:** 
	b. Confidencialidad.

---

### **Pregunta 18:**

¿Qué propiedad de la seguridad de la información se ve afectada cuando los datos son alterados de manera no autorizada?

- a. Confidencialidad.
- b. Disponibilidad.
- c. Integridad.
- d. Autenticación.

**Respuesta:** 
	c. Integridad.

---

### **Pregunta 19:**

¿Cuál de los siguientes **no** es un principio básico de seguridad?

- a. Confidencialidad.
- b. Disponibilidad.
- c. Autenticidad.
- d. No repudio.

**Respuesta:** d. 
	No repudio.

---

### **Pregunta 20:**

¿Cuál de las siguientes afirmaciones describe **autenticidad**?

- a. Capacidad de garantizar que los datos no han sido alterados.
- b. Garantía de que los datos están disponibles cuando se necesiten.
- c. Confirmación de que una entidad es quien dice ser.
- d. Capacidad de denegar una acción o evento después de ocurrido.

**Respuesta:**
	c. Confirmación de que una entidad es quien dice ser.


---
PEP 1  25/10/2023

Escenario Una empresa de comercio electrónico, que ha alcanzado un éxito significativo en su mercado local, se encuentra en el proceso de expandirse a mercados internacionales. Esta firma, además de ofrecer productos propios, facilita transacciones entre usuarios en un estilo similar a un mercado en línea. En el marco de esta expansión, planea integrar una diversidad de sistemas de pago, establecer alianzas con proveedores de diferentes partes del mundo y adoptar tecnologías avanzadas para la logística y administración del inventario. Con la expansión global en mente, la empresa reconoce la necesidad de alojar su plataforma en servidores ubicados estratégicamente alrededor del mundo, asegurando así una rápida respuesta y constante disponibilidad. Además, la integración de múltiples sistemas de pago y alianzas con proveedores internacionales añade una capa adicional de complejidad a su infraestructura tecnológica. Por otro lado, al considerar la implementación del Internet de las Cosas (IoT) para la gestión de inventarios y logística, surgen desafíos relacionados tanto con la conectividad como con la seguridad. A todo esto, se suma el hecho de que, al servir a una clientela global, la plataforma deberá ser accesible desde una amplia variedad de dispositivos y sistemas operativos, cada uno con sus propias particularidades y requerimientos de seguridad. Sin embargo, al entrar en nuevos territorios, la empresa no solo se enfrenta a retos tecnológicos, sino también a una amplia gama de problemas. Estos incluyen la exposición a actores maliciosos regionales, variaciones en las legislaciones de protección de datos y la posibilidad de que competidores busquen obtener información estratégica. Cada región presenta sus propios riesgos y la empresa debe estar preparada para enfrentar amenazas tanto legales como tecnológicas. Uno de los desafíos más complejos radica en equilibrar las necesidades y expectativas de los usuarios con las demandas de una implementación de seguridad robusta. Mientras que las medidas de seguridad sólidas, como la autenticación multifactor, pueden ofrecer una capa adicional de protección, también pueden ser percibidas por los nuevos usuarios como barreras que complican la experiencia de usuario. Además, las expectativas en cuanto a usabilidad y características varían entre regiones, y lo que es estándar en un mercado puede ser nuevo o desconocido en otro. Por último, otro desafío crucial es la dificultad inherente a estimar los costos y beneficios de las inversiones en ciberseguridad. La exposición a posibles ataques aumenta con la expansión, pero determinar cuánto invertir en prevención es una tarea compleja. Los costos asociados a la prevención y respuesta ante amenazas pueden ser elevados, y una brecha de seguridad en un nuevo mercado puede tener repercusiones en la reputación de la empresa que duren mucho más que el incidente en sí

**1. ¿Cuál de los siguientes se considera un activo crítico para la empresa de comercio electrónico en expansión internacional?**

- a) Los comentarios en las redes sociales.
- b) La diversidad de sistemas de pago.
- c) La plataforma en línea.
- d) El software de administración de inventario.
- e) Los vehículos de entrega.

**Respuesta:** 
	c. La plataforma en línea.  
	**Justificación:** La plataforma en línea es el núcleo del negocio, facilitando todas las transacciones y la interacción con los clientes. Si esta se ve comprometida, todo el negocio corre riesgo.

---

**2. ¿Qué aspecto representa una vulnerabilidad en el contexto de la diversidad de sistemas de pago?**

- a) Diversas monedas.
- b) Diferentes proveedores de sistemas de pago.
- c) Diferentes tipos de sistemas de autenticación y tecnologías.
- d) Altas comisiones.
- e) Compatibilidad con distintos sistemas operativos.

**Respuesta:** 
	c. Diferentes tipos de sistemas de autenticación y tecnologías.  
	**Justificación:** La diversidad en los métodos de autenticación entre diferentes sistemas de pago puede crear puntos débiles que los atacantes podrían explotar.

---

**3. ¿Cuál de las siguientes es una amenaza a considerar debido a la expansión a mercados internacionales?**

- a) Actores maliciosos regionales.
- b) Incremento de tráfico en la plataforma.
- c) Fallos de hardware.
- d) Fluctuaciones de la moneda.
- e) Opiniones de clientes insatisfechos.

**Respuesta:** 
	a. Actores maliciosos regionales.  
	**Justificación:** Al expandirse internacionalmente, la empresa se expone a actores maliciosos que son específicos de diferentes regiones y que podrían no haber sido una preocupación en su mercado local.

---

**4. En el contexto de implementación de IoT para la gestión de inventarios, ¿qué factor incrementa la exposición a riesgos?**

- a) Mayor eficiencia en el seguimiento del inventario.
- b) Uso de tecnología de vanguardia.
- c) Mayor cantidad de puntos de acceso.
- d) Reducción en los costos operativos.
- e) Facilita la adaptación a mercados internacionales.

**Respuesta:** 
	c. Mayor cantidad de puntos de acceso.  
	**Justificación:** Al implementar IoT, el número de dispositivos conectados y, por lo tanto, los puntos de acceso a la red aumentan, lo que amplía la superficie de ataque.

---

**5. Ante el desafío de equilibrar seguridad y experiencia de usuario, ¿qué control podría implementarse?**

- a) Aumentar la complejidad de las contraseñas.
- b) Autenticación multifactorial sin contraseñas.
- c) Verificación de identidad por video.
- d) Encriptación de datos de usuarios.
- e) Reconocimiento facial.

**Respuesta:** 
	b. Autenticación multifactorial.  
	**Justificación:** La autenticación multifactorial proporciona una capa adicional de seguridad sin sacrificar significativamente la experiencia del usuario, ya que suele ser rápida y, en muchos casos, ya es conocida por los usuarios.

---

**6. En el contexto del ciberespacio, ¿qué representa el hecho de que la empresa de e-commerce esté expandiéndose a mercados internacionales?**

- a) Limitación de riesgos.
- b) Reducción del cibercrimen.
- c) Aumento de la exposición.
- d) Autenticidad garantizada.
- e) Incremento de la disponibilidad.

**Respuesta:**
	c. Aumento de la exposición.  
	**Justificación:** Al expandirse a mercados internacionales, la empresa está extendiendo su presencia en el ciberespacio, lo que inevitablemente aumenta su exposición a potenciales amenazas.

---

**7. Considerando la integridad de los datos, ¿qué amenaza podría comprometer las transacciones entre usuarios en el mercado en línea?**

- a) Fallos en la autenticación multifactorial.
- b) Manipulación de datos de transacciones.
- c) Control físico inadecuado.
- d) Controles disuasivos insuficientes.
- e) Expansión internacional.

**Respuesta:** 
	b. Manipulación de datos de transacciones.  
	**Justificación:** La integridad se refiere a asegurar que los datos no sean alterados sin autorización. La manipulación de datos de transacción comprometería directamente esta integridad.

---

**8. Dada la naturaleza global de la empresa de e-commerce, ¿qué representa una mayor preocupación en términos de accountability?**

- a) Diversos sistemas de pago.
- b) Diferentes legislaciones de protección de datos.
- c) Variedad de productos ofertados.
- d) La utilización del Internet de las Cosas (IoT).
- e) Autenticación unifactorial.

**Respuesta:**
	b. Diferentes legislaciones de protección de datos.  
	**Justificación:** La accountability se refiere a la responsabilidad de las acciones y decisiones. Diferentes legislaciones pueden tener diferentes requisitos y consecuencias legales, lo que complica la responsabilidad.

---

**9. ¿Cuál de las siguientes opciones es un control técnico?**

- a) Políticas de seguridad.
- b) Vigilancia en las instalaciones.
- c) Firewalls.
- d) Capacitación sobre seguridad.
- e) Señalizaciones de seguridad.

**Respuesta:**
	c. Firewalls.  
	**Justificación:** Los firewalls son herramientas técnicas diseñadas para filtrar tráfico y proteger sistemas contra amenazas.

---

**10. Considerando la expansión a mercados internacionales, ¿qué tipo de control sería más efectivo para mitigar riesgos asociados al cibercrimen?**

- a) Controles disuasivos.
- b) Controles recuperativos.
- c) Controles compensatorios.
- d) Controles preventivos.
- e) Controles correctivos.

**Respuesta:** 
	d. Controles preventivos.  
	**Justificación:** Dada la ampliación y exposición a nuevas amenazas, es fundamental implementar controles que prevengan el cibercrimen antes de que ocurra.

---

**11. En relación con el principio de defensa en profundidad, ¿qué acción es más coherente?**

- a) Implementar un solo control robusto.
- b) Depender únicamente de controles físicos.
- c) Establecer múltiples capas de seguridad.
- d) Concentrarse solo en la autenticidad.
- e) Ignorar los controles recuperativos.

**Respuesta:** 
	c. Establecer múltiples capas de seguridad.  
	**Justificación:** La defensa en profundidad se refiere a la implementación de múltiples capas de seguridad para protegerse contra amenazas.

---

**12. ¿Qué elemento garantiza la autenticidad de una transacción?**

- a) La disponibilidad constante.
- b) Un certificado digital.
- c) Una política de privacidad sólida.
- d) La expansión a nuevos mercados.
- e) Controles disuasivos.

**Respuesta:** 
	b. Un certificado digital.  
	**Justificación:** Los certificados digitales validan la identidad de una entidad y garantizan la autenticidad de la comunicación o transacción.


---
**13. Ante un incidente de seguridad, ¿qué control se activaría para corregir el problema?**

- a) Control disuasivo.
- b) Control compensatorio.
- c) Control preventivo.
- d) Control recuperativo.
- e) Control correctivo.

**Respuesta:** 
	e) Control correctivo.  
	**Justificación:** Los controles correctivos se implementan para corregir problemas una vez que han sido identificados.

---

**14. ¿Qué representa el no repudio en una transacción de comercio electrónico?**

- a) Garantiza la disponibilidad de la transacción.
- b) Asegura la confidencialidad de los datos.
- c) Verifica la autenticidad de la transacción.
- d) Asegura que ninguna de las partes puede negar su participación.
- e) Evalúa la vulnerabilidad de la transacción.

**Respuesta:** 
	d) Asegura que ninguna de las partes pueda negar su participación.  
	**Justificación:** El no repudio se refiere a la garantía de que ninguna de las partes involucradas en una transacción pueda negar posteriormente su participación en ella.

---

**15. Ante una brecha de seguridad en la que se filtraron datos sensibles de usuarios, ¿qué principio se ha comprometido primordialmente?**

- a) Disponibilidad.
- b) Autenticidad.
- c) No repudio.
- d) Integridad.
- e) Confidencialidad.

**Respuesta:** 
	e) Confidencialidad.  
	**Justificación:** La confidencialidad se refiere a la protección de la información contra la divulgación no autorizada.

---

**16. ¿Qué tipo de control es primordialmente un sistema de videovigilancia en las instalaciones de un centro de datos?**

- a) Técnico.
- b) Físico.
- c) Administrativo.
- d) Disuasivo.
- e) Recuperativo.

**Respuesta:** 
	b) Físico.  
	**Justificación:** Los controles físicos están destinados a proteger activos reales o tangibles, como las instalaciones o hardware.

---

**17. Al establecer políticas de acceso a datos y definir roles dentro de la plataforma, la empresa está implementando principalmente controles:**

- a) Técnicos.
- b) Físicos.
- c) Administrativos.
- d) Correctivos.
- e) Compensativos.

**Respuesta:** 
	c) Administrativos.  
	**Justificación:** Los controles administrativos son políticas y procedimientos diseñados para gestionar y monitorear el acceso y uso de procesos, sistemas y datos.

---

**18. Un empleado recibe un correo electrónico de un atacante haciéndose pasar por un proveedor. ¿Qué tipo de cibercrimen es esto?**

- a) Ataque DDoS.
- b) Phishing.
- c) Ransomware.
- d) Virus.
- e) Worm.

**Respuesta:** 
	b) Phishing.  
	**Justificación:** El phishing implica engañar a las víctimas para que compartan información confidencial, a menudo haciéndose pasar por una entidad confiable.

---

**19. De acuerdo con la ley chilena actual sobre delitos informáticos, ¿qué delito está asociado con la introducción, alteración, daño o supresión de datos informáticos con la intención de que estos se consideren auténticos?**

- a) Ataque a la integridad de un sistema informático.
- b) Interceptación ilícita.
- c) Falsificación informática.
- d) Fraude informático.
- e) Abuso de dispositivos.

**Respuesta:** 
	c) Falsificación informática.  
	**Justificación:** El Artículo 5° señala que aquel que indebidamente introduzca, altere, dañe o suprima datos informáticos con la intención de que sean tomados como auténticos será sancionado bajo el delito de "Falsificación informática".

---

**20. Según la ley proporcionada, ¿cuál de las siguientes opciones NO es considerada una circunstancia agravante para los delitos tratados en este Título?**

- a) Cometer el delito abusando de una posición de confianza en la administración del sistema informático.
- b) Cometer el delito mientras se interrumpe la prestación de servicios de utilidad pública como transporte.
- c) Cometer el delito con la intención de obtener un beneficio económico.
- d) Cometer el delito abusando de la vulnerabilidad de niños, niñas, adolescentes o adultos mayores.
- e) Cometer el delito utilizando dispositivos creados principalmente para la perpetración de dichos delitos.

**Respuesta:** 
	c) Cometer el delito con la intención de obtener un beneficio económico.  
	**Justificación:** Mientras que las opciones a, b, y d están mencionadas como circunstancias agravantes en el Artículo 10, la opción c es una característica del fraude informático según el Artículo 7°, pero no se menciona como una circunstancia agravante específica en el Artículo 10.


---
**21. Según el Código de Ética de EC-Council, ¿cuál de las siguientes afirmaciones es correcta en relación con la propiedad intelectual?**

- a) Está permitido utilizar la propiedad intelectual de otros siempre que no se obtenga beneficio económico de ello.
- b) Se puede usar la propiedad intelectual de otros siempre y cuando no se infrinjan las leyes del país.
- c) La propiedad intelectual de otros se debe proteger y confiar en la propia innovación y esfuerzo.
- d) Se puede usar la propiedad intelectual de otros si se tiene el consentimiento del propietario.
- e) La propiedad intelectual no es relevante en el Código de Ética de EC-Council.

**Respuesta:** 
	c) La propiedad intelectual de otros se debe proteger y confiar en la propia innovación y esfuerzo.  
	**Justificación:** Según el Código de Ética de EC-Council, se debe "Proteger la propiedad intelectual de otros confiando en tu propia innovación y esfuerzos, garantizando que todos los beneficios recaigan en su creador".

---

**22. De acuerdo con el Código de Ética de EC-Council, ¿cuál es la postura correcta respecto a la participación en comunidades de hacking underground que promueven actividades de sombrero negro?**

- a) Es aceptable si el profesional no participa activamente en actividades de sombrero negro.
- b) Se puede participar solo para recopilar información y mejorar la seguridad de los sistemas.
- c) Es aceptable siempre y cuando no se violen las leyes del país.
- d) Está estrictamente prohibido participar en dichas comunidades.
- e) Solo es aceptable si se tiene el consentimiento de EC-Council.

**Respuesta:** 
	d) Está estrictamente prohibido participar en dichas comunidades.  
	**Justificación:** El Código de Ética de EC-Council establece que no se debe "formar parte de ninguna comunidad de hacking underground con el propósito de predicar y expandir actividades de sombrero negro".

---

**23. Según el Código de Ética Profesional de ISACA, ¿cuál de las siguientes afirmaciones es correcta con respecto a la privacidad y confidencialidad de la información?**

- a) La información confidencial obtenida puede ser utilizada para beneficio personal si se estima conveniente.
- b) La información confidencial debe divulgarse siempre para transparencia.
- c) La información confidencial puede ser divulgada únicamente cuando sea requerido por una autoridad legal.
- d) La información confidencial puede ser compartida con cualquier parte interesada.
- e) La divulgación de información es a discreción del miembro de ISACA.

**Respuesta:** 
	c) La información confidencial puede ser divulgada únicamente cuando sea requerido por una autoridad legal.  
	**Justificación:** El código de ISACA establece que los miembros deben "mantener la privacidad y confidencialidad de la información obtenida en el curso de sus deberes a menos que la divulgación sea requerida por una autoridad legal".

---

**24. Según el Código de Ética de ISC2, ¿cuál de las siguientes afirmaciones es correcta respecto a la relación entre los miembros de ISC2 y el Código?**

- a) Todos los miembros de ISC2 tienen la opción de seguir o no el Código de Ética.
- b) Sólo aquellos miembros de ISC2 que deseen mantener su certificación deben seguir el Código.
- c) Aquellos miembros de ISC2 que violen cualquier disposición del Código no enfrentarán ninguna acción disciplinaria.
- d) Se obliga a los miembros de ISC2 a seguir el procedimiento de queja ética al observar cualquier acción por parte de un miembro de ISC2 que viole el Código.
- e) El Código de Ética de ISC2 tiene como principal objetivo ser un sustituto del juicio ético del profesional.

**Respuesta:** 
	d) Se obliga a los miembros de ISC2 a seguir el procedimiento de queja ética al observar cualquier acción por parte de un miembro de ISC2 que viole el Código.  
	**Justificación:** El Código de Ética de ISC2 establece claramente que los miembros están obligados a seguir el procedimiento de queja ética cuando observan una violación del Código por parte de otro miembro.

---

**25. De acuerdo con los cánones del Código de Ética de ISC2, ¿cuál es uno de los deberes fundamentales que los profesionales certificados por ISC2 deben cumplir?**

- a) Brindar servicios solo cuando se obtenga un beneficio personal.
- b) Actuar de manera deshonesta si es necesario para proteger la información.
- c) Proporcionar un servicio diligente y competente a los principios.
- d) Abstenerse de proteger la infraestructura si va en contra de los intereses de la organización.
- e) No adherirse a estándares éticos de comportamiento.

**Respuesta:** 
	c) Proporcionar un servicio diligente y competente a los principios.  
	**Justificación:** Uno de los cánones del Código de Ética de ISC2 establece explícitamente que los profesionales deben "Proporcionar un servicio diligente y competente a los principios".

---

**26. Para garantizar una expansión efectiva en mercados internacionales, ¿qué metodología puede ayudar mejor a la empresa a alinear su tecnología de la información con las metas empresariales?**

- a) PCI DSS
- b) ISO 27000
- c) COBIT
- d) CIS Controls
- e) Ninguna de las anteriores

**Respuesta:** 
	c) COBIT.  
	**Justificación:** COBIT (Control Objectives for Information and Related Technologies) se enfoca en la gobernanza de TI y cómo alinear los recursos tecnológicos con los objetivos y estrategias empresariales, ideal para la expansión internacional.

---

**27. Para garantizar la seguridad en las transacciones de pago, ¿qué estándar debería seguir la empresa?**

- a) COBIT
- b) CIS Controls
- c) PCI DSS
- d) ISO 27000
- e) Ninguna de las anteriores

**Respuesta:** 
	c) PCI DSS.  
	**Justificación:** PCI DSS (Payment Card Industry Data Security Standard) está diseñado para proteger las transacciones con tarjetas de crédito y débito y la manipulación de datos sensibles asociados a ellas.

---

**28. ¿Qué conjunto de prácticas se centra más en la implementación y monitoreo de configuraciones de seguridad en dispositivos y sistemas?**

- a) PCI DSS
- b) ISO 27000
- c) COBIT
- d) CIS Controls
- e) Ninguna de las anteriores

**Respuesta:** 
	d) CIS Controls.  
	**Justificación:** CIS Controls (Center for Internet Security Controls) ofrece un conjunto de acciones para la ciberdefensa que proporcionan una defensa específica y efectiva contra amenazas cibernéticas.


---
PEP 1 12/05/2023
Escenario 

Eres el responsable de ciberseguridad en una pequeña empresa de comercio electrónico. Recientemente, has notado un aumento en los intentos de phishing dirigidos a tus compañeros de trabajo. Los correos electrónicos de phishing parecen provenir de una entidad que se hace pasar por el soporte técnico del servicio de correo electrónico que utiliza la empresa. Los correos electrónicos solicitan a los empleados que proporcionen sus credenciales de inicio de sesión para resolver problemas técnicos inexistentes. Esto sugiere que un grupo de ciberdelincuentes está tratando de obtener acceso no autorizado a las cuentas de correo electrónico de los empleados para lanzar ataques más amplios y acceder a información sensible

**Pregunta 1**: ¿Cuál de las siguientes vulnerabilidades están explotando los agentes de amenaza en este escenario?

A) Vulnerabilidades en el software de la empresa  
B) Fallos en la configuración de la red  
C) Falta de concienciación y formación en ciberseguridad de los empleados  
D) Malas prácticas de contraseñas  
E) Inadecuada segmentación de la red

**Respuesta correcta**: 
	C) Falta de concienciación y formación en ciberseguridad de los empleados.  
	**Justificación**: Los ciberdelincuentes están aprovechando la falta de conocimientos de los empleados sobre phishing y seguridad, lo que los hace susceptibles a entregar sus credenciales de inicio de sesión.

---

**Pregunta 2**: ¿Qué tipo de agente de amenaza está involucrado en este escenario?

A) Hacktivistas  
B) Grupos terroristas  
C) Ciberdelincuentes  
D) Espías industriales  
E) Insiders maliciosos

**Respuesta correcta**: 
	C) Ciberdelincuentes.  
	**Justificación**: El escenario sugiere que el grupo detrás de los ataques de phishing tiene motivaciones financieras y busca acceso no autorizado para obtener información sensible, lo que encaja con el perfil de ciberdelincuentes.

---

**Pregunta 3**: ¿Cuál de los siguientes objetivos de ciberseguridad está directamente amenazado en este escenario?

A) Disponibilidad  
B) Confidencialidad  
C) Integridad  
D) No repudio  
E) Autenticidad

**Respuesta correcta**: 
	B) Confidencialidad.  
	**Justificación**: Al obtener acceso a las cuentas de correo electrónico de los empleados, los ciberdelincuentes podrían acceder a información confidencial, lo que pone en riesgo la confidencialidad de los datos de la empresa.

---

**Pregunta 4**: ¿Cuál de las siguientes medidas podría ayudar a prevenir futuros ataques de phishing?

A) Implementar un firewall de red  
B) Realizar copias de seguridad de datos periódicas  
C) Establecer políticas de contraseñas seguras  
D) Capacitar a los empleados en concienciación sobre phishing y ciberseguridad  
E) Utilizar software antivirus actualizado

**Respuesta correcta**:
	D) Capacitar a los empleados en concienciación sobre phishing y ciberseguridad.  
	**Justificación**: La formación en concienciación sobre phishing y ciberseguridad ayudará a los empleados a reconocer y evitar ataques de phishing, reduciendo así el riesgo de que proporcionen sus credenciales a los ciberdelincuentes.

---

**Pregunta 5**: Si un ataque de phishing tiene éxito, ¿qué consecuencia directa podría tener en la empresa?

A) Interrupción del servicio de correo electrónico  
B) Pérdida de la integridad de los datos  
C) Dificultades en la autenticación de los usuarios  
D) Acceso no autorizado a información confidencial  
E) Compromiso de la disponibilidad de la red

**Respuesta correcta**: 
	D) Acceso no autorizado a información confidencial.  
	**Justificación**: Si un empleado proporciona sus credenciales en respuesta a un correo electrónico de phishing, los atacantes tendrían acceso a su cuenta de correo electrónico y a cualquier información confidencial contenida en ella.

---

**Pregunta 6**: ¿Qué es el cibercrimen y cuál es su relación con las amenazas en el ámbito de la ciberseguridad?

A) El cibercrimen se refiere a la explotación de vulnerabilidades en sistemas informáticos para obtener acceso no autorizado, mientras que las amenazas son eventos o acciones que pueden explotar esas vulnerabilidades.  
B) El cibercrimen es el acto de crear software malicioso, mientras que las amenazas son los diferentes tipos de software malicioso que existen.  
C) El cibercrimen es una disciplina de la informática que estudia cómo proteger sistemas y redes, mientras que las amenazas son eventos que pueden poner en riesgo la seguridad de dichos sistemas y redes.  
D) El cibercrimen se refiere a la realización de actividades delictivas utilizando tecnologías de la información y la comunicación, mientras que las amenazas son eventos o acciones que pueden causar daños o pérdidas en el ámbito de la ciberseguridad.  
E) Ninguna de las anteriores.

**Respuesta correcta**: 
	D) El cibercrimen se refiere a la realización de actividades delictivas utilizando tecnologías de la información y la comunicación, mientras que las amenazas son eventos o acciones que pueden causar daños o pérdidas en el ámbito de la ciberseguridad.

---

**Pregunta 7**: ¿Cuál es la diferencia entre autenticidad y autenticación en el contexto de la ciberseguridad?

A) La autenticidad se refiere a la verificación de la identidad de un usuario, mientras que la autenticación es la capacidad de demostrar que un evento o transacción ha tenido lugar.  
B) La autenticidad se refiere a la capacidad de demostrar que un evento o transacción ha tenido lugar, mientras que la autenticación es la verificación de la identidad de un usuario.  
C) La autenticidad y la autenticación son sinónimos y se utilizan indistintamente en el ámbito de la ciberseguridad.  
D) La autenticidad se refiere al proceso de cifrado de datos, mientras que la autenticación es el proceso de descifrado de datos.  
E) Ninguna de las anteriores.

**Respuesta correcta**: 
	B) La autenticidad se refiere a la capacidad de demostrar que un evento o transacción ha tenido lugar, mientras que la autenticación es la verificación de la identidad de un usuario.

---

**Pregunta 8**: ¿Qué es un vector de ataque en el contexto de la ciberseguridad?

A) Un vector de ataque es un método utilizado por los ciberdelincuentes para explotar vulnerabilidades y comprometer la seguridad de un sistema o red.  
B) Un vector de ataque es una medida preventiva implementada para proteger los sistemas y redes de la explotación de vulnerabilidades.  
C) Un vector de ataque es un evento inesperado que puede causar daños o pérdidas en un sistema o red.  
D) Un vector de ataque es un tipo específico de software malicioso diseñado para atacar y comprometer la seguridad de un sistema o red.  
E) Ninguna de las anteriores.

**Respuesta correcta**: 
	A) Un vector de ataque es un método utilizado por los ciberdelincuentes para explotar vulnerabilidades y comprometer la seguridad de un sistema o red.

---

**Pregunta 9**: ¿Quién es el dueño del riesgo en el contexto de la ciberseguridad y cuál es su función?

A) El dueño del riesgo es el individuo que realiza un ataque cibernético, y su función es explotar las vulnerabilidades en los sistemas de seguridad.  
B) El dueño del riesgo es el individuo o entidad que acepta la responsabilidad de gestionar un riesgo, incluyendo su identificación, evaluación y mitigación.  
C) El dueño del riesgo es el individuo o entidad que se ve directamente afectado por un riesgo, y su función es soportar las consecuencias si el riesgo se materializa.  
D) El dueño del riesgo es el individuo que desarrolla las políticas de seguridad de una organización, y su función es garantizar que estas políticas se cumplan.  
E) Ninguna de las anteriores.

**Respuesta correcta**: 
	B) El dueño del riesgo es el individuo o entidad que acepta la responsabilidad de gestionar un riesgo, incluyendo su identificación, evaluación y mitigación.

---

**Pregunta 10**: ¿Qué es el no repudio en el contexto de la ciberseguridad?

A) El no repudio es la capacidad de demostrar que un evento o acción específica ha tenido lugar, de manera que esta no pueda ser negada posteriormente.  
B) El no repudio es la capacidad de un sistema para resistir ataques cibernéticos sin interrupción o pérdida de funcionalidad.  
C) El no repudio es la garantía de que la información transmitida a través de una red llegue a su destino sin ser interceptada o alterada.  
D) El no repudio es la capacidad de un sistema para recuperarse rápidamente de un ataque cibernético y restaurar su funcionalidad normal.  
E) Ninguna de las anteriores.

**Respuesta correcta**:
	A) El no repudio es la capacidad de demostrar que un evento o acción específica ha tenido lugar, de manera que esta no pueda ser negada posteriormente.

---

**Pregunta 11**: ¿Cómo impactaría en una empresa el acceso no autorizado a información confidencial?

A) No tendría impacto significativo en la empresa.  
B) Podría tener un impacto financiero significativo, incluyendo posibles multas y pérdida de negocio debido a la pérdida de confianza de los clientes.  
C) Podría aumentar la eficiencia de los procesos de negocio, ya que los empleados tendrían acceso a más información.  
D) Podría mejorar la seguridad de la empresa, ya que se identificarían y corregirían las vulnerabilidades.

**Respuesta correcta**: 
	B) Podría tener un impacto financiero significativo, incluyendo posibles multas y pérdida de negocio debido a la pérdida de confianza de los clientes.

---

**Pregunta 12**: ¿Qué estándar o marco de control deberías considerar si tu organización procesa, almacena o transmite información de tarjetas de crédito?

A) CIS Controls  
B) ISO 27000  
C) NIST CSF  
D) PCI DSS  
E) COBIT

**Respuesta correcta**: 
	D) PCI DSS  
	**Justificación**: PCI DSS es el estándar de seguridad de datos de la industria de tarjetas de pago y es específicamente para organizaciones que manejan información de tarjetas de crédito.

---

**Pregunta 13**: ¿Cuál de los siguientes marcos de ciberseguridad es más apropiado para una organización que busca un enfoque de gestión de riesgos de ciberseguridad que sea consistente con las recomendaciones del gobierno de los Estados Unidos?

A) CIS Controls  
B) ISO 27000  
C) NIST CSF  
D) PCI DSS  
E) COBIT

**Respuesta correcta**: 
	C) NIST CSF  
	**Justificación**: NIST CSF es un marco de ciberseguridad creado por el Instituto Nacional de Estándares y Tecnología de los Estados Unidos, y está ampliamente reconocido y recomendado por el gobierno de los EE.UU.

---

**Pregunta 14**: Si tu organización está interesada en un marco de ciberseguridad que no sólo se centre en la tecnología, sino también en los aspectos de gestión y gobierno de la tecnología de la información, ¿cuál de los siguientes sería la mejor opción?

A) CIS Controls  
B) ISO 27000  
C) NIST CSF  
D) PCI DSS  
E) COBIT

**Respuesta correcta**: 
	E) COBIT  
	**Justificación**: COBIT es un marco de gobernanza de TI que incluye principios y prácticas para la gestión y gobierno de la ciberseguridad, no solo se centra en los aspectos técnicos.

---

**Pregunta 15**: ¿Cuál de los siguientes marcos sería más adecuado para una organización que busca un conjunto de controles de ciberseguridad pragmáticos y centrados en la práctica?

A) CIS Controls  
B) ISO 27000  
C) NIST CSF  
D) PCI DSS  
E) COBIT

**Respuesta correcta**: 
	A) CIS Controls  
	**Justificación**: CIS Controls es un conjunto de prácticas recomendadas que se centran en un conjunto de controles de ciberseguridad prácticos y efectivos.

---

**Pregunta 16**: Si tu organización está interesada en un marco de ciberseguridad que sea compatible con las normas internacionales y que se centre en un enfoque de gestión de la seguridad de la información, ¿cuál de los siguientes sería la mejor opción?

A) CIS Controls  
B) ISO 27000  
C) NIST CSF  
D) PCI DSS  
E) COBIT

**Respuesta correcta**: 
	B) ISO 27000  
	**Justificación**: La serie ISO 27000 proporciona un enfoque internacionalmente reconocido para la gestión de la seguridad de la información.}


---
PEP 1 : 02/11/2022

**Pregunta 1**: Marco de trabajo que permite el reconocimiento de tácticas y técnicas utilizadas por un atacante sobre un sistema. Alguna de sus 14 tácticas son el reconocimiento, desarrollo de recursos y acceso inicial, filtración e impacto.

A) STRIDE  
B) CyberKill Chain  
C) CAPEC  
D) Mitre Att&ck Framework  
E) Ninguna de las anteriores

**Respuesta correcta**: 
	D) Mitre Att&ck Framework

---

**Pregunta 2**: Las siguientes son características de los controles CIS:  
i. Ayuda a los defensores a identificar los puntos más críticos que deben hacer para detener los ataques más importantes.  
ii. Sus primeros controles apuntan a identificar y controlar activos.  
iii. Se definen con el principio de “ofensiva informa a la defensiva”.  
iv. Todas sus recomendaciones individuales son específicas y prácticas de implementar.  
v. Establece las prácticas más fundamentales y valiosas que toda empresa debería considerar.

A) i, ii  
B) i, ii, iii  
C) i, ii, iii, iv  
D) i, ii, iii, iv, v  
E) i, ii, iii, v

**Respuesta correcta**: 
	D) i, ii, iii, iv, v

---

**Pregunta 3**: A la hora de defender la necesidad de invertir en nuevos controles de ciberseguridad, la estimación de costos y beneficios es un desafío ¿Por qué?

A) Es difícil estimar los beneficios de las políticas y mecanismos de seguridad.  
B) La seguridad a través de la oscuridad es una práctica habitual en las organizaciones.  
C) Los activos de la organización en el ciberespacio están bajo amenaza constante.  
D) Todas las anteriores  
E) Ninguna de las anteriores

**Respuesta correcta**: 
	a

---

**Pregunta 4**: Buena práctica, estándar o metodología que identifica controles de seguridad en cada etapa del ciclo de vida del software.

A) CWE Top 25  
B) OWASP SAMM  
C) Microsoft SDL  
D) NIST SP800-53  
E) LINDDUN

**Respuesta correcta**: 
	C) Microsoft SDL

---

**Pregunta 5**: ¿A cuál de los siguientes estándares, metodologías o buenas prácticas corresponde el siguiente objetivo:  
“Enfoque priorizado, flexible, repetible, basado en el desempeño y costo efectivo, que incluya medidas de seguridad de la información y controles que los propietarios y operadores de infraestructura crítica puedan adoptar voluntariamente para ayudarlos a identificar, evaluar y gestionar los riesgos cibernéticos”?

A) ISO 27000  
B) NIST Cybersecurity Framework  
C) CIS Controls  
D) COBIT  
E) Ninguna de las anteriores

**Respuesta correcta**: 
	B) NIST Cybersecurity Framework

---

**Pregunta 6**: Entre los objetivos del PCI DSS se tienen:  
i. Construir y mantener una red y sistemas seguros  
ii. Reglas de comportamiento (uso aceptable)  
iii. Proteger los datos del titular de la tarjeta de crédito  
iv. Mantener una política de seguridad de la información  
v. Monitorear y probar redes regularmente

Son verdaderas:

A) ii, iii, iv y v  
B) i, ii, iii y iv  
C) i, iii y iv  
D) i, iii, iv y v  
E) Todas son verdaderas

**Respuesta correcta**: 
	D) i, iii, iv y v

---

**Pregunta 7**: Entre las categorías del SGP se tiene la gestión de la función de la ciberseguridad, esta consta de 12 funciones, entre las cuales se tiene:  
i. Gestión de personas  
ii. Gestión de la información  
iii. Gestión de la cadena de suministro  
iv. Continuidad del negocio  
v. Acceso a sistemas

Son verdaderas:

A) i, ii, iii y v  
B) i, ii, iv y v  
C) i, iii y iv  
D) ii, iii, iv y v  
E) Todas son verdaderas

**Respuesta correcta**: 
	a

---

**Pregunta 8**: Para crear un programa de ciberseguridad con el NIST CSF uno de los pasos es crear el perfil actual de la organización. Para ello es esencial contar con:  
i. Objetivos de la organización  
ii. Ambiente de amenazas en que se desenvuelve  
iii. Requerimientos y controles actuales  
iv. Análisis de riesgos

Son verdaderas:

A) i, ii y iii  
B) i y ii  
C) i, iii y iv  
D) ii, iii, iv  
E) Todas son verdaderas

**Respuesta correcta**: 
	a