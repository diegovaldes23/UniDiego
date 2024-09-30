
### **Soluciones por hardware 1 y 2:**

1. **Solución por hardware 1 - `test_and_set`:**
    
    - **Clave:** Es una instrucción atómica (indivisible) que prueba y cambia el valor de una variable en un solo paso.
    - **Cómo funciona:** El procesador lee y actualiza una variable de lock en memoria en una sola operación. Si la variable estaba libre (0), la bloquea (1).
    - **Ejemplo:** Dos hebras intentan adquirir un lock. La hebra que consigue cambiar el valor de la variable a 1 primero gana el acceso a la sección crítica.
2. **Solución por hardware 2 - `compare_and_swap` (CAS):**
    
    - **Clave:** Compara el valor de una variable con un valor esperado y, si coinciden, cambia el valor por uno nuevo.
    - **Cómo funciona:** Esta operación es también atómica. Se utiliza para actualizar variables compartidas de manera segura sin interrupción por otras hebras.
    - **Ejemplo:** Una hebra intenta cambiar el valor de una variable en memoria, pero solo lo logra si el valor actual coincide con el valor esperado. Si no, la operación se repite hasta tener éxito.

---

### **Soluciones por software:**

1. **Solución por software 1 - Algoritmo de Peterson:**
    
    - **Clave:** Un algoritmo que garantiza exclusión mutua entre dos hebras, usando variables booleanas y un turno compartido.
    - **Cómo funciona:** Las hebras indican que quieren entrar a la sección crítica y ceden el turno si otra hebra también quiere entrar. La hebra con turno entra a la sección crítica.
    - **Ejemplo:** Dos hebras intentan acceder a una variable compartida. El algoritmo decide cuál de las dos entra primero basado en el turno, mientras que la otra espera.
2. **Algoritmo de la panadería:**
    
    - **Clave:** Un algoritmo que extiende el algoritmo de Peterson para múltiples hebras, usando "tickets" como en una panadería.
    - **Cómo funciona:** Cada hebra toma un "número" (ticket) y espera su turno según el valor de su ticket. La hebra con el número más bajo entra a la sección crítica.
    - **Ejemplo:** Varias hebras quieren acceder a la SC. Cada una toma un ticket y esperan hasta que llegue su turno de acceder, asegurando orden justo.

---

### **Soluciones por sistema operativo (SO):**

1. **Semáforos:**
    
    - **Clave:** Un semáforo es una variable entera que controla el acceso a los recursos compartidos mediante operaciones de señalización (`wait` y `signal`).
    - **Cómo funciona:** Las hebras ejecutan una operación `wait` antes de entrar a la SC, y una operación `signal` al salir. El semáforo asegura que solo un número limitado de hebras puedan acceder a la SC al mismo tiempo.
    - **Ejemplo:** Un semáforo binario asegura que solo una hebra pueda entrar a la sección crítica. O bien, un semáforo con un contador mayor permite que hasta N hebras accedan simultáneamente.
2. **Locks y Mutexes:**
    
    - **Locks:**
        
        - **Clave:** Son mecanismos que aseguran que solo una hebra pueda acceder a la sección crítica. Utilizan operaciones `lock.acquire()` y `lock.release()`.
        - **Cómo funciona:** Una hebra adquiere el lock al entrar a la SC, bloqueando a las demás. Luego libera el lock al salir, permitiendo que otras hebras entren.
        - **Ejemplo:** Un sistema de archivos usa locks para asegurar que solo un proceso pueda escribir en un archivo a la vez.
    - **Mutex (Mutual Exclusion Object):**
        
        - **Clave:** Similar a un lock, pero más específicamente diseñado para proteger secciones críticas en un entorno multihilo.
        - **Cómo funciona:** Las hebras bloquean y desbloquean el mutex para garantizar que solo una pueda acceder a la SC a la vez.
        - **Ejemplo:** En un servidor web, un mutex puede proteger el acceso a una lista de clientes activos para evitar que dos hebras modifiquen la lista al mismo tiempo.

---

### **Tabla Comparativa (Actualizada):**

| **Solución**                    | **Implementación** | **Ventaja**                                               | **Desventaja**                                         | **Usos Típicos**                                    |
| ------------------------------- | ------------------ | --------------------------------------------------------- | ------------------------------------------------------ | --------------------------------------------------- |
| `test_and_set`                  | Hardware           | Sencillo, atómico, y eficiente en hardware.               | Busy-waiting, posible consumo de CPU alto.             | Exclusión mutua simple en sistemas de bajo nivel.   |
| `compare_and_swap` (CAS)        | Hardware           | Elimina las condiciones de carrera sin locks.             | Más complejo que `test_and_set`.                       | Implementación de estructuras lock-free.            |
| Algoritmo de Peterson           | Software           | Simple, garantiza exclusión mutua entre dos hebras.       | Solo funciona para dos hebras.                         | Exclusión mutua en problemas simples (2 hebras).    |
| Algoritmo de la panadería       | Software           | Garantiza orden justo en SC para múltiples hebras.        | Algo complejo y menos eficiente que hardware.          | Exclusión mutua con múltiples hebras.               |
| Semáforos                       | SO                 | Controla el acceso a recursos limitados, flexible.        | Puede complicarse con deadlocks.                       | Control de acceso a recursos compartidos.           |
| Locks                           | SO                 | Fácil de usar, protegen SC de forma confiable.            | Posibles problemas de deadlock si no se maneja bien.   | Exclusión mutua en aplicaciones concurrentes.       |
| Mutex                           | SO                 | Protege eficientemente SC en multihilos.                  | Deadlock si no se libera correctamente.                | Protección de SC en aplicaciones multithreaded.     |
| Problema Productor-Consumidor   | SO/Semáforo/Mutex  | Solución clásica de sincronización eficiente.             | Necesita coordinación cuidadosa para evitar deadlocks. | Buffer compartido entre productor y consumidor.     |
| Sincronización con hebras POSIX | SO/Condiciones     | Variables de condición permiten sincronización eficiente. | Puede complicarse si no se maneja correctamente.       | Sincronización eficiente en aplicaciones multihilo. |
|                                 |                    |                                                           |                                                        |                                                     |

