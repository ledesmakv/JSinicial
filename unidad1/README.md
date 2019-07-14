# Unidad 1

## Declaración de variables y operador de asignación

### Variables

Es una estructura de datos que puede cambiar de valor a lo largo de la ejecución de un programa. Corresponde a un área reservada de la memoria principal de la CPU.
La variable está asociada a algún tipo de dato en base al cuál se determinará la cantidad de bytes a utilizar para almacenar su valor.
En programación, son las palabras mediante las cuales se hará referencia a una determinada información dentro del programa, ya que en muchas ocaciones no se va a tener el contenido a manipular de antemano, sino que el mismo se generará o se solicitará en un momento determinado.
De esta forma, las variables permiten a los programadores abstraerse del valor de la información y aún así poder manipularla con total seguridad.
Algunas consideraciones a tener en cuenta:<br />
<br />
-   La variable se debe declarar (reservar un espacio en la memoria RAM de la CPU). En JavaScript una
    variable se declara con la palabra reservada var seguida del nombre de la variable.<br />
    _Ejemplo:_<br />
    **var** nombreDeLaVariable<br />
<br />
-   La declaración de una variable solo se debe realizar una vez. Luego de declararla se trabaja con con esa
    variable sin la palabra var.

-   Para asignar un valor a la variable se utiliza el operador de asignación **=** (igual). La variable debe ir del
    lado izquierdo del operador y el valor debe ir del lado derecho del operador.
    _Ejemplo:_
    **var** unValor
    unValor = 1

-   La primera vez que se le asigna un valor a una variable se la está inicializando (se le está danto el valor
    inicial). Esto puede ocurrir a la hora de declararla o durante el desarrollo del programa.
    _Ejemplo:_
    **var** unValor
    **var** otroValor = 1 (se inicializa la variable al declararla)
    unValor = 2 (se inicializa la variable luego de declararla)
    otroValor = 3 (se asigna un nuevo valor a una variable ya inicializada)

-   El JavaScript el nombre de la variable solo puede estar formado por letras del alfabeto inglés, números, el
    guión bajo (_) o el símbolo pesos (\$). No puede tener espacios en blanco. El primer caracter no puede ser un número.
    \_Ejemplo:_
    miVariable (nombre válido)
    \_unaVariable1 (nombre válido)
    otra\$variable (nombre válido)
    1variable (nombre inválido)
    la variable (nombre inválido)

-   JavaScript es un lenguaje sensible a caracteres en minúscula y mayúscula (**case sensitive**), por lo que la
    variación influye en los nombres de las variables.
    _Ejemplo:_
    **miVariable** es distinto a **MiVariable**
    **OtraVariable** es distinto a **otraVariable**

-   Existe un conjunto de palabras que no se pueden utilizar como nombre de variables ya que para
    JavaScript tienen un significado o función establecida. Esta lista de palabras se conoce como **palabras reservadas** y su utilización como nombre de variable pueden generar errores en el código.
    _Las palabras resevadas son:_
    break, case, catch, continue, default, delete, do, else, finally, for, function, if, in, instanceof, new, return, switch, this, throw, try, typeof, var, void, while, with, abstract, boolean, byte, char, class, const, debugger, double, enum, export, extends, final, float, goto, implements, import, int, interface, long, native, package, private, protected, public, short, static, super, synchronized, throws, transient, volatile.
    _Ejemplo:_
    var **var** (nombre de variable inválido)
    var **do** (nombre de variable inválido)
    var **var**iable (nombre de variable válido)
    var **do**nde (nombre de variable válido)
    ⋅⋅* Si bien no es obligatorio, conviene que el nombre de la variable tenga una relación con su contenido. Es decir, si vamos a guardar un nombre, nuestra variable podría llamarse nombre o unNombre, por ejemplo. Esto servirá para cuando se lea el código del programa sea más fácil de entender su funcionamiento.
    ⋅⋅* Finalmente, en programación se puede utilizar una forma de escritura llamada notación camello, llamada así porque parecen las jorobas de un camello. En esta notación los nombres de cada palabra empiezan con mayúscula y el resto se escribe con minúsculas (salvo la primer paralabra). No se usan puntos ni guiones para separar las palabras.
    _Ejemplo:_
    **mivariable** podría escribirse como **miVariable**
    **una_variable** podría escribirse como **unaVariable**

### Valor

Contenido de una variable sobre la que se efectuarán operaciones en un algoritmo.

### Tipo de dato

Es una restricción impuesta por el lenguaje de programación para la interpretación, manipulación y representación de datos. Indica los valores que puede tomar una variable y las operaciones que se pueden realizar con ella en un algoritmo.
En JavaScript existen los tipos de datos numéricos, de cadena, lógicos, indefinidos, nulos y objetos.

### Literal

Permite declarar valores constantes, que no pueden modificarse en el transcurso del programa.

### Expresión

Conjunto válido de literales, variables y operadores que al evaluarse dan como resultado un único valor del tipo numérico, de cadena o lógico.

## Tipos de datos

**Numéricos (number)**
Se dividen en las siguientes categorías:

-   Enteros decimales (base 10): secuencia de dígitos de 0 a 9. No deben comenzar con 0 (cero). Pueden
    ser positivos o negativos.
    _Ejemplo:_
    12579
    -135
    105
    -9876
    14
    -2

-   Enteros octales (base 8): secuencia de dígitos de 0 a 7. Para identificarlos se les coloca un 0 (cero) por
    delante. Pueden ser positivos o negativos.  
     _Ejemplo:_
    0777
    -0642
    0105
    -0531
    0111
    -0246

-   Enteros hexadecimales (base 16): secuencia de dígitos de 0 a 9 y las letras A a F. Para identificarlos se les coloca un 0x (cero x) por delante. Pueden ser positivos o negativos.
    _Ejemplo:_
    0xFA59
    -0xA6B8
    0x105
    -0xCE64D2
    0xFEDCBA
    -0x123456

*   Punto flotante (decimales): secuencia de dígitos de 0 a 9 con la utilización del . (punto) para separar los enteros de los decimales o la letra e para los exponentes. Pueden ser positivos o negativos.
    _Ejemplo:_
    3.1416
    -1.2345
    3e6
    -4e2
    105e-20
    -16e-14

Tabla de comparación de las distintas bases de tipos de datos numéricos:

| Decimal (base 10) | Octal (base 8) | Hexadecimal (base 16) | Binario (base 2) |
| ----------------- | -------------- | --------------------- | ---------------- |
| 0                 | 0              | 0                     | 0                |
| 1                 | 01             | 0x1                   | 1                |
| 2                 | 02             | 0x2                   | 10               |
| 3                 | 03             | 0x3                   | 11               |
| 4                 | 04             | 0x4                   | 100              |
| 5                 | 05             | 0x5                   | 101              |
| 6                 | 06             | 0x6                   | 110              |
| 7                 | 07             | 0x7                   | 111              |
| 8                 | 010            | 0x8                   | 1000             |
| 9                 | 011            | 0x9                   | 1001             |
| 10                | 012            | 0xA                   | 1010             |
| 11                | 013            | 0xB                   | 1011             |
| 12                | 014            | 0xC                   | 1100             |
| 13                | 015            | 0xD                   | 1101             |
| 14                | 016            | 0xE                   | 1110             |
| 15                | 017            | 0xF                   | 1111             |
| 16                | 020            | 0x10                  | 10000            |

Además, JavaScript contiene números con valores especiales. Estos son:

-   No es un número (**NaN, Not a Number**): se utiliza al realizar una operación matemática en datos
    inapropiados, como cadenas o con el valor no definido.
    _valor:_
    NaN

-   Infinito (Infinity): se utiliza cuando un número es demasiado grande para representarlo. Pueden ser
    positivos o negativos.
    _valor:_
    Infinity
    -Infinity

### Cadenas (string)

Un valor de cadena está formado por una cadena de cero o más caracteres (letras, dígitos y signos de puntuación). El tipo de datos string se usa para representar texto. Para identificarlos se los encierra entre pares de comillas simples (') o dobles ("). Pueden incluirse comillas dobles en cadenas delimitadas por comillas simples y viceversa.
Las cadenas que no contienen ningún carácter ("") se denominan cadenas vacías (de longitud cero).
Además JavaScript proporciona secuencias de escape que se pueden incluir en cadenas para crear caracteres que no es posible escribir directamente.

    _Ejemplos:_
    "Hola mundo, esto es una cadena"
    '¡Esto es otra cadena!'
    "Esto es una 'cadena'"
    '¿Esto es otra "cadena"?'
    "753"
    '-468'
    "d"
    'n'

### Lógicos (boolean)

Los tipos de datos booleanos solamente pueden tener dos valores, verdadero o falso.

_valores:_
