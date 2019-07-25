# Unidad 2

## JavaScript

### Sintaxis

La sintaxis de un lenguaje de programación se define como el conjunto de reglas que deben seguirse al escribir el código fuente de los programas para considerarse como correctos para dicho lenguaje de programación.
La sintaxis de JavaScript es muy similar a la de otros lenguajes de programación como Java y C. Las normas básicas que definen la sintaxis de JavaScript son las siguientes:<br />
<br />

-   _No se tienen en cuenta los espacios en blanco y las nuevas líneas:_<br />
    el intérprete de JavaScript ignora cualquier espacio en blanco sobrante, por lo que el código se puede ordenar de forma adecuada para entenderlo mejor (tabulando las líneas, añadiendo espacios, creando nuevas líneas, etc.)<br />

-   _Se distinguen las mayúsculas y minúsculas:_<br />
    se dice que JavaScript es case sensitive, esto quiere decir que una palabra escrita en minúsculas es distinta a la misma palabra con una o todas sus letras en mayúsculas, por lo que la variación influye.<br />

-   _No se define el tipo de dato de las variables:_<br />
    al crear una variable, no es necesario indicar el tipo de dato que almacenará. De esta forma, una misma variable puede almacenar diferentes tipos de datos durante la ejecución del script.<br />

-   _Cada sentencia debería terminar con punto y coma (;):_<br />
    en la mayoría de lenguajes de programación, es obligatorio terminar cada sentencia con punto y coma (;). Aunque JavaScript no obliga a hacerlo, es conveniente seguir la tradición de terminar cada sentencia con punto y coma (;).<br />

-   _Se pueden incluir comentarios:_<br />
    los comentarios se utilizan para añadir información en el código fuente del programa. Aunque el contenido de los comentarios no se visualiza por pantalla, sí se envía al navegador del usuario junto con el resto del script, por lo que es necesario extremar las precauciones sobre la información incluida en los comentarios.<br />
    JavaScript tiene dos formas de escribir comentarios, los de una sola línea y los que ocupan varias líneas.<br />
    _Una sola línea de comentario:_ se definen añadiendo dos barras oblicuas (//) al principio de la línea.<br />
    Ejemplo:<br />
    // a continuación se declarará una variable, pero esta línea es un comentario var nombreVariable;<br />
    _Varias líneas de comentario:_ se definen encerrando el texto del comentario entre los símbolos /\* y \*/.<br />
    Ejemplo:<br />
    /\* Los comentarios de varias líneas son muy útiles cuando se necesita incluir bastante <br />información en los comentarios.<br />
    A continuación declaro una nueva variable \*/<br />
    var nuevaVariable;<br />

### Etiqueta script

Para que el navegador interprete el código JavaScript utilizaremos las etiquetas HTML
`<script></script>`, que se pueden incluir tanto en la cabecera del documento (entre etiquetas
`<head></head>`), como en en el cuerpo del mismo (entre etiquetas
`<body></body>`).
En caso de querer incluir código JavaScript dentro de un documento XHTML y que resulte válido, se debe asignar el atributo type a la etiqueta de apertura `<script>`.
Los valores que se le pueden asignar al atributo type están estandarizados y para el caso de JavaScript el valor correcto es text/javascript.
También se puede colocar el código JavaScript en un documento de extensión .js e incluirlo en el documento HTML.<br />

```html
<script type="text/javascript"></script>
```

**Inserción de código JavaScript en la cabecera de un documento HTML:**<br />
Al colocar código JavaScript entre etiquetas `<script></script>` dentro de las etiquetas `<head></head>`, el script se ejecutará secuencialmente al cargarse la cabecera y luego se cargará el resto del documento en el navegador.<br />

**archivo_1.html**

```html
<html>
    <head>
        <title>Archivo 1</title>
        <script type="text/javascript">
            // El código:
            var unaVariable = 1;
        </script>
    </head>
    <body>
        <p>Esto es un párrafo</p>
    </body>
</html>
```

En archivo_1.html el código se ejecutará durante la carga de la cabecera. Cuando se ejecute, se declarará e inicializará la variable unaVariable. Una vez ejecutado, se mostrará el contenido del documento, en este caso el párrafo.<br /><br />

**Inserción de código JavaScript en el cuerpo de un documento HTML:**<br />
Al colocar código JavaScript entre etiquetas `<script></script>` dentro de las etiquetas `<body></body>`, el script se ejecutará secuencialmente a medida que cargue el contenido del documento en el navegador.<br />

**archivo_2.html**

```html
<html>
    <head>
        <title>Archivo 2</title>
    </head>
    <body>
        <p>Antes del script</p>
        <script type="text/javascript">
            // El código:
            var miVariable = 1;
        </script>
        <p>Después del script</p>
    </body>
</html>
```

En archivo_2.html el código se ejecutará durante la carga del cuerpo, luego de mostrar el contenido del primer párrafo. Cuando se ejecute, se declarará e inicializará la variable miVariable. Una vez ejecutado, se mostrará el contenido del segundo párrafo.<br /><br />

**Inserción de código JavaScript desde un archivo externo:**<br />
En este caso se escribe todo el código en un archivo externo cuya extensión será .js, y luego se incluye dentro del documento HTML. Según donde se coloquen las etiquetas <script></script> que llamen al documento externo, el script se ejecutará secuencialmente al cargarse esa parte del documento en el navegador.
Esta forma de manejar los archivos es la más utilizada, ya que permite separar el código JavaScript del documento HTML.<br />

**codigo.js**

```javascript
// El código:
var otraVariable = 1;
```

**archivo_3.html**

```html
<html>
    <head>
        <title>Archivo 3</title>
        <script type="text/javascript" src="codigo.js"></script>
    </head>
    <body>
        <p>Esto es un párrafo</p>
    </body>
</html>
```

En archivo_3.html el código del archivo codigo.js será incluido en el documento mediante el atributo src en la etiqueta de apertura `<script>`. En este caso funcionará igual que archivo_1.html, el código se ejecutará durante la carga de la cabecera. Cuando se ejecute, se declarará e inicializará la variable otraVariable. Una vez ejecutado, se mostrará el contenido del documento, en este caso el párrafo.<br /><br />

**Etiqueta noscript:**<br />
En caso de que un navegador en el que se muestra una página con código JavaScript no lo tenga habilitado, se puede informar la necesidad de habilitarlo mediante las etiquetas HTML `<noscript></noscript>`.<br />
Las etiquetas `<noscript></noscript>` se debe incluir entre las etiquetas `<body></body>` en la zona donde desee mostrarse el mensaje de deseado.<br />
Las etiquetas `<noscript></noscript>` pueden incluir cualquier etiqueta HTML.<br />

**archivo_4.html**

```html
<html>
    <head>
        <title>Archivo 4</title>
    </head>
    <body>
        <h1>Bienvenido</h1>
        <script type="text/javascript">
            // El código:
            var laVariable = 1;
        </script>
        <noscript>
            <p>Advertencia</p>
            <p>Esta página requiere habilitar JavaScript</p>
        </noscript>
    </body>
</html>
```

Si al abrir el archivo_4.html el navegador que lo interpreta no tiene JavaScript habilitado, se verá en pantalla el contenido del encabezado 1 y de los párrafos dentro de las etiquetas `<noscript></noscript>`, pero no se ejecutará el código.<br />
Si al contrario, tiene habilitado JavaScript, el código se ejecutará durante la carga del cuerpo, luego de mostrar el contenido del encabezado 1. Cuando se ejecute, se declarará e inicializará la variable laVariable y no se mostrará el contenido de las etiquetas `<noscript></noscript>`.<br />

##Ingreso y egreso de información

###Método prompt:
Este método o función del navegador cuando se ejecuta muestra una ventana emergente con botones “Aceptar” y “Cancelar”, un texto que se puede definir y un campo de entrada de texto con un valor predeterminado que también se puede definir.
En caso de pulsar el botón “Aceptar”, se obtiene el valor ingresado en el campo de texto.
En caso de pulsar el botón “Cancelar” o se cierra la ventana emergente, se obtiene el valor null.
Este método se utilizará para solicitar datos al usuario durante la ejecución del script, estos datos deberán ser guardados en una variable para su posterior manipulación.

```javascript
var valor = prompt('Ingrese un valor', 'valor por defecto');
```

![alt text](images/promp.png 'prompt')

En el ejemplo anterior se puede observar que la estructura de este método consta de la palabra prompt seguido de unos paréntesis que encierran dos valores separados con coma (,). El primer valor es el texto que aparece sobre el campo de entrada y el sgundo valor es el valor por defecto que aparece dentro de este campo.<br />
También se puede observar que una vez que se pulsa alguno de los tres botones ("Aceptar", "Cancelar" o "Cerrar"), el valor obtenido se guardará, en este ejemplo, en la variable valor.
Se debe tener en cuenta, que cualquier valor ingresado, excepto el null, se tomará como tipo de dato cadena, lo que significa que si se escribe un número en el campo de texto, el valor obtenido no será del tipo de dato numérico, por lo que no se podrán realizar operaciones numéricas.<br /><br />

Para que el valor obtenido sea numérico es necesario convertirlo. JavaScript ofrece dos métodos: parseInt (convierte el valor a convertir en un tipo de dato numérico entero) y parseFloat (convierte el valor a convertir en un tipo de dato numérico de punto flotante).<br />

**parseInt**

```javascript
    var numero = prompt("Ingrese un número", "0"); // Ingreso el valor 1.5, que en realidad se guarda como "1.5" numero = parseInt(numero); // Luego de la
    conversión, numero valdrá 1 numérico entero
```

En el ejemplo anterior se puede observar que la estructura del método parseInt consta de la palabra parseInt (con la letra i en mayúscula) seguido de unos paréntesis que encierran el valor a convertir. Este nuevo valor se guardará, en este ejemplo, nuevamente en la variable numero, pero con el tipo de dato numérico entero.

**parseFloat**

```javascript
    var numero = prompt("Ingrese un número", "0"); // Ingreso el valor 1.5, que en realidad se guarda como "1.5" numero = parseFloat(numero); // Luego de la
    conversión, numero valdrá 1.5 numérico flotante
```

En el ejemplo anterior se puede observar que la estructura del método parseFloat consta de la palabra parseFloat (con la letra f en mayúscula) seguido de unos paréntesis que encierran el valor a convertir. Este nuevo valor se guardará, en este ejemplo, nuevamente en la variable numero, pero con el tipo de dato numérico flotante.<br />
Finalmente, es posible realizar la conversión en la misma línea que se ingresa el valor.

**parseInt**

```javascript
var numero = parseInt(prompt('Ingrese un número', '0'));
/* En la línea anterior se obtendrá el valor mediante el prompt lugo se lo convertirá en número entero
y finalmente se guardará en la variable número */
```

**parseFloat**

```javascript
var numero = parseFloat(prompt("Ingrese un número", "0"));
/* En la línea anterior se obtendrá el valor mediante el prompt lugo se lo convertirá en número punto flotante */
y finalmente se guardará en la variable número
```

**Método confirm:**
Este método o función del navegador cuando se ejecuta muestra una ventana emergente con botones “Aceptar” y “Cancelar” y un texto que se puede definir.<br />
En caso de pulsar el botón “Aceptar”, se obtiene el valor lógico true.<br />
En caso de pulsar el botón “Cancelar” o se cierra la ventana emergente, se obtiene el valor lógico false.<br />
Este método se utilizará para solicitar al usuario una respuesta lógica durante la ejecución del script, esta respuesta deberá ser guardada en una variable para su posterior manipulación.

```javascript
var valor = confirm('Desea aceptar o cancelar?');
```

![alt text](images/confirm.png 'confirm')

En el ejemplo anterior se puede observar que la estructura de este método consta de la palabra confirm seguido de unos paréntesis que encierran un valor. Este valor es el texto que aparece sobre los botones.
También se puede observar que una vez que se pulsa alguno de los tres botones ("Aceptar", "Cancelar" o "Cerrar"), el valor lógico obtenido se guardará, en este ejemplo, en la variable valor.<br />

**Método alert**
Este método o función del navegador cuando se ejecuta muestra una ventana emergente con un botón “Aceptar” y un texto que se puede definir.<br />
Al pulsar el botón “Aceptar”, se cierra la ventana, no se obtiene ningún valor.<br />
Este método se utilizará mostrar en pantalla un valor durante la ejecución del script.

```javascript
alert('Esto es un mensaje a través de alert');
```

![alt text](images/alert.png 'alert')

En el ejemplo anterior se puede observar que la estructura de este método consta de la palabra alert seguido de unos paréntesis que encierran un valor. Este valor es el texto que aparece sobre el botón.
Se debe tener en cuenta que la ejecución del script se pausa hasta que se pulse el botón "Aceptar", luego se continuará ejecutando el script. Se puede mostrar cualquier tipo de valor.

**Método document.write**
Este método o función del documento cuando se ejecuta genera código HTML que se agrega al documento. Este método se utilizará para agregar al documento un valor durante la ejecución del script.

```html
<body>
    <script type="text/javascript">
        document.write('<h1>Encabezado generado por JavaScript</h1>');
    </script>
    <p>Párrafo</p>
</body>
```

![alt text](images/encabezado.png 'encabezado')

En el ejemplo anterior se puede observar que la estructura de este método consta de las palabra document.write seguido de unos paréntesis que encierran un valor. Este valor se agregará al documento en el lugar secuencial donde se ejecute el código.<br />
En el ejemplo, el encabezado es generado desde JavaScript, se agrega al documento antes del párrafo.<br />
Se debe tener en cuenta que las etiquetas HTML a utilizar dentro de este método son consideradas cadenas,por lo que deben ir entre comillas. Se puede mostrar cualquier tipo de valor. No es obligatorio el uso de etiquetas HTML.

### Caracteres especiales

**Escape de caracteres**
Existe un conjunto de caracteres especiales que al ser interpretados por el navedagor, afectan a la cadena de texto a mostrar.<br />
Se los reconoce porque comienzan con el caracter de barra invertida (\).<br />
Algunos de ellos son:<br />

-   \n: salto de línea
-   \t: tabulación
-   \b: retroceso de línea
-   \f: avance de línea
-   \r: return
-   \': comilla simple (').
-   \": comilla doble (").
-   \\: barra invertida (').

```javascript
alert('Esto es un "mensaje" a través de\nalert');
```

![alt text](images/alert_escapado.png 'alert escapado')
En el ejemplo anterior se puede observar:

-   El uso de comillas dobles dentro de la cadena a través de \".
-   Un salto de línea dentro de la cadena a través de \n.
