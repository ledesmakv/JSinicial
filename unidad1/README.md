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
    variable se declara con la palabra reservada var seguida del nombre de la variable.<br /><br />
    _Ejemplo:_<br />
    **var** nombreDeLaVariable<br />

-   La declaración de una variable solo se debe realizar una vez. Luego de declararla se trabaja con con esa
    variable sin la palabra var.<br />

-   Para asignar un valor a la variable se utiliza el operador de asignación **=** (igual). La variable debe ir del
    lado izquierdo del operador y el valor debe ir del lado derecho del operador.<br /><br />
    _Ejemplo:_<br />
    **var** unValor<br />
    unValor = 1<br />

-   La primera vez que se le asigna un valor a una variable se la está inicializando (se le está danto el valor
    inicial). Esto puede ocurrir a la hora de declararla o durante el desarrollo del programa.<br /><br />
    _Ejemplo:_<br />
    **var** unValor<br />
    **var** otroValor = 1 ---------------------------- (se inicializa la variable al declararla)<br />
    unValor = 2 -------------------------------------- (se inicializa la variable luego de declararla)<br />
    otroValor = 3 ------------------------------------ (se asigna un nuevo valor a una variable ya inicializada)<br />

-   El JavaScript el nombre de la variable solo puede estar formado por letras del alfabeto inglés, números, el
    guión bajo (_) o el símbolo pesos (\$). No puede tener espacios en blanco. El primer caracter no puede ser un número.<br /><br />
     _Ejemplo:_ 
        <br />
         miVariable ---------------------------- (nombre válido) <br />
        _unaVariable1 -------------------------- (nombre válido)<br />
        otra\$variable ------------------------- (nombre válido)<br />
        1variable ------------------------------ (nombre inválido)<br />
        la variable ---------------------------- (nombre inválido)<br />

-   JavaScript es un lenguaje sensible a caracteres en minúscula y mayúscula (**case sensitive**), por lo que la
    variación influye en los nombres de las variables.<br /><br />
    _Ejemplo:_<br />
    **miVariable** es distinto a **MiVariable**<br />
    **OtraVariable** es distinto a **otraVariable**<br />

-   Existe un conjunto de palabras que no se pueden utilizar como nombre de variables ya que para
    JavaScript tienen un significado o función establecida. Esta lista de palabras se conoce como **palabras reservadas** y su utilización como nombre de variable pueden generar errores en el código.<br />
    _Las palabras resevadas son:_<br />
    break, case, catch, continue, default, delete, do, else, finally, for, function, if, in, instanceof, new, return, switch, this, throw, try, typeof, var, void, while, with, abstract, boolean, byte, char, class, const, debugger, double, enum, export, extends, final, float, goto, implements, import, int, interface, long, native, package, private, protected, public, short, static, super, synchronized, throws, transient, volatile.<br /><br />
    _Ejemplo:_<br />
    var **var** --------------------------- (nombre de variable inválido)<br />
    var **do** ---------------------------- (nombre de variable inválido)<br />
    var **var**iable ---------------------- (nombre de variable válido)<br />
    var **do**nde ------------------------- (nombre de variable válido)<br /><br />
    * Si bien no es obligatorio, conviene que el nombre de la variable tenga una relación con su contenido. Es decir, si vamos a guardar un nombre, nuestra variable podría llamarse nombre o unNombre, por ejemplo. Esto servirá para cuando se lea el código del programa sea más fácil de entender su funcionamiento.<br />
    * Finalmente, en programación se puede utilizar una forma de escritura llamada notación camello, llamada así porque parecen las jorobas de un camello. En esta notación los nombres de cada palabra empiezan con mayúscula y el resto se escribe con minúsculas (salvo la primer paralabra). No se usan puntos ni guiones para separar las palabras.<br /><br />
    _Ejemplo:_<br />
    **mivariable** podría escribirse como **miVariable**<br />
    **una_variable** podría escribirse como **unaVariable**<br />

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
    ser positivos o negativos.<br /><br />
    _Ejemplo:_<br />
    12579<br />
    -135<br />
    105<br />
    -9876<br />
    14<br />
    -2<br />

-   Enteros octales (base 8): secuencia de dígitos de 0 a 7. Para identificarlos se les coloca un 0 (cero) por
    delante. Pueden ser positivos o negativos. <br /> <br />
    _Ejemplo:_<br />
    0777<br />
    -0642<br />
    0105<br />
    -0531<br />
    0111<br />
    -0246<br />

-   Enteros hexadecimales (base 16): secuencia de dígitos de 0 a 9 y las letras A a F. Para identificarlos se les coloca un 0x (cero x) por delante. Pueden ser positivos o negativos.<br /><br />
    _Ejemplo:_<br />
    0xFA59<br />
    -0xA6B8<br />
    0x105<br />
    -0xCE64D2<br />
    0xFEDCBA<br />
    -0x123456<br />

*   Punto flotante (decimales): secuencia de dígitos de 0 a 9 con la utilización del . (punto) para separar los enteros de los decimales o la letra e para los exponentes. Pueden ser positivos o negativos.<br /><br />
    _Ejemplo:_<br />
    3.1416<br />
    -1.2345<br />
    3e6<br />
    -4e2<br />
    105e-20<br />
    -16e-14<br />

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
    inapropiados, como cadenas o con el valor no definido.<br /><br />
    _valor:_<br />
    NaN<br />

-   Infinito (Infinity): se utiliza cuando un número es demasiado grande para representarlo. Pueden ser
    positivos o negativos.<br /><br />
    _valor:_<br />
    Infinity<br />
    -Infinity<br />

### Cadenas (string)

Un valor de cadena está formado por una cadena de cero o más caracteres (letras, dígitos y signos de puntuación). El tipo de datos string se usa para representar texto. Para identificarlos se los encierra entre pares de comillas simples (') o dobles ("). Pueden incluirse comillas dobles en cadenas delimitadas por comillas simples y viceversa.
Las cadenas que no contienen ningún carácter ("") se denominan cadenas vacías (de longitud cero).
Además JavaScript proporciona secuencias de escape que se pueden incluir en cadenas para crear caracteres que no es posible escribir directamente.<br /><br />
_Ejemplos:_<br />
"Hola mundo, esto es una cadena"<br />
'¡Esto es otra cadena!'<br />
"Esto es una 'cadena'"<br />
'¿Esto es otra "cadena"?'<br />
"753"<br />
'-468'<br />
"d"<br />
'n'<br />

### Lógicos (boolean)

Los tipos de datos booleanos solamente pueden tener dos valores, verdadero o falso.<br /><br />

_valores:_<br />
