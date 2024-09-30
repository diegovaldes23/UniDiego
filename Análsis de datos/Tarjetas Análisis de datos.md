A continuación, te presento los temas mas relevantes del ppt 1
### 1. **Hipótesis del Aprendizaje Automático**

- **Conceptos de experiencia, tarea y medida de eficiencia en el aprendizaje automático**: Según el PPT, la hipótesis del aprendizaje automático se basa en la idea de que un programa aprende de una _experiencia_ para mejorar en una _tarea_ específica, con una _medida de eficiencia_ que evalúa su rendimiento. Por ejemplo, si se está entrenando un modelo para clasificar imágenes, la experiencia puede consistir en la exposición a diferentes imágenes etiquetadas, la tarea sería la clasificación de esas imágenes, y la medida de eficiencia podría ser la precisión del modelo al clasificar nuevas imágenes.
    - **Ejemplo**: Supongamos un programa que aprende a identificar si una imagen contiene un gato o no. La experiencia es el conjunto de imágenes etiquetadas como "gato" o "no gato", la tarea es la clasificación de nuevas imágenes y la medida de eficiencia es el porcentaje de imágenes correctamente clasificadas.

### 2. **Problema Sesgo vs. Varianza**

- **Explicación del problema de sesgo y varianza en modelos de aprendizaje**: El problema del _sesgo_ se refiere a cuando un modelo es demasiado simple para capturar las complejidades de los datos, resultando en un bajo rendimiento tanto en el conjunto de entrenamiento como en los nuevos datos (subajuste). Por otro lado, el problema de la _varianza_ surge cuando un modelo es demasiado complejo, lo que lo lleva a ajustar demasiado los datos de entrenamiento y a fallar al generalizar en nuevos datos (sobreajuste).
    - **Ejemplo**: Un modelo lineal simple que intenta predecir las ventas de un producto basado en una sola variable (como la publicidad) puede tener un sesgo alto, ya que no captura todas las influencias en las ventas. Un modelo que incluye muchas variables innecesarias puede tener alta varianza y no generalizar bien para nuevos datos.

### 3. **Ajuste de Complejidad**

- **Métodos para ajustar la complejidad de un modelo de aprendizaje**: En el PPT, se describe que uno de los métodos principales para ajustar la complejidad es dividir los datos en conjuntos de _entrenamiento_, _validación_ y _prueba_. El conjunto de entrenamiento se utiliza para ajustar el modelo, mientras que el conjunto de validación ayuda a seleccionar la complejidad del modelo (elegir el número de parámetros, por ejemplo) para evitar el sobreajuste. El conjunto de prueba se usa finalmente para evaluar el modelo.
    - **Ejemplo**: En un modelo de regresión, se puede ajustar la complejidad seleccionando el grado del polinomio que mejor ajusta los datos en el conjunto de validación sin causar sobreajuste.

### 4. **Validación Cruzada**

- **Definición y explicación de la validación cruzada en modelos de aprendizaje automático**: La _validación cruzada_ es una técnica que permite evaluar el rendimiento de un modelo dividiendo los datos en varios subconjuntos o "pliegues". En cada iteración, un pliegue se utiliza como conjunto de prueba mientras que los otros se usan para entrenar el modelo. Este proceso se repite varias veces, promediando los resultados de las pruebas para obtener una evaluación robusta del modelo.
    - **Ejemplo**: En una validación cruzada con 5 pliegues, los datos se dividen en 5 subconjuntos. Se entrena el modelo en 4 subconjuntos y se prueba en el quinto, repitiendo el proceso para cada pliegue. Al final, se promedia el error de los 5 pliegues para obtener una estimación general del rendimiento del modelo.

### 5. **Proceso de Regularización**

- **Métodos para evitar el sobreajuste usando regularización**: En el PPT, se menciona que la _regularización_ introduce un término adicional en la función de error del modelo que penaliza la complejidad excesiva. Los métodos más comunes incluyen la regularización L1 (Lasso) y L2 (Ridge). Al aumentar el término de regularización, se reduce la tendencia del modelo a ajustar en exceso los datos de entrenamiento, favoreciendo soluciones más simples.
    - **Ejemplo**: En una regresión lineal, la regularización L2 penaliza los valores grandes de los coeficientes del modelo, lo que reduce la complejidad del modelo al disminuir el peso de algunas características menos importantes.

### 6. **Navaja de Occam y Longitud de Descripción Mínima**

- **Explicación del principio de parsimonia y la longitud de descripción mínima en la elección de modelos**: El _principio de parsimonia_ (o Navaja de Occam) sugiere que, entre varios modelos que explican los datos, se debe preferir el más simple que tenga el menor número de supuestos. La _longitud de descripción mínima_ (MDL) es una formalización de este principio, en el que el modelo seleccionado es aquel que minimiza la suma de la longitud de la descripción del modelo y los datos dados el modelo.
    - **Ejemplo**: Si tenemos dos modelos que predicen el precio de una casa basado en su tamaño, uno con 3 características y otro con 10, según la Navaja de Occam, preferiríamos el modelo con 3 características si ambos tienen un rendimiento similar.

### 7. **1.4 Bases de Datos Analíticas (Data Warehouse)**

- **Descripción de las bases de datos analíticas y su uso en la toma de decisiones estratégicas**: Las _bases de datos analíticas_ o _Data Warehouses_ están diseñadas específicamente para el análisis y la toma de decisiones, en lugar de operaciones cotidianas. Se construyen a partir de datos operacionales que se integran y transforman para facilitar su análisis mediante consultas complejas y reportes.
    - **Ejemplo**: Un Data Warehouse puede integrar datos de ventas, marketing y finanzas de una empresa para ayudar a los gerentes a analizar el rendimiento empresarial y tomar decisiones estratégicas.

### 8. **Diseño de un Data Warehouse**

- **Aspectos clave del diseño de un Data Warehouse para soportar análisis de datos**: El diseño de un Data Warehouse requiere considerar la integración de datos de múltiples fuentes, la creación de esquemas que permitan consultas eficientes y la implementación de procesos ETL (extracción, transformación y carga) para consolidar y transformar los datos antes de cargarlos en el sistema.
    - **Ejemplo**: Al diseñar un Data Warehouse para una cadena de supermercados, se deben integrar los datos de todas las tiendas y proveedores en un esquema de estrella o copo de nieve, para facilitar el análisis de ventas por categoría de producto, ubicación y tiempo.

### 9. **Hipercubo en Data Warehousing**

- **Ejemplo de estructuras de almacenamiento multidimensionales (hipercubo)**: Los _hipercubos_ son estructuras de almacenamiento que permiten representar datos en múltiples dimensiones, facilitando el análisis de grandes volúmenes de información a través de consultas OLAP (procesamiento analítico en línea). Un hipercubo permite analizar datos en función de varias dimensiones, como el tiempo, el producto, y la ubicación.
    - **Ejemplo**: Un hipercubo en una cadena de retail podría permitir analizar las ventas de un producto específico (como CDs) en distintas tiendas, en diferentes meses y con diversas cantidades vendidas.


----

A continuación, te presento los diferentes tipos de esquemas utilizados en el diseño de un **Data Warehouse**, como el esquema de estrella y el esquema de copo de nieve, junto con su propósito, uso y ejemplos.

### 1. **Esquema de Estrella (Star Schema)**

Fact Table : datos principales
Dimension table : detalles 

- **¿Para qué sirve?**: Es el esquema más simple y común en un Data Warehouse. Sirve para organizar los datos en una estructura que permite realizar consultas rápidas y eficientes.
- **¿Cómo se usa?**: En este esquema, los datos están organizados alrededor de una tabla de hechos (fact table) que contiene los datos principales, como transacciones o ventas, y varias tablas de dimensiones (dimension tables) que proporcionan detalles contextuales, como tiempo, productos, o ubicaciones. Las tablas de dimensiones están conectadas directamente a la tabla de hechos.
- **Ejemplo**: Un sistema de ventas puede tener una tabla de hechos que registre cada transacción (fact table), y tablas de dimensiones que contengan detalles sobre los productos vendidos, las fechas de las transacciones y las ubicaciones de las tiendas (dimension tables). Esto facilita realizar análisis rápidos, como ventas totales por región y por temporada.

Imagina que tienes una tienda en línea que vende productos electrónicos. Quieres analizar las ventas de tu tienda.

- **Tabla de Hechos (Fact Table)**: Contiene los datos principales sobre las **ventas**, como la cantidad de productos vendidos, el monto total de la venta, y el identificador del producto vendido.
- **Tablas de Dimensiones (Dimension Tables)**: Proporcionan detalles adicionales, como:
    - **Dimensión de Producto**: Contiene detalles como el nombre del producto, su categoría (teléfonos, laptops, etc.), y su precio.
    - **Dimensión de Fecha**: Contiene información sobre la fecha de la venta (día, mes, año).
    - **Dimensión de Cliente**: Contiene información sobre el cliente (nombre, dirección, edad).
    - **Dimensión de Tienda**: Contiene detalles sobre la tienda desde donde se envió el producto.

Este diseño en estrella facilita hacer preguntas como: ¿Cuántos teléfonos vendimos en marzo? ¿Qué tiendas vendieron más laptops?


### 2. **Esquema de Copo de Nieve (Snowflake Schema)**

Tabla de dimensiones -> subtabla -> subsubtabla y asi
para poder realizar consultas mas complejas

- **¿Para qué sirve?**: Sirve para normalizar las tablas de dimensiones, dividiendo las dimensiones en tablas más pequeñas y detalladas, lo que reduce la redundancia de datos.
- **¿Cómo se usa?**: A diferencia del esquema de estrella, en el esquema de copo de nieve las tablas de dimensiones están normalizadas, es decir, las dimensiones están divididas en subtablas. Esto puede reducir el espacio de almacenamiento y mejorar la organización de los datos, pero las consultas pueden ser más complejas debido a las relaciones adicionales entre tablas.
- **Ejemplo**: En lugar de una única tabla de dimensión para los productos, el esquema de copo de nieve tendría una tabla para productos y otras subtablas para categorías de productos y proveedores. Esto hace que los datos estén más organizados y estructurados, aunque las consultas se vuelven más complicadas debido a las múltiples relaciones entre tablas.

### 3. **Esquema de Constelación de Factos (Fact Constellation Schema)**

- **¿Para qué sirve?**: Este esquema permite manejar múltiples tablas de hechos que comparten dimensiones comunes, creando una "constelación" de tablas de hechos interrelacionadas.
- **¿Cómo se usa?**: Es útil en situaciones donde se necesitan analizar diferentes procesos de negocio que comparten dimensiones comunes. Cada proceso de negocio tiene su propia tabla de hechos, pero estas tablas comparten varias tablas de dimensiones.
- **Ejemplo**: Un Data Warehouse para una empresa minorista podría tener una tabla de hechos para las ventas y otra tabla de hechos para los envíos. Ambas tablas pueden compartir dimensiones como tiempo, producto y ubicación, permitiendo realizar análisis integrados entre ventas y envíos.

### 4. **Esquema Galaxia (Galaxy Schema)**

- **¿Para qué sirve?**: También conocido como "esquema de constelación", es una extensión del esquema de estrella o copo de nieve, en la que varias tablas de hechos están relacionadas con múltiples dimensiones.
- **¿Cómo se usa?**: Se usa cuando se manejan varios sistemas de informes complejos. Este esquema combina varias estrellas o copos de nieve para formar una estructura más grande que abarca diferentes áreas del negocio.
- **Ejemplo**: En un conglomerado con diferentes líneas de negocio, el esquema galaxia puede incluir tablas de hechos para ventas, inventario, y marketing, todas compartiendo dimensiones comunes como tiempo, ubicación y productos.

### 5. **Esquema de Panel de Control (Dashboard Schema)**

- **¿Para qué sirve?**: Este tipo de esquema está diseñado para facilitar la integración de datos en tiempo real o casi en tiempo real con interfaces visuales, como paneles de control (dashboards).
- **¿Cómo se usa?**: Los datos se estructuran de manera que se puedan consultar y procesar rápidamente para generar gráficos y métricas clave en un entorno de monitoreo o toma de decisiones rápidas.
- **Ejemplo**: En una empresa de tecnología, el esquema de panel de control podría organizar datos sobre rendimiento del sistema, tickets de soporte y métricas financieras en tiempo real, para que los gerentes puedan monitorear las operaciones en un solo lugar.

### Comparación de Esquemas:

- **Esquema de Estrella**: Simple y rápido, pero puede ser menos eficiente en términos de almacenamiento.
- **Esquema de Copo de Nieve**: Más eficiente en almacenamiento, pero más complejo para consultas.
- **Esquema de Constelación de Factos/Galaxia**: Ideal para múltiples procesos de negocio, pero muy complejo.
- **Esquema de Panel de Control**: Optimizado para consultas rápidas y visualización en tiempo real, pero más especializado.