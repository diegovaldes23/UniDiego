
---

### **¿Qué es el paralelismo?**

- **Descripción:** El paralelismo divide un problema complejo en tareas más pequeñas que pueden ejecutarse al mismo tiempo en varios procesadores.
- **Para qué sirve:** Acelera la resolución de problemas grandes, como simulaciones científicas, al aprovechar múltiples procesadores a la vez.
- **Ejemplo:** Simular el clima global se vuelve más rápido cuando varias computadoras calculan diferentes partes del modelo climático simultáneamente.

---

### **Velocidad secuencial**

- **Descripción:** Es la velocidad a la que un procesador ejecuta instrucciones, medida en gigahercios (GHz).
- **Para qué sirve:** Determina cuántas instrucciones puede manejar un procesador por segundo. Importante para aplicaciones donde cada milisegundo cuenta.
- **Ejemplo:** Un procesador de 3.0 GHz puede ejecutar hasta 3 mil millones de instrucciones por segundo, ideal para videojuegos o simulaciones en tiempo real.

---

### **Aplicaciones Grand Challenge**

- **Descripción:** Problemas científicos o de ingeniería tan grandes que requieren supercomputación para resolverlos.
- **Para qué sirve:** Abordan desafíos como el análisis del genoma humano o simulaciones detalladas de sistemas físicos complejos.
- **Ejemplo:** Simular la estructura de proteínas puede tomar días en un supercomputador, pero sería imposible en una computadora normal.

---

### **Supercomputadores paralelos actuales**

- **Descripción:** Computadoras que utilizan muchos procesadores pequeños trabajando juntos para resolver partes de un problema más grande.
- **Para qué sirve:** Se utilizan para resolver problemas grandes de manera más eficiente, como análisis de datos a gran escala.
- **Ejemplo:** Un supercomputador moderno puede analizar millones de datos genéticos al mismo tiempo para identificar patrones de enfermedades.

---

### **OpenMP**

- **Descripción:** Un estándar para programar en paralelo utilizando memoria compartida entre varios procesadores.
- **Para qué sirve:** Facilita la creación de aplicaciones paralelas, permitiendo que las tareas se distribuyan entre múltiples procesadores en sistemas de memoria compartida.
- **Ejemplo:** Usando OpenMP, puedes dividir el procesamiento de una imagen grande entre varios procesadores, haciendo que la edición sea mucho más rápida.

---

### **Método Monte Carlo (Cálculo de π)**

- **Descripción:** Un método probabilístico para calcular valores aproximados mediante la generación de números aleatorios.
- **Para qué sirve:** Se utiliza para resolver problemas complejos como la estimación de integrales, usando simulaciones aleatorias.
- **Ejemplo:** Para calcular π, se generan puntos aleatorios dentro de un cuadrado y se compara cuántos caen dentro de un círculo inscrito. La proporción se utiliza para aproximar π.

---

### **Directiva parallel de OpenMP**

- **Descripción:** Permite que un bloque de código se ejecute en paralelo por varias hebras, dividiendo el trabajo.
- **Para qué sirve:** Distribuye tareas entre varios procesadores para mejorar la eficiencia en aplicaciones paralelas.
- **Ejemplo:** Al procesar una lista de números, cada hebra puede calcular una parte diferente, acelerando el cálculo total.

---

### **Paralelismo anidado**

- **Descripción:** Permite que regiones paralelas existan dentro de otras regiones paralelas.
- **Para qué sirve:** Facilita la programación de algoritmos complejos que requieren múltiples niveles de paralelización.
- **Ejemplo:** En una simulación climática, una hebra podría encargarse de simular el océano, y dentro de esa tarea, otras hebras podrían simular las corrientes oceánicas.

---

### **Locks (bloqueos)**

- **Descripción:** Son mecanismos que aseguran que solo una hebra pueda acceder a una sección crítica de código a la vez.
- **Para qué sirve:** Previenen condiciones de carrera y aseguran que los datos compartidos no se corrompan cuando varias hebras acceden a ellos simultáneamente.
- **Ejemplo:** Si varias hebras intentan escribir en la misma base de datos al mismo tiempo, un lock aseguraría que solo una hebra pueda hacerlo mientras las otras esperan.

---

### **Tasks en OpenMP**

- **Descripción:** Son unidades de trabajo que pueden ser ejecutadas de forma paralela y asíncrona por cualquier hebra disponible.
- **Para qué sirve:** Facilita la paralelización de trabajos irregulares o no estructurados, como recorrer listas enlazadas o árboles.
- **Ejemplo:** En un algoritmo de búsqueda, cada nodo de un árbol puede procesarse como una tarea independiente, permitiendo una exploración más rápida del árbol.

---

### **Condición de carrera**

- **Descripción:** Ocurre cuando el resultado de un programa depende del orden en que se ejecutan las hebras o procesos.
- **Para qué sirve:** Identificar y evitar estos errores es crucial en programación paralela para garantizar que los resultados sean correctos y reproducibles.
- **Ejemplo:** Si dos hebras intentan aumentar el valor de una variable compartida al mismo tiempo sin sincronización, el valor final puede ser incorrecto.

---

### **Exclusión mutua**

- **Descripción:** Mecanismo que asegura que solo una hebra o proceso pueda acceder a una sección crítica a la vez.
- **Para qué sirve:** Evita que varias hebras modifiquen datos compartidos al mismo tiempo, lo que podría causar errores en los resultados.
- **Ejemplo:** En un sistema de ventas, la exclusión mutua asegura que dos personas no puedan comprar el mismo asiento en un vuelo simultáneamente.

---

### **Sección crítica**

- **Descripción:** Parte del código donde el acceso a recursos compartidos debe ser controlado para evitar conflictos entre las hebras.
- **Para qué sirve:** Protege los datos compartidos para que solo una hebra a la vez pueda modificarlos.
- **Ejemplo:** Al actualizar el saldo de una cuenta bancaria en una aplicación, la sección crítica asegura que solo una transacción se procese a la vez.

---

### **Modelo de memoria OpenMP**

- **Descripción:** OpenMP utiliza un modelo de memoria compartida, donde las hebras pueden acceder a las mismas variables globales, pero también pueden tener variables privadas.
- **Para qué sirve:** Facilita la comunicación y sincronización entre hebras, pero requiere cuidado para evitar condiciones de carrera.
- **Ejemplo:** En un programa que multiplica matrices, las variables privadas permiten que cada hebra procese un conjunto específico de datos sin interferir con otras hebras.

---

### **Semáforos**

- **Descripción:** Variables utilizadas para controlar el acceso a recursos compartidos entre hebras o procesos en un sistema.
- **Para qué sirve:** Garantizan que un número limitado de hebras o procesos puedan acceder a un recurso compartido, como un archivo o una base de datos.
- **Ejemplo:** Un semáforo puede permitir que solo cinco usuarios accedan a un archivo a la vez en una aplicación de almacenamiento en la nube.

---

### **Barreras en OpenMP**

- **Descripción:** Puntos de sincronización en los que todas las hebras deben llegar antes de que alguna de ellas pueda continuar.
- **Para qué sirve:** Garantiza que todas las hebras terminen su trabajo antes de que se pase a la siguiente fase del programa.
- **Ejemplo:** En una simulación científica, las hebras que procesan diferentes secciones de una imagen deben esperar en una barrera hasta que todas terminen antes de combinar sus resultados.

---

### **Reducción en OpenMP**

- **Descripción:** Técnica que permite combinar los resultados de operaciones realizadas por varias hebras en una única variable compartida.
- **Para qué sirve:** Útil cuando necesitas sumar, multiplicar o realizar otras operaciones acumulativas en paralelo, sin riesgo de condiciones de carrera.
- **Ejemplo:** Si cada hebra está sumando un conjunto de valores, la cláusula `reduction(+:sum)` asegura que al final todas las sumas se combinen correctamente en una sola variable `sum`.

---

### **Locks anidados**

- **Descripción:** Un tipo de lock que permite que la misma hebra lo adquiera varias veces sin liberar el lock.
- **Para qué sirve:** Asegura que una hebra pueda entrar en una sección crítica varias veces sin bloquearse a sí misma.
- **Ejemplo:** En una aplicación de procesamiento de imágenes, si una hebra entra en una función recursiva y necesita acceder a recursos compartidos en cada nivel de recursión, un lock anidado lo permitirá sin bloquearse.

---

### **Flush en OpenMP**

- **Descripción:** Operación que asegura que las hebras tengan una visión consistente de la memoria al sincronizar las variables compartidas.
- **Para qué sirve:** Garantiza que todas las operaciones de escritura realizadas por una hebra sean visibles para las demás hebras.
- **Ejemplo:** En una aplicación de cálculo científico, antes de que una hebra lea los resultados de otra hebra, se puede usar `flush` para asegurarse de que esté leyendo los datos más recientes.

---

### **Tasks y paralelismo irregular**

- **Descripción:** Los tasks permiten dividir el trabajo de manera dinámica, adaptándose mejor a estructuras de datos como listas enlazadas o árboles, donde la carga de trabajo no es homogénea.
- **Para qué sirve:** Es ideal para programas que requieren dividir el trabajo en partes no predecibles, como búsquedas o algoritmos de grafos.
- **Ejemplo:** En un algoritmo de búsqueda en un árbol, cada nodo puede ser procesado por un task independiente, permitiendo que las ramas del árbol se procesen simultáneamente.

---

### **Modelo de concurrencia**

- **Descripción:** Un modelo donde múltiples tareas o procesos se ejecutan simultáneamente, compartiendo recursos como memoria o dispositivos de entrada/salida.
- **Para qué sirve:** Facilita la ejecución eficiente de aplicaciones multitarea, distribuyendo las cargas de trabajo entre múltiples hebras o procesos.
- **Ejemplo:** Un servidor web puede usar concurrencia para atender múltiples solicitudes de usuarios al mismo tiempo, sin bloquearse mientras se procesan las respuestas.

---

### **Atomicidad**

- **Descripción:** Garantía de que una operación se ejecute completamente sin ser interrumpida por otras hebras.
- **Para qué sirve:** Previene que otras hebras interfieran en una operación mientras está en proceso, asegurando consistencia en datos compartidos.
- **Ejemplo:** En una base de datos, una transferencia de dinero entre cuentas debe ser atómica para asegurar que ambas cuentas se actualicen correctamente, sin interferencias.

---

### **Solución de Peterson**

- **Descripción:** Un algoritmo de software para garantizar exclusión mutua entre dos procesos o hebras.
- **Para qué sirve:** Asegura que dos hebras no entren simultáneamente en su sección crítica, evitando condiciones de carrera.
- **Ejemplo:** En un programa donde dos hebras modifican una variable compartida, la solución de Peterson garantiza que solo una hebra acceda a la variable a la vez.

---

### **Algoritmo de la panadería**

- **Descripción:** Un algoritmo que permite a múltiples hebras acceder a la sección crítica, asignando un "ticket" a cada una para determinar su turno.
- **Para qué sirve:** Proporciona exclusión mutua en sistemas donde varias hebras compiten por recursos compartidos.
- **Ejemplo:** Similar a una panadería real, las hebras toman un número y esperan su turno para entrar a la sección crítica, garantizando un acceso justo y ordenado.

---

### **Mutex (Exclusión mutua)**

- **Descripción:** Un mecanismo de sincronización que permite a las hebras adquirir y liberar un bloqueo, asegurando que solo una hebra acceda a un recurso a la vez.
- **Para qué sirve:** Previene condiciones de carrera al controlar el acceso exclusivo a recursos compartidos.
- **Ejemplo:** Un mutex puede usarse para proteger una base de datos de accesos simultáneos, asegurando que solo un cliente pueda realizar cambios en la base de datos a la vez.

---

### **Variables de condición**

- **Descripción:** Un mecanismo que permite a las hebras bloquearse y esperar hasta que otra hebra las notifique para continuar.
- **Para qué sirve:** Facilita la coordinación entre hebras, permitiendo que una hebra espere hasta que una condición específica se cumpla.
- **Ejemplo:** En un programa productor-consumidor, las variables de condición pueden usarse para que los consumidores esperen hasta que el productor haya agregado más elementos al buffer.

---

### **Cláusula `schedule` en OpenMP**

- **Descripción:** Controla cómo se distribuyen las iteraciones de un bucle entre las hebras, permitiendo diferentes estrategias de distribución (estática, dinámica, guiada).
- **Para qué sirve:** Optimiza la carga de trabajo en bucles paralelos, adaptándose a la variabilidad en los tiempos de ejecución de las iteraciones.
- **Ejemplo:** Usar `schedule(dynamic, 2)` para asignar dos iteraciones a cada hebra, ajustando dinámicamente la carga según terminen su trabajo.

---

### **Construcción `single` en OpenMP**

- **Descripción:** Especifica que un bloque de código debe ser ejecutado solo por una hebra, independientemente de cuántas hebras estén disponibles.
- **Para qué sirve:** Utilizado para tareas que solo necesitan ejecutarse una vez, como inicializaciones o cálculos únicos.
- **Ejemplo:** En una simulación, solo una hebra puede cargar los datos iniciales, mientras que las demás esperan a que termine antes de continuar.

---

### **Construcción `master` en OpenMP**

- **Descripción:** Indica que solo la hebra maestra (hebra principal) ejecutará un bloque de código, sin barrera implícita al inicio o al final.
- **Para qué sirve:** Utilizado para tareas específicas que solo deben ser realizadas por la hebra maestra.
- **Ejemplo:** La hebra maestra puede encargarse de consolidar los resultados de todas las hebras al final de una simulación.

---

### **Construcción `ordered` en OpenMP**

- **Descripción:** Garantiza que las iteraciones de un bucle se ejecuten en el orden secuencial, incluso si se están ejecutando en paralelo.
- **Para qué sirve:** Asegura la ejecución ordenada de secciones de un bucle que no pueden ser ejecutadas fuera de secuencia.
- **Ejemplo:** En una simulación de procesamiento de datos, algunas partes del bucle deben ejecutarse en orden, como los pasos finales de un cálculo.

---

### **Barrera implícita en OpenMP**

- **Descripción:** Un punto de sincronización donde todas las hebras deben esperar a que las demás terminen antes de continuar.
- **Para qué sirve:** Garantiza que todas las hebras han completado su trabajo en una sección antes de avanzar a la siguiente fase del programa.
- **Ejemplo:** Después de paralelizar el cálculo de una matriz, las hebras deben esperar en una barrera para asegurarse de que todas hayan completado su parte antes de combinar los resultados.

---

### **Claúsula `reduction` en OpenMP**

- **Descripción:** Permite combinar los resultados parciales de varias hebras en una única variable compartida al finalizar el bloque paralelo.
- **Para qué sirve:** Asegura que los cálculos acumulativos (como sumas o productos) se realicen correctamente al trabajar en paralelo.
- **Ejemplo:** Al sumar los elementos de un arreglo en paralelo, `reduction(+:sum)` suma los resultados parciales de cada hebra en una sola variable `sum`.