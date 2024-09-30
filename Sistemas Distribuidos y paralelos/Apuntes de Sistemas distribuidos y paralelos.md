
### Índice:

1. **¿Qué es el paralelismo?**
2. **Velocidad secuencial**
3. **Aplicaciones Grand Challenge**
4. **Supercomputadores tradicionales**
5. **Supercomputadores paralelos actuales**
6. **Historia: Seymour Cray**
7. **Cray Computers**
8. **Procesadores escalares**
9. **Procesadores super escalares**
10. **Procesadores vectoriales**
11. **Intel Core 2 Duo**
12. **Multiprocesadores de memoria compartida**
13. **Multiprocesadores de memoria distribuida**
14. **Clúster de computadores**
15. **Tendencias actuales**
16. **Taxonomía Flynn**
17. **Supercomputadores modernos**
18. **Ranking de los computadores más veloces**

### Capítulo 1:

1. **¿Qué es el paralelismo?**  
    El paralelismo es una estrategia utilizada para resolver problemas computacionales complejos más rápidamente, dividiendo el problema en tareas más pequeñas, asignándolas a varios procesadores que operan simultáneamente y coordinando estos procesos. Un ejemplo común es la simulación de clima global, donde la resolución requiere un procesamiento intensivo que sólo puede ser manejado con computadoras paralelas.
    
2. **Velocidad secuencial**  
    Un procesador moderno de 3.0 GHz puede ejecutar hasta mil millones de instrucciones por segundo, aunque en aplicaciones grandes y paralelas, se requieren trillones de operaciones por segundo. Este rendimiento se ve afectado por factores como la memoria cache y la contención del bus.
    
3. **Aplicaciones Grand Challenge**  
    Estos son problemas científicos y de ingeniería de gran escala que requieren supercomputación, como el modelado global del clima, la investigación del genoma humano y simulaciones de química computacional. Ejemplo: Simular la dinámica de proteínas con un supercomputador puede tomar semanas.
    
4. **Supercomputadores tradicionales**  
    Los supercomputadores del pasado usaban procesadores especializados, lo que ofrecía un rendimiento superior pero a un costo muy elevado y con limitaciones en cuanto a tecnología de enfriamiento y escalabilidad.
    
5. **Supercomputadores paralelos actuales**  
    En lugar de procesadores dedicados, se utilizan muchos procesadores más pequeños que trabajan en paralelo para resolver partes del problema. Aunque es más barato, requiere nuevas tecnologías de software y una reescritura de códigos secuenciales.
    
6. **Historia: Seymour Cray**  
    Seymour Cray es considerado el padre de la supercomputación. Desarrolló algunos de los primeros supercomputadores, como el Cray-1, que introdujo la computación vectorial.
    
7. **Cray Computers**  
    Ejemplos de supercomputadores desarrollados por Cray incluyen el Cray-1 (1976) y el Cray XK6 (2011), que ofrecen capacidades significativamente diferentes en términos de rendimiento y tecnología.
    
8. **Procesadores escalares**  
    Un procesador escalar ejecuta una instrucción por ciclo de reloj, y su rendimiento puede ser limitado en aplicaciones que requieren un procesamiento intensivo.

### Descripción del pipelining:

- **Pipelining** es una técnica utilizada en los procesadores para mejorar su rendimiento. Consiste en dividir la ejecución de una instrucción en diferentes etapas, donde cada etapa realiza una parte del trabajo.

### Explicación de las etapas:

1. **IF (Instruction Fetch)**: En esta etapa, el procesador busca (fetch) la instrucción desde la memoria.
2. **DE (Decode)**: En esta etapa, el procesador decodifica la instrucción, es decir, interpreta qué operación debe realizar.
3. **EX (Execute)**: Aquí se realiza la operación aritmética o lógica especificada por la instrucción.
4. **WB (Write Back)**: Finalmente, el resultado de la operación se escribe de vuelta en el registro correspondiente.

### Funcionamiento del pipelining:

- En un procesador escalar sin pipelining, se ejecutaría una instrucción completa antes de comenzar la siguiente, lo cual es ineficiente porque algunas unidades del procesador estarían inactivas durante partes del ciclo.
- Con pipelining, varias instrucciones se superponen en el tiempo. Mientras una instrucción está en la etapa de "IF", otra puede estar en "DE", otra en "EX", y otra en "WB". Así, el procesador está utilizando todas las unidades simultáneamente, lo que maximiza la eficiencia.

### El gráfico:

- El gráfico a la derecha muestra esta superposición. En el eje vertical se representan las diferentes instrucciones (1, 2, 3, 4, etc.) y en el eje horizontal se muestra el tiempo en ciclos de reloj.
- La primera instrucción comienza su ciclo en la etapa de "IF" (ciclo 1), luego pasa a "DE" (ciclo 2), "EX" (ciclo 3) y "WB" (ciclo 4).
- Mientras la primera instrucción está en "DE", la segunda instrucción puede comenzar su ciclo en "IF". Esto es lo que genera la "tubería" de instrucciones superpuestas. 

			![[Pasted image 20240923102349.png]]

---


9. **Procesadores super escalares**  
    Estos procesadores pueden emitir varias instrucciones por ciclo, lo que aumenta el rendimiento al ejecutar instrucciones en paralelo, siempre que las instrucciones sean independientes.

#### Procesador superescalar:

- Un **procesador superescalar** tiene múltiples pipelines, lo que significa que puede emitir más de una instrucción por ciclo de reloj, siempre y cuando estas instrucciones sean independientes entre sí.
- Cada línea horizontal en el gráfico representa una **instrucción** diferente (1, 2, 3, etc.).
- Cada instrucción sigue las etapas del pipeline: **IF (Instruction Fetch)**, **DE (Decode)**, **EX (Execute)** y **WB (Write Back)**.

### Interpretación del gráfico:

- En este gráfico, las instrucciones se están ejecutando en **paralelo** en varias pipelines, aprovechando la capacidad del procesador para emitir múltiples instrucciones en cada ciclo de reloj.
- La **instrucción 1** comienza en el ciclo 1 en la etapa de **IF** y luego avanza a las etapas siguientes.
- Mientras tanto, la **instrucción 2** se emite en paralelo y también comienza en **IF** en el ciclo 1, pero utilizando una pipeline diferente.
- Lo mismo sucede con las **instrucciones 3 y 4**; todas estas instrucciones se emiten y avanzan simultáneamente a través de las diferentes etapas del pipeline.

				![[Pasted image 20240929180941.png]]
### Clave del superescalar:

- La capacidad de ejecutar múltiples instrucciones en paralelo depende de que las instrucciones sean **independientes entre sí**. Si no lo son, pueden ocurrir **dependencias** que obligan a que algunas instrucciones esperen a que otras finalicen, lo que reduce la eficiencia.

### Comparación con un procesador escalar:

- En un **procesador escalar**, solo una instrucción se procesaría en cada ciclo, por lo que la segunda instrucción tendría que esperar hasta que la primera completara todas las etapas antes de comenzar.
- En cambio, en un **procesador superescalar**, varias instrucciones pueden procesarse simultáneamente en diferentes pipelines, como lo muestra este gráfico.


    
10. **Procesadores vectoriales**  
    Los procesadores vectoriales ejecutan una operación sobre varios datos simultáneamente. Aunque son costosos, son útiles para aplicaciones específicas como simulaciones científicas.
    
11. **Intel Core 2 Duo**  
    Este procesador introdujo la idea de pipelines más amplios y la compartición de cache L2 entre núcleos, lo que mejoró el rendimiento en aplicaciones multitarea.
    
12. **Multiprocesadores de memoria compartida**  
    En este tipo de arquitectura, varios procesadores comparten el mismo espacio de memoria, lo que permite un acceso uniforme o no uniforme a la memoria, dependiendo de la configuración.
    
13. **Multiprocesadores de memoria distribuida**  
    Cada procesador tiene su propia memoria y los nodos se comunican a través de redes de paso de mensajes, lo que permite una mejor escalabilidad en aplicaciones paralelas.
    
14. **Clúster de computadores**  
    Un clúster está compuesto de varios computadores conectados a través de una red. Aunque es barato y fácil de escalar, presenta limitaciones en términos de rendimiento de I/O.
    
15. **Tendencias actuales**  
    Las tendencias incluyen la memoria distribuida compartida, procesadores many-core, computación en la nube HPC, y virtualización.
    
16. **Taxonomía Flynn**  
    Esta clasificación agrupa las arquitecturas de computación según la cantidad de instrucciones y datos procesados simultáneamente (SISD, SIMD, MIMD).
    
17. **Supercomputadores modernos**  
    Los supercomputadores modernos emplean procesadores pequeños trabajando en paralelo, son más baratos y escalables pero requieren software especializado para gestionar la programación paralela.
    
18. **Ranking de los computadores más veloces**  
    Los supercomputadores se miden por el benchmark LINPACK, que evalúa la velocidad en operaciones de punto flotante. Ejemplo: El supercomputador Frontier es el más rápido del mundo con 1206 petaflops.


Aquí tienes una tabla comparativa entre los procesadores escalar, superescalar y vectorial:

| **Característica**    | **Procesador Escalar**                                                                      | **Procesador Superescalar**                                                                               | **Procesador Vectorial**                                                                                       |
| --------------------- | ------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------- |
| **Definición**        | Ejecuta una sola instrucción por ciclo de reloj.                                            | Puede emitir y ejecutar múltiples instrucciones por ciclo de reloj.                                       | Ejecuta una operación sobre múltiples datos en paralelo.                                                       |
| **Funcionamiento**    | Procesa las instrucciones una por una, pasando por las etapas del pipeline secuencialmente. | Procesa múltiples instrucciones en paralelo utilizando varias pipelines, siempre que sean independientes. | Procesa un conjunto de datos como una sola unidad mediante una instrucción vectorial.                          |
| **Ventaja principal** | Simplicidad en la ejecución. Ideal para tareas secuenciales.                                | Mayor eficiencia al ejecutar varias instrucciones en paralelo.                                            | Eficiente para tareas que implican grandes volúmenes de datos como simulaciones científicas.                   |
| **Uso típico**        | Tareas secuenciales y simples.                                                              | Aplicaciones con alta concurrencia, donde las instrucciones pueden dividirse en partes independientes.    | Aplicaciones científicas o de ingeniería, como simulaciones numéricas, gráficos, etc.                          |
| **Pipelining**        | Un solo pipeline, ejecuta una instrucción a la vez.                                         | Múltiples pipelines, ejecuta varias instrucciones simultáneamente.                                        | Utiliza una técnica similar al pipelining pero aplicando una operación sobre un conjunto de datos en paralelo. |


---

### Capítulo 2:

### Índice:

1. **Concurrencia y sincronización**
2. **Beneficios de la concurrencia**
3. **Ejemplo de problema de concurrencia**
4. **Condición de carrera**
5. **Sección crítica**
6. **Exclusión mutua**
7. **Modelo de concurrencia**
8. **Requerimientos para una solución de exclusión mutua**
9. **Tipos de soluciones al problema de la sección crítica**
10. **Atomicidad**
11. **Solución por hardware**
12. **Soluciones por software**
13. **Solución de Peterson**
14. **Algoritmo de la panadería**
15. **Servicios del sistema operativo: Semáforos y Locks**
16. **Productor/consumidor con semáforos**
17. **Sincronización con hebras POSIX**
18. **Mutex**
19. **Variables de condición**
20. **Productor/consumidor usando pthreads**
21. **Barreras para hebras**
22. **Implementación de barreras con pthreads**

### Resumen de los temas:

1. **Concurrencia y sincronización**  
    La concurrencia ocurre cuando varias tareas (procesos o hebras) comparten un recurso simultáneamente. Se requiere sincronización para evitar la corrupción de los datos compartidos, como en el acceso a bases de datos o impresoras en sistemas distribuidos. Ejemplo: Dos hebras accediendo a una lista compartida.
    
2. **Beneficios de la concurrencia**  
    La concurrencia mejora el rendimiento al utilizar múltiples procesadores, aumentando el throughput y la interactividad de las aplicaciones. Ejemplo: Mientras una hebra realiza una operación de I/O, otras hebras pueden continuar su trabajo, mejorando la eficiencia global.
    
3. **Ejemplo de problema de concurrencia**  
    Si dos hebras intentan insertar un nodo en una lista compartida al mismo tiempo, el resultado puede depender del orden de ejecución, generando inconsistencias.
    
4. **Condición de carrera**  
    Se refiere a la situación donde el resultado de una operación depende del orden en que las hebras se ejecutan. Es un error potencial en aplicaciones concurrentes.
    
5. **Sección crítica**  
    Es un fragmento de código donde varias hebras acceden a recursos compartidos. Si al menos una hebra modifica estos recursos, debe garantizarse que sólo una hebra lo haga a la vez para evitar conflictos.
	    Si ninguna hebra modifica los datos (write) no hay SC
	    Si no hay recursos compartidos, no hay SC 
	    Si es mono hebra no hay SC
    
6. **Exclusión mutua**  
    Este concepto asegura que solo una hebra puede ejecutar una sección crítica a la vez. Se aplica en operaciones concurrentes como pop() y push() en un stack compartido.
    
7. **Modelo de concurrencia**  
    Las hebras tienen secciones críticas (CS) que requieren exclusión mutua. Las funciones `enterCS()` y `exitCS()` controlan la entrada y salida de estas secciones.
    
8. **Requerimientos para una solución de exclusión mutua**  
    Para que una solución sea correcta, debe cumplir con exclusión mutua, evitar deadlocks, prevenir inanición y garantizar el progreso de las hebras.
    
9. **Tipos de soluciones al problema de la sección crítica**  
    Estas soluciones pueden implementarse por hardware, software, sistemas operativos o compiladores. Ejemplo: Uso de semáforos para controlar el acceso a las secciones críticas.

### **Requerimientos para una solución de Exclusión Mutua (EM):**

1. **Exclusión mutua:**
    
    - **Definición:** Cuando una hebra está en su sección crítica (SC), ninguna otra hebra puede estar en su SC al mismo tiempo.
    - **Ejemplo:** Si una hebra está actualizando el saldo de una cuenta bancaria, ninguna otra hebra debe modificar ese saldo hasta que la primera haya terminado.
2. **Sin deadlock:**
    
    - **Definición:** No debe ocurrir que todas las hebras queden bloqueadas indefinidamente intentando acceder a la sección crítica.
    - **Ejemplo:** Si dos hebras están esperando indefinidamente para entrar a la SC porque ambas necesitan que la otra termine, se produce un deadlock. La solución debe evitar esto.
3. **Sin inanición (starvation):**
    
    - **Definición:** Ninguna hebra debe quedar esperando para siempre sin poder entrar a su sección crítica.
    - **Ejemplo:** Si una hebra de baja prioridad nunca puede entrar a su SC porque las hebras de alta prioridad siempre la bloquean, está en inanición. Debe garantizarse que todas las hebras eventualmente entren a la SC.
4. **Progreso:**
    
    - **Definición:** Si una hebra intenta entrar a la sección crítica y esta está libre, debe poder entrar sin demoras injustificadas.
    - **Ejemplo:** Si una hebra verifica que la SC está libre, debe entrar inmediatamente sin ser bloqueada innecesariamente por otras hebras.

---

### **Notas importantes:**

- Una hebra puede tener más de una sección crítica.
- **Deadlock** implica inanición, pero **inanición** no siempre implica deadlock.
- No se puede asumir nada sobre la **velocidad** ni el **orden de ejecución** de las hebras. Es decir, la solución debe funcionar independientemente de estos factores.

---

### **Tipos de soluciones al problema de la Exclusión Mutua (SC):**

1. **Por hardware:**
    
    - **Definición:** Usar instrucciones nativas del procesador para asegurar la exclusión mutua.
    - **Ejemplo:** Instrucciones como `test_and_set` o `compare_and_swap` permiten que una hebra bloquee una sección crítica sin interferencias.
2. **Por software:**
    
    - **Definición:** Algoritmos en lenguajes de alto nivel que implementan la exclusión mutua.
    - **Ejemplo:** El **algoritmo de Peterson** es un ejemplo de solución por software para dos hebras, que garantiza que ambas no entren a la SC al mismo tiempo.
3. **Por sistema operativo (SO):**
    
    - **Definición:** Utilizar los servicios que ofrece el sistema operativo para gestionar la exclusión mutua.
    - **Ejemplo:** Usar **semaphores** o **mutexes** que proporciona el sistema operativo para evitar condiciones de carrera.
4. **Por compilador:**
    
    - **Definición:** Usar estructuras sintácticas propias del lenguaje que implementan la exclusión mutua.
    - **Ejemplo:** En **Java**, puedes usar el bloque `synchronized`, o en **C++**, utilizar `std::lock_guard` para proteger la SC.

10. **Atomicidad**  
    Una operación es atómica si se ejecuta completamente sin ser interrumpida. Esto es crucial para evitar errores en operaciones concurrentes.
    
11. **Solución por hardware**  
    Algunas soluciones deshabilitan interrupciones o usan instrucciones especiales de máquina como `testset()` para lograr exclusión mutua.
    
12. **Soluciones por software**  
    Ejemplo: La solución de Peterson garantiza exclusión mutua para dos hebras, aunque puede generar busy-waiting.
    
13. **Solución de Peterson**  
    Esta solución es un algoritmo que asegura exclusión mutua para dos procesos mediante el uso de banderas y un turno compartido. Es eficiente pero aplicable solo a dos hebras.
    
14. **Algoritmo de la panadería**  
    Este algoritmo permite la concurrencia para N hebras, utilizando un sistema de "tickets" como en una panadería, para determinar el orden en que las hebras acceden a la sección crítica.
    
15. **Servicios del sistema operativo: Semáforos y Locks**  
    Los semáforos son variables especiales usadas para señalizar a las tareas. Ejemplo: Un semáforo binario o mutex garantiza que sólo una hebra pueda acceder a una sección crítica a la vez.
    
16. **Productor/consumidor con semáforos**  
    En este problema, un productor genera datos que se almacenan en un buffer compartido, y un consumidor los toma uno a uno. Semáforos aseguran que no haya acceso simultáneo al buffer.
    
17. **Sincronización con hebras POSIX**  
    Las hebras POSIX definen mecanismos como mutexes y variables de condición para sincronizar múltiples hebras dentro de un proceso.
    
18. **Mutex**  
    Un mutex es similar a un semáforo binario y se usa para asegurar acceso exclusivo a una sección crítica. Ejemplo: Un mutex se bloquea antes de entrar a la sección crítica y se libera al salir.
    
19. **Variables de condición**  
    Permiten que una hebra se bloquee dentro de una sección crítica y libere el mutex asociado. Esto permite una sincronización más fina entre las hebras.
    
20. **Productor/consumidor usando pthreads**  
    Este patrón usa mutexes y variables de condición para implementar el acceso sincronizado entre un productor y un consumidor que comparten un buffer.
    
21. **Barreras para hebras**  
    Las barreras son puntos de sincronización donde todas las hebras deben llegar antes de continuar. Se utilizan en algoritmos que requieren sincronización global.
    
22. **Implementación de barreras con pthreads**  
    Las barreras se pueden implementar usando mutexes y variables de condición, y aseguran que las hebras se sincronicen en un punto específico del programa antes de continuar.
    

### **Tabla Comparativa (Actualizada):**

| **Solución**                                                                            | Foto                                 |
| --------------------------------------------------------------------------------------- | ------------------------------------ |
| **Solución por Hardware 1**: Deshabilitación de interrupciones                          | ![[Pasted image 20240929213521.png]] |
| **Solución por Hardware 2**: `test_and_set` -> Atómicas                                 | ![[Pasted image 20240929213603.png]] |
| **Solución por Software**: Algoritmos de exclusión mutua (Peterson, Panadería)          | ![[Pasted image 20240929213713.png]] |
| **Algoritmo de Peterson (Software)**: Por flags                                         | ![[Pasted image 20240929213726.png]] |
| **Algoritmo de la Panadería (Software)**: Por ticket de llegada                         | ![[Pasted image 20240929213812.png]] |
| **Semáforos (SO)**: `wait` (decrementa el semáforo) y `signal` (incrementa el semáforo) | ![[Pasted image 20240929213908.png]] |
| **Locks/Mutex (SO)**: Un semáforo binario que solo puede tomar los valores 0 o 1        | ![[Pasted image 20240929214132.png]] |
| **Problema Productor-Consumidor**: SO/Semáforo/Mutex                                    | ![[Pasted image 20240929214235.png]] |
| **Problema Productor-Consumidor (con sem)**: SO/Semáforo/Mutex                          | ![[Pasted image 20240929214243.png]] |

### Tabla actualizada con beneficios y contras:

| **Solución**                            | **Implementación**                                                  | **Beneficios**                                                             | **Contras**                                                                         |
| --------------------------------------- | ------------------------------------------------------------------- | -------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- |
| Solución por Hardware 1                 | Deshabilitación de interrupciones                                   | Sencillo de entender, garantiza exclusión mutua                            | No sirve para multiprocesadores, puede generar inanición, limita context-switching. |
| Solución por Hardware 2                 | `test_and_set` -> Atómicas                                          | Rápido, atómico, evita condiciones de carrera                              | Puede generar busy-waiting, consumo de CPU elevado, posible inanición.              |
| Solución por Software                   | Algoritmos (Peterson, Panadería)                                    | No necesita soporte de hardware, garantiza exclusión mutua                 | Complejidad alta, puede no escalar bien a múltiples hebras.                         |
| Algoritmo de Peterson (Software)        | Por flags                                                           | Sencillo para dos hebras, garantiza exclusión mutua                        | Solo funciona para dos hebras, difícil de extender.                                 |
| Algoritmo de la panadería (Software)    | Por ticket de llegada                                               | Garantiza orden justo, funciona para múltiples hebras                      | Algo complejo, menos eficiente en sistemas con muchas hebras.                       |
| Semáforos (SO)                          | `wait` (decrementa el semáforo) y `signal` (incrementa el semáforo) | Flexible, puede controlar el acceso a múltiples recursos simultáneamente   | Posible deadlock, requiere manejo cuidadoso.                                        |
| Locks/Mutex (SO)                        | Un semáforo binario solo puede tomar los valores 0 o 1              | Protege eficazmente las secciones críticas, fácil de usar                  | Posible deadlock si no se libera correctamente, puede provocar inanición.           |
| Problema Productor-Consumidor           | SO/Semáforo/Mutex                                                   | Solución clásica de sincronización, robusta y bien estudiada               | Complejidad adicional en implementación, riesgo de deadlock si no se gestiona bien. |
| Problema Productor-Consumidor (con sem) | SO/Semáforo/Mutex                                                   | Permite gestionar correctamente buffers compartidos entre múltiples hebras | Posible deadlock si se implementa mal.                                              |
| Sincronización con hebras POSIX         | SO/Condiciones                                                      | Permite sincronización eficiente mediante señales                          | Requiere una implementación cuidadosa, puede ser difícil de depurar.                |




---
### Capítulo 3:
### Índice del documento OpenMP

1. **¿Qué es OpenMP?**
2. **Beneficios de OpenMP**
3. **Hello world! en OpenMP/C**
4. **Modelo OpenMP de programación**
5. **Modelo OpenMP de ejecución**
6. **Modelo OpenMP de memoria**
7. **Construcción región paralela**
8. **Directivas y cláusulas**
9. **Variables de medio ambiente**
10. **Funciones runtime en OpenMP**
11. **Método Monte Carlo para cálculo de π**
12. **Solución OpenMP Monte Carlo de π**
13. **Directiva parallel**
14. **Paralelismo anidado**
15. **Atributos de compartición**
16. **Construcción for y schedule**
17. **Construcciones para sincronización**
18. **Locks y sincronización**
19. **Tasks en OpenMP**
20. **Paralelismo irregular con tasks**
21. **Sort con task**

---

### Resumen por tema:

1. **¿Qué es OpenMP?**  
    OpenMP es un estándar para la programación paralela en sistemas de memoria compartida. Se basa en extender lenguajes tradicionales como C/C++ y Fortran mediante directivas y funciones de biblioteca que permiten paralelización incremental y desarrollo de aplicaciones paralelas portátiles.
    
2. **Beneficios de OpenMP**  
    OpenMP permite el desarrollo fácil de aplicaciones paralelas de memoria compartida, sobre todo en aquellas que manipulan grandes matrices o arreglos. Su principal ventaja es la portabilidad y la escalabilidad casi lineal en experimentos con hasta 128 procesadores.
    
3. **Hello world! en OpenMP/C**  
    Un ejemplo sencillo en C usando OpenMP para crear múltiples hebras que ejecutan un bloque de código en paralelo, imprimiendo mensajes de cada hebra.
    
4. **Modelo OpenMP de programación**  
    En OpenMP, las hebras son generadas para dividir el trabajo en paralelo. Las variables pueden ser compartidas o privadas para cada hebra, y el control de la concurrencia y sincronización queda en manos del programador.
    
5. **Modelo OpenMP de ejecución**  
    La ejecución en OpenMP comienza con la hebra maestra, que crea hebras hijas para realizar trabajo paralelo. Cuando finaliza la región paralela, las hebras se sincronizan y la hebra maestra continúa.
    
6. **Modelo OpenMP de memoria**  
    OpenMP maneja memoria compartida entre hebras, donde cada hebra puede tener su propia visión temporal de la memoria y también memoria privada. La sincronización es esencial para evitar condiciones de carrera.
    
7. **Construcción región paralela**  
    La directiva `#pragma omp parallel` permite que un bloque de código sea ejecutado por varias hebras en paralelo. Se pueden especificar variables privadas o compartidas a través de cláusulas.
    
8. **Directivas y cláusulas**  
    OpenMP usa directivas como `parallel`, `for`, `sections` y `single`, con cláusulas como `private`, `shared`, `firstprivate` y `reduction` para controlar la paralelización y el comportamiento de las hebras.
    
9. **Variables de medio ambiente**  
    Variables como `OMP_NUM_THREADS` controlan la cantidad de hebras usadas, mientras que `OMP_SCHEDULE` define cómo se distribuyen las iteraciones de un bucle entre las hebras.
    
10. **Funciones runtime en OpenMP**  
    OpenMP proporciona funciones como `omp_get_num_threads()` y `omp_get_thread_num()` para controlar el entorno de ejecución paralela y sincronizar el acceso a los datos compartidos.
    
11. **Método Monte Carlo para cálculo de π**  
    El método Monte Carlo genera una secuencia de valores aleatorios para estimar el valor de π, utilizando una fórmula basada en la proporción del área de un círculo inscrito en un cuadrado.
    
12. **Solución OpenMP Monte Carlo de π**  
    El código en OpenMP divide el cálculo de π en varias hebras que suman resultados parciales, los cuales se combinan al final para obtener una estimación precisa.
    
13. **Directiva parallel**  
    La directiva `parallel` crea un equipo de hebras que ejecutan el bloque de código en paralelo. La hebra maestra coordina la creación de las hebras y continúa su ejecución después de la región paralela.
    
14. **Paralelismo anidado**  
    OpenMP permite la creación de regiones paralelas dentro de otras regiones paralelas, con la opción de habilitar el paralelismo anidado mediante la variable `OMP_NESTED`.
    
15. **Atributos de compartición**  
    Las variables en OpenMP pueden ser privadas, compartidas o `firstprivate`, determinando si cada hebra tiene su propia copia o si comparten la misma variable en memoria.
    
16. **Construcción for y schedule**  
    OpenMP distribuye automáticamente las iteraciones de un bucle `for` entre las hebras. La directiva `schedule` controla cómo se distribuyen las iteraciones, ya sea estática o dinámicamente.
    
17. **Construcciones para sincronización**  
    OpenMP ofrece construcciones como `barrier`, `flush` y `critical` para garantizar la correcta sincronización de las hebras, asegurando consistencia de datos y evitando condiciones de carrera.
    
18. **Locks y sincronización**  
    Los `locks` en OpenMP permiten controlar el acceso a recursos compartidos, asegurando que solo una hebra pueda acceder a una sección crítica a la vez.
    
19. **Tasks en OpenMP**  
    Los tasks permiten asignar trabajo concurrente de manera no estructurada, útil en el procesamiento de estructuras de datos como listas y árboles. Las tareas se ejecutan asíncronamente y pueden ser manejadas por cualquier hebra disponible.
    
20. **Paralelismo irregular con tasks**  
    Ejemplos de paralelismo irregular incluyen la paralelización del procesamiento de una lista enlazada, donde las tareas son creadas dinámicamente y ejecutadas en paralelo por varias hebras.
    
21. **Sort con task**  
    Un ejemplo práctico de tareas en OpenMP es el algoritmo de ordenación `sort`, donde se dividen las tareas de ordenamiento en pequeños bloques paralelizados, optimizando el rendimiento en matrices grandes.