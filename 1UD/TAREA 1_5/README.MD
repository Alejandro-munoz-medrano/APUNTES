# Ventajas e inconvenientes entre lenguajes interpretados, compilados y virtuales

## Lenguajes interpretados
Son aquellos cuyos programas se ejecutan mediante un **intérprete** que traduce el código fuente a lenguaje máquina **en tiempo de ejecución**.

### Ventajas:
- **Portabilidad**: Pueden ejecutarse en múltiples plataformas sin modificación.
- **Desarrollo rápido**: No es necesario compilar el código para ejecutarlo, lo que permite hacer pruebas y ver resultados de inmediato.
- **Facilidad para depuración**: Se ejecuta línea por línea, facilitando la detección de errores.

### Inconvenientes:
- **Rendimiento más bajo**: Suelen ser más lentos que los lenguajes compilados.
- **Mayor consumo de recursos**: El intérprete consume más memoria y CPU durante la ejecución.

**Ejemplos**: Python, JavaScript, Ruby.

---

## Lenguajes compilados
Son aquellos cuyos programas se traducen directamente a código máquina mediante un **compilador**, generando un archivo ejecutable.

### Ventajas:
- **Mayor rendimiento**: El código compilado está optimizado para el hardware.
- **Protección del código**: No se distribuye el código fuente, sino el binario.
- **Menor consumo de recursos en ejecución**: No necesita un intérprete en tiempo de ejecución.

### Inconvenientes:
- **Menos flexible**: Si hay un error, se debe recompilar el programa.
- **Desarrollo más lento**: Requiere recompilar tras cada cambio importante.

**Ejemplos**: C, C++, Rust.

---

## Lenguajes virtuales (bytecode)
El código fuente se compila a un **bytecode intermedio**, que luego es ejecutado por una máquina virtual (VM).

### Ventajas:
- **Portabilidad**: El bytecode puede ejecutarse en cualquier sistema que tenga la máquina virtual.
- **Equilibrio entre rendimiento y flexibilidad**: Más eficiente que la interpretación directa, pero más flexible que la compilación a código máquina.
- **Optimización Just-in-Time (JIT)**: Las máquinas virtuales pueden realizar optimizaciones en tiempo de ejecución.

### Inconvenientes:
- **Rendimiento menor que los lenguajes compilados**: Aunque más rápidos que los interpretados, son más lentos que los compilados.
- **Dependencia de la máquina virtual**: Requieren instalar una VM en cada plataforma.

**Ejemplos**: Java, C#, Kotlin.

---

# Utilidad de un depurador (debugger)

Un **depurador** es una herramienta que permite **inspeccionar y controlar** la ejecución de un programa para detectar y corregir errores. Su utilidad incluye:

- **Ejecución paso a paso**: Permite avanzar línea a línea y observar el comportamiento del código.
- **Inspección de variables**: Permite ver los valores de las variables durante la ejecución.
- **Modificación de valores en tiempo real**: Permite cambiar valores para ver cómo afecta al programa.
- **Control del flujo de ejecución**: El desarrollador puede avanzar, retroceder o saltar a partes del código.
- **Detección de errores**: Identifica problemas como desbordamientos de memoria o punteros nulos.

---

# Punto de ruptura (breakpoint) en un depurador

Un **punto de ruptura** es una herramienta que se coloca en una línea específica del código donde se desea que la ejecución del programa se detenga temporalmente durante la depuración.

### Qué es:
Es una instrucción que indica al depurador que pause la ejecución del programa al llegar a esa línea.

### Qué permite hacer:
- **Inspeccionar el estado del programa**: Detiene la ejecución en un punto crítico para revisar variables y la lógica del programa.
- **Controlar el flujo de ejecución**: Permite avanzar paso a paso desde el punto de ruptura o saltar a otras partes del código.
- **Identificar problemas específicos**: Facilita la observación del comportamiento exacto de una función o bloque de código.

