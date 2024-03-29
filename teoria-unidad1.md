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
    \_Ejemplo:_
    <br />
    miVariable ---------------------------- (nombre válido) <br />
    \_unaVariable1 -------------------------- (nombre válido)<br />
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
    -   Si bien no es obligatorio, conviene que el nombre de la variable tenga una relación con su contenido. Es decir, si vamos a guardar un nombre, nuestra variable podría llamarse nombre o unNombre, por ejemplo. Esto servirá para cuando se lea el código del programa sea más fácil de entender su funcionamiento.<br />
    -   Finalmente, en programación se puede utilizar una forma de escritura llamada notación camello, llamada así porque parecen las jorobas de un camello. En esta notación los nombres de cada palabra empiezan con mayúscula y el resto se escribe con minúsculas (salvo la primer paralabra). No se usan puntos ni guiones para separar las palabras.<br /><br />
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
    ser positivos o negativos.<br />
    _Ejemplo:_<br />
    12579<br />
    -135<br />
    105<br />
    -9876<br />
    14<br />
    -2<br />

-   Enteros octales (base 8): secuencia de dígitos de 0 a 7. Para identificarlos se les coloca un 0 (cero) por
    delante. Pueden ser positivos o negativos. <br />
    _Ejemplo:_<br />
    0777<br />
    -0642<br />
    0105<br />
    -0531<br />
    0111<br />
    -0246<br />

-   Enteros hexadecimales (base 16): secuencia de dígitos de 0 a 9 y las letras A a F. Para identificarlos se les coloca un 0x (cero x) por delante. Pueden ser positivos o negativos.<br />
    _Ejemplo:_<br />
    0xFA59<br />
    -0xA6B8<br />
    0x105<br />
    -0xCE64D2<br />
    0xFEDCBA<br />
    -0x123456<br />

*   Punto flotante (decimales): secuencia de dígitos de 0 a 9 con la utilización del . (punto) para separar los enteros de los decimales o la letra e para los exponentes. Pueden ser positivos o negativos.<br />
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
    inapropiados, como cadenas o con el valor no definido.<br />
    _valor:_<br />
    NaN<br />

-   Infinito (Infinity): se utiliza cuando un número es demasiado grande para representarlo. Pueden ser
    positivos o negativos.<br />
    _valor:_<br />
    Infinity<br />
    -Infinity<br />

### Cadenas (string)

Un valor de cadena está formado por una cadena de cero o más caracteres (letras, dígitos y signos de puntuación). El tipo de datos string se usa para representar texto. Para identificarlos se los encierra entre pares de comillas simples (') o dobles ("). Pueden incluirse comillas dobles en cadenas delimitadas por comillas simples y viceversa.
Las cadenas que no contienen ningún carácter ("") se denominan cadenas vacías (de longitud cero).
Además JavaScript proporciona secuencias de escape que se pueden incluir en cadenas para crear caracteres que no es posible escribir directamente.<br />
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

Los tipos de datos booleanos solamente pueden tener dos valores, verdadero o falso.<br />

_valores:_<br />
true <br />
false <br />

JavaScript usa las siguientes reglas para convertir valores que no son de tipo boolean en valores de tipo boolean:<br />

-   Todos los **objetos** se consideran **true**.
-   Las **cadenas** se consideran **false** si y solo si están **vacías**.
-   **undefined** y **null** se consideran **false**.
-   Los **números** se consideran **false** si y solo si son **cero**.

### Indefinido (undefined)

Se obtiene el valor undefined cuando se usa una propiedad de objeto que no existe o una variable que se ha declarado, pero nunca ha tenido un valor asignado.<br />
_valor:_<br />
undefined<br />

### Nulo (null)

Una variable que contiene **null** no contiene ningún número, cadena, valor booleano u objeto. Para borrar el contenido de una variable (sin eliminar la variable), se le asigna el valor null.
En JavaScript, null no es lo mismo que 0.<br />
_valor:_<br />
null<br />

### Objetos (object)

Los objetos de JavaScript son colecciones de propiedades y métodos.
Un método es una función que es miembro de un objeto.
Una propiedad es un valor o un conjunto de valores (en forma de matriz u objeto) que es miembro de un objeto.

## Operadores

#### Aritméticos:

Se utilizan para realizar operaciones aritméticas. Devuelve un número.<br />
Pueden ser:<br />

-   **suma:** el operador es **+**<br />
    _ejemplos:_<br />
    var **suma** = 2 **+** 4 ------------------- (el valor obtenido será **6**)<br />
    var **otraSuma** = 7 **+** 3 --------------- (el valor obtenido será **10**)<br />
    var **miSuma** = 0 **+** 6 ----------------- (el valor obtenido será **6**)<br />
    var **miOtraSuma** = 5 **+** 0 ------------- (el valor obtenido será **5**)<br /><br />

-   **resta:** el operador es **-**<br />
    _ejemplos:_<br />
    var **resta** = 2 **-** 4 ----------------------- (el valor obtenido será **-2**)<br />
    var **otraResta** = 7 **-** 3 ------------------- (el valor obtenido será **4**)<br />
    var **miResta** = 0 **-** 6 --------------------- (el valor obtenido será **-6**)<br />
    var **miOtraResta** = 5 **-** 0 ----------------- (el valor obtenido será **5**)<br /><br />

-   **multiplicación:** el operador es **\***<br />
    _ejemplos:_<br />
    var **multiplicacion** = 2 **\*** 4 ---------------- (el valor obtenido será **8**)<br />
    var **otraMultiplicacion** = 7 **\*** 3 ------------ (el valor obtenido será **21**)<br />
    var **miMultiplicacion** = 0 **\*** 6 -------------- (el valor obtenido será **0**)<br />
    var **miOtraMultiplicacion** = 5 **\*** 0 ---------- (el valor obtenido será **0**)<br /><br />

-   **división:** el operador es **/**<br />
    _ejemplos:_<br />
    var **division** = 2 **/** 4 ---------------- (el valor obtenido será **0.5**)<br />
    var **otraDivision** = 7 **/** 3 ------------ (el valor obtenido será **2.3333**)<br />
    var **miDivision** = 0 **/** 6 -------------- (el valor obtenido será **0**)<br />
    var **miOtraDivision** = 5 **/** 0 ---------- (el valor obtenido será **Infinity**)<br /><br />

-   **módulo:** el operador es **%**<br />
    _ejemplos:_<br />
    var **modulo** = 2 **%** 4 ---------------- (el valor obtenido será **0**, ya que el resto de 2/4 es 0)<br />
    var **otroModulo** = 7 **%** 3 ------------ (el valor obtenido será **1**, ya que el resto de 7/3 es 1)<br />
    var **miModulo** = 0 **%** 6 -------------- (el valor obtenido será **0**)<br />
    var **miOtroModulo** = 5 **%** 0 ---------- (el valor obtenido será **NaN**)<br /><br />

-   **incremento:** el operador es **++**. Incrementa en una unidad el valor de la variable.<br />
    _ejemplos:_<br />
    var **miVariable** = 3<br />
    **miVariable++** ------------ (el valor de **miVariable** ahora será **4**)<br />

-   **decremento:** el operador es **--**. Decrementa en una unidad el valor de la variable.<br />
    _ejemplos:_<br />
    var **miVariable** = 3<br />
    **miVariable--** ------------ (el valor de **miVariable** ahora será **2**)<br />

### De asignación

Se utilizan para asignar un valor o expresión a una variable. La variable se coloca a la izquierda del operador y el valor o la expresión se coloca a la derecha.
Pueden ser:<br />

-   **asignación**: el operador es =. Si escribo x = y, asigna a x el contenido de y.<br />
    _ejemplos_:<br />
    var **valorUno** = 6 ------------------------- (**valorUno** pasa a valer **6**)<br />
    var **valorDos** = 3 ------------------------- (**valorDos** pasa a valer **3**)<br />
    **valorUno = valorDos** ---------------------- (**valorUno** ahora pasará a valer **3**)<br /><br />

-   **asignación con suma**: el operador es +=. Si escribo x += y, asigna a x el contenido de x + y.<br />
    _ejemplos_:<br />
    var **valorUno** = 6 ------------------------- (**valorUno** pasa a valer **6**)<br />
    var **valorDos** = 3 ------------------------- (**valorDos** pasa a valer **3**)<br />
    **valorUno += valorDos** ---------------------- (**valorUno** ahora pasará a valer **9**)<br /><br />

-   **asignación con resta**: el operador es -=. Si escribo x -= y, asigna a x el contenido de x - y.<br />
    _ejemplos_:<br />
    var **valorUno** = 6 ------------------------- (**valorUno** pasa a valer **6**)<br />
    var **valorDos** = 3 ------------------------- (**valorDos** pasa a valer **3**)<br />
    **valorUno -= valorDos** ---------------------- (**valorUno** ahora pasará a valer **3**)<br /><br />

-   **asignación con multiplicación**: el operador es \*=. Si escribo x \*= y, asigna a x el contenido de x \* y.<br />
    _ejemplos_:<br />
    var **valorUno** = 6 ------------------------- (**valorUno** pasa a valer **6**)<br />
    var **valorDos** = 3 ------------------------- (**valorDos** pasa a valer **3**)<br />
    **valorUno \*= valorDos** ---------------------- (**valorUno** ahora pasará a valer **18**)<br /><br />

-   **asignación con división**: el operador es /=. Si escribo x /= y, asigna a x el contenido de x / y.<br />
    _ejemplos_:<br />
    var **valorUno** = 6 ------------------------- (**valorUno** pasa a valer **6**)<br />
    var **valorDos** = 3 ------------------------- (**valorDos** pasa a valer **3**)<br />
    **valorUno /= valorDos** ---------------------- (**valorUno** ahora pasará a valer **2**)<br /><br />

-   **asignación con módulo**: el operador es %=. Si escribo x %= y, asigna a x el contenido de x % y.<br />
    _ejemplos_:<br />
    var **valorUno** = 6 ------------------------- (**valorUno** pasa a valer **6**)<br />
    var **valorDos** = 3 ------------------------- (**valorDos** pasa a valer **3**)<br />
    **valorUno %= valorDos** ---------------------- (**valorUno** ahora pasará a valer **0**)<br /><br />

### De cadena

Se utilizan para unir valores del tipo cadena. Existe un solo operador de cadena:<br />

-   **Concatenación:** el operador es +.<br />
    Ejemplos:<br />
    var **cadena1** = "Hola"<br />
    var **cadena2** = "Mundo"<br />
    var **otraCadena = cadena1 + cadena2** ----------------- (**otraCadena** ahora vale **"HolaMundo"**)<br />
    **otraCadena = cadena2 + " " + cadena1** --------------- (**otraCadena** ahora pasará a valer **"Mundo Hola"**)<br /><br />
    Debe tenerse en cuenta que se utiliza el mismo operador para concatenar como para realizar sumas aritméticas,
    por lo que según el contexto el operador funcionará de diferentes maneras:<br />

    -   Si se utiliza solamente entre números, funcionará como operador de suma aritmética.<br />
        Ejemplos: <br />
        var **respuesta = 1 + 3 + 5 + 6 + 8** ---------------------- (**respuesta** valdrá **23**)<br />

    -   Si se utiliza solamente entre cadenas, funcionará como operador de concatenación.<br />
        Ejemplos: <br />
        var **respuesta = "1" + "3" + "5" + "6" + "8"** ---------------------- (**respuesta** valdrá **"13568"**)<br />

    -   Si se utiliza entre números y cadenas, funcionará como operador de suma y de concatenación.<br />
        Ejemplos: <br />
        var **respuesta = 1 + 3 + "5" + 6 + 8** ---------------------- (**respuesta** valdrá **"4568"**)<br />
        var **otraRespuesta = 1 + "3" + 5 + "6" + 8** ---------------------- (**respuesta** valdrá **"13568"**)<br />
        **otraRespuesta = "1" + 3 + 5 + 6 + 8** ---------------------- (**respuesta** valdrá **"13568"**)<br />
        **otraRespuesta = 1 + 3 + 5 + 6 + "8"** ---------------------- (**respuesta** valdrá **"158"**)<br />

### Lógicos

Se utilizan para realizar relaciones lógicas entre expresiones. Devuelven un valor lógico true o false en base a las expresiones con las que se realicen las operaciones.<br />
Pueden ser:<br />

-   **Operador Y (AND):** el operador es &&. Devolverá true si todas las expresiones son verdaderas. Si alguna de las expresiones se evalúa como falsa, el resultado será false.<br />
    Tabla de la verdad de AND:<br />

| **Expresión 1** | **Operador** | **Expresión 2** | **Resultado** |
| --------------- | ------------ | --------------- | ------------- |
| true            | &&           | true            | true          |
| true            | &&           | false           | false         |
| false           | &&           | true            | false         |
| false           | &&           | false           | false         |

-   **Operador O (OR):** el operador es ||. Devolverá false si todas las expresiones son falsas. Si alguna de las expresiones se evalúa como verdadera, el resultado será true.<br />
    Tabla de la verdad de OR:<br />

| **Expresión 1** | **Operador** | **Expresión 2** | **Resultado** |
| --------------- | ------------ | --------------- | ------------- |
| true            | \|\|         | true            | true          |
| true            | \|\|         | false           | true          |
| false           | \|\|         | true            | true          |
| false           | \|\|         | false           | false         |

-   **Operador Negación (NOT):** el operador es ! y se coloca delante de la expresión a operar. Devolverá el valor lógico opuesto a la expresión a la que se aplica.<br />
    Tabla de la verdad de NOT:<br />

| **Expresión 1** | **Operación de la expresión** | **Resultado** |
| --------------- | ----------------------------- | ------------- |
| true            | !true                         | false         |
| false           | !false                        | true          |

### De comparación

Se utilizan para realizar comparaciones lógicas entre expresiones. Devuelven un valor lógico true o false en base a las expresiones con las que se realicen las operaciones.<br />
Pueden ser:<br />

-   **Igualdad**: el operador es ==. Si ambas expresiones tienen el mismo valor, el resultado será true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = "2"<br />
    var **resultado**
    **resultado = valorUno == valorDos** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno == valorTres** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno == valorCuatro** ---------------------- (**resultado** será **true**)<br /><br />

-   **Igualdad estricta**: el operador es ===. Si ambas expresiones tienen el mismo valor y tipo de dato, el resultado será true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = "2"<br />
    var **resultado**
    **resultado = valorUno === valorDos** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno === valorTres** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno === valorCuatro** ---------------------- (**resultado** será **false**)<br /><br />

-   **Desigualdad**: el operador es !=. Si ambas expresiones tienen distinto valor, el resultado será true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = "2"<br />
    var **resultado**
    **resultado = valorUno != valorDos** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno != valorTres** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno != valorCuatro** ---------------------- (**resultado** será **false**)<br /><br />

-   **Desigualdad estricta**: el operador es !==. Si ambas expresiones tienen distinto valor y tipo de dato, el
    resultado será true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = "2"<br />
    var **resultado**
    **resultado = valorUno !== valorDos** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno !== valorTres** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno !== valorCuatro** ---------------------- (**resultado** será **true**)<br /><br />

-   **Mayor**: el operador es >. Si la expresión de la izquierda es mayor que la de la derecha, el resultado será
    true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = 1<br />
    var **resultado**
    **resultado = valorUno > valorDos** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno > valorTres** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno > valorCuatro** ---------------------- (**resultado** será **true**)<br /><br />

-   **Mayor o igual**: el operador es >=. Si la expresión de la izquierda es mayor o igual que la de la derecha, el
    resultado será true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = 1<br />
    var **resultado**
    **resultado = valorUno >= valorDos** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno >= valorTres** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno >= valorCuatro** ---------------------- (**resultado** será **true**)<br /><br />

-   **Menor**: el operador es <. Si la expresión de la izquierda es menor que la de la derecha, el resultado será
    true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = 1<br />
    var **resultado**
    **resultado = valorUno \< valorDos** ------------------------- (**resultado** será **false**)<br />
    **resultado = valorUno \< valorTres** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno \< valorCuatro** ---------------------- (**resultado** será **false**)<br /><br />

-   **Menor o igual**: el operador es <=. Si la expresión de la izquierda es menor o igual que la de la derecha, el resultado será true, de lo contrario false.<br />
    _ejemplos_:<br />
    var **valorUno** = 2<br />
    var **valorDos** = 2<br />
    var **valorTres** = 4<br />
    var **valorCuatro** = 1<br />
    var **resultado**
    **resultado = valorUno \<= valorDos** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno \<= valorTres** ------------------------- (**resultado** será **true**)<br />
    **resultado = valorUno \<= valorCuatro** ---------------------- (**resultado** será **false**)<br /><br />

### Precedencia de operadores:

El intérprete tiene prioridades para ir evaluando operadores a la hora de ejecutarse una expresión. El orden es el siguiente:<br /><br />

1. Agrupaciones: ( ) ---- (para agrupaciones dentro de agrupaciones siempre se utilizarán paréntesis)
2. Negación, Incremento, Decremento: ! ++ --
3. Multiplicación, División, Módulos: \* / %
4. Suma, Resta: + -
5. Relaciones lógicas: > >= < <=
6. Igualdad, Desigualdad: == === != !==
7. Operador AND: &&
8. Operador OR: ||
9. Condicional: ?:
10. Asignación: =
    <br /><br />
    _Ejemplo:_<br />

```javascript
var r = (4 % 2) + 3 - (2 + 6 / 2) > (6 % 3) + (5 % 2) == ((6 % 2) + 3 * 2 >= 1 + 2 && 5 * 2 - (7 % 3) + 1 < 4 - 2);
```

_Detectamos dos grandes agrupaciones, y una más pequeña. También vemos que no existen operadores de negación, incremento ni decremento. Comenzamos resolviendo la agrupación pequeña, primero la división y luego la suma._

```javascript
r = (4 % 2) + 3 - 5 > (6 % 3) + (5 % 2) == ((6 % 2) + 3 * 2 >= 1 + 2 && 5 * 2 - (7 % 3) + 1 < 4 - 2);
```

_Luego, resolvemos las multiplicaciones, divisiones y módulos._

```javascript
r = 0 + 3 - 5 > 0 + 1 == (0 + 6 >= 1 + 2 && 10 - 1 + 1 < 4 - 2);
```

_Ahora procedemos a resolver la sumas y restas._

```javascript
r = -2 > 1 == (6 >= 3 && 10 < 2);
```

_Ahora procedemos a resolver las relaciones lógicas._

```javascript
r = false == (true && false);
```

_Primero debemos resolver la operación lógica AND dentro de las agrupaciones._

```javascript
r = false == false;
```

_Finalmente comparo la igualdad de ambas agrupaciones y asigno el valor a r._

```javascript
r = true;
```

_El resultado de toda la operación realizada será true._
