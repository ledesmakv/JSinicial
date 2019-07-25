# Unidad 3

## Planteo de algoritmos

### Algoritmo:

Se lo puede plantear de dos maneras:

-   _Diagrama de flujo:_ esquema estructurado que debe poder ser leído secuencialmente.
-   _Pseudocódigo:_ utilización de un lenguaje propio para describir los procesos secuenciales del algoritmo.
    Luego se procede a la codificación, proceso que pasa el algoritmo a código informático.

**Diagrama de flujo**
![alt text](images/diagrama_flujo.png 'diagrama de flujo')

**Código**

```javascript
var A = parseFloat(prompt('Ingresar valor de A'));
var B = parseFloat(prompt('Ingresar valor de B'));
var C = A + B;
alert(C);
```

## Condicionales

### Estructura if – else:

Estructura que permite efectuar determinadas acciones en base a una condición lógica.
La sintaxis de un condicional simple es: if(condición) { sentencias para true } else { sentencias para false } El uso del else es optativo, solamente es obligatorio el uso del if.

**Diagrama de flujo**
![alt text](images/diagrama_if.png 'diagrama de flujo if-else')

**Código**

```javascript
var valor = parseFloat(prompt('Ingrese un número'));
if (valor == 0) {
    alert('el número ingresado es cero');
} else {
    alert('el número ingresado no es cero');
}
```

### Estructura if – else anidada:

Estructura que se utiliza cuando se debe volver a preguntar dentro de la respuesta de una condición lógica.

**Diagrama de flujo**
![alt text](images/if_anidado.png 'diagrama de flujo if anidados')

**Código**

```javascript
var valor = parseFloat(prompt('Ingrese un número'));
if (valor != 0) {
    if (valor > 0) {
        alert('el número es positivo');
    } else {
        alert('el número es negativo');
    }
} else {
    alert('el número ingresado es cero');
}
```

### Estructura if – else if – else:

Estructura que permite replantear una condición si la anterior no se cumple. Acepta como última parte un else, que es optativo.
Se pueden encadenar la cantidad de _else if_ que sean necesarios.

**Código**

```javascript
if (condición) {
    ...
} else if (condición) {
    ...
} else {
    ...
}
```

### Operador ternario:

Su sintaxis es:
variable = (condición) ? valor verdadero : valor falso;

**Código**

```javascript
var respuesta;
var valor = parseFloat(prompt('Ingrese un número'));
respuesta = valor == 0 ? 'el número es cero' : 'el número no es cero';
alert(respuesta);
```

Es decir, si la condición entre paréntesis es verdadera a variable le es asignado el valor verdadero, si es falsa, le es asignado el valor falso.

### Estructura switch:

Esta estructura es un selector de casos, su funcionamiento es similar al condicional else – if.
Este selector tendrá un valor a analizar y lo compara con los case que tenga definidos, que serán valores.
Luego de cada case, se debe poner un break para indicar que de ser el case correcto, salga del selector.
Además, luego del último case/break es recomendable que haya un default, que es el caso por defecto, lo que hará si ninguno de los valores comparados coincide. Éste último no requiere un break, ya que será la última opción a comparar.
En caso de querer ejecutar la misma acción para más de un case, se debe poner los case seguidos, luego las instrucciones y un break.

**Diagrama de flujo**
![alt text](images/switch.png 'estructura de switch')

**Código**

```javascript
switch(valor a analizar){
      case valor 1:
            sentencias
      break;
      case valor 2:
            sentencias
      break;
      case valor 3:
            sentencias
      break;
      ...
      case valor n:
            sentencias
      break;
      default:
            sentencias
}
```

## Ciclos de repetición

## Estructura for:

Estructura que permite efectuar reiteradas acciones conociendo el número de repeticiones que serán necesarias. La sintaxis es: for(condición inicial; condición de ciclo; incrmento/decrmento) { sentencias a repetir }

**Diagrama de flujo**
![alt text](images/for.png 'estructura de for')

**Código**

```javascript
var valor;
// Ciclo que repetirá el proceso 10 veces:
for (var i = 0; i < 10; i++) {
    valor = parseFloat(prompt('Ingrese un número'));
    document.write('El valor ingresador es ' + valor);
    document.write('El valor de i es ' + i);
}
// Ciclo que repetirá el proceso 15 veces:
for (var i = 15; i > 0; i--) {
    valor = parseFloat(prompt('Ingrese un número'));
    document.write('El valor ingresador es ' + valor);
    document.write('El valor de i es ' + i);
}
```

### Estructura while:

Estructura que permite efectuar reiteradas acciones mientras se cumpla una condición. Primero verifica si se cumple la condición y luego entra al ciclo.
La sintaxis es: while(condición necesaria) { sentencias a repetir }

**Diagrama de flujo**
![alt text](images/while.png 'estructura de while')

**Código**

```javascript
var valor;
// Ciclo que repetirá mientras el valor sea distinto de 0:
valor = parseFloat(prompt('Ingrese un número'));
while (valor != 0) {
    document.write('El valor ingresador es ' + valor);
    valor = parseFloat(prompt('Ingrese un número'));
}
// Necesito volver a pedir el valor dentro del ciclo para evitar que sea infinito.
```

### Estructura do while:

Estructura que permite efectuar reiteradas acciones mientras se cumpla una condición. Efectua el primer ciclo de y luego verifica si se cumple la condición para volver a repetir el ciclo.
La sintaxis es: do { sentencias a repetir } while(condición necesaria)

**Diagrama de flujo**
![alt text](images/dowhile.png 'estructura de do while')

**Código**

```javascript
var valor;
// Ciclo que repetirá mientras el valor sea distinto de 0:
do {
    valor = parseFloat(prompt('Ingrese un número'));
    document.write('El valor ingresador es ' + valor);
} while (valor != 0);
```

## Validación

## Operador isNaN:

Este operador determina si un valor no es un número (Not a Number), devuelve true si es NaN y false si no lo es. La sintaxis del isNaN es: respuesta = isNaN(valor);

```javascript
var valor;
valor = parseFloat(prompt('Ingrese un número'));
var respuesta = isNaN(valor);
document.write(respuesta);
```

Este operador servirá para realizar validaciones, ya que en el desarrollo de programas cuando se le pide ingreso de datos al usuario, se debe estar seguro de que el dato fue ingresado y que éste respeta la condición solicitada.

## Validación de números:

Para hacer este tipo de validación se utiliza el operador isNaN y el ciclo de repetición do while, ya que de no haber ingresado un número, se le debe solicitar al usuario que ingrese de nuevo el valor.

```javascript
var valor;
do {
    valor = parseFloat(prompt('Ingrese un número'));
} while (isNaN(valor) == true);
```

En el ejemplo anterior podemos observar que la condición de repetición es que el valor ingresado sea un NaN.

## Validación de textos:

Para hacer este tipo de validación se utiliza el operador isNaN y el ciclo de repetición do while, ya que de no haber ingresado un texto, se le debe solicitar al usuario que ingrese de nuevo el valor.

```javascript
var valor;
do {
    valor = prompt('Ingrese un número');
} while (isNaN(valor) == false);
```

En el ejemplo anterior podemos observar que la condición de repetición es que el valor ingresado no sea un NaN.

## Variables auxiliares

### Contadores:

La variable auxiliar del tipo contador irá guardando una cantidad de valores, generalmente dentro de un ciclo. Para realizar la cuenta de valores suele utilizarse el operador de incremento ++.
La variable auxiliar que se utiliza como contador se debe inicializar, generalmente con el valor 0.

```javascript
var valor;
var contador = 0;
do {
    valor = prompt('Ingrese un número');
    contador++;
} while (contador == 10);
```

En el ejemplo anterior se puede observar que la variable contador se utiliza para ir contando la cantidad de valores ingresados. Cuando el contador llegue a 10, el ciclo termina.

### Acumularores:

La variable auxiliar del tipo acumulador irá guardando una sumatoria de valores, generalmente dentro de un ciclo. Para realizar la acumulación de valores suele utilizarse el operador de asignación +=.
La variable auxiliar que se utiliza como acumulador se debe inicializar, generalmente con el valor 0.

```javascript
var valor;
var acumulador = 0;
do {
    valor = prompt('Ingrese un número');
    acumulador += valor;
} while (valor != 0);
document.write(acumulador);
```

En el ejemplo anterior se puede observar que la variable acumulador se utiliza para ir sumando los distintos valores ingresados. En caso que el número ingresado sea 0, termina el ciclo y muestra el valor del acumulador.

### Máximos y mínimos:

Este tipo de variables auxiliares sirven para obtener los valores máximos y mínimos, generalmente dentro de un ciclo.
Para obtenerlos, se debe contar la cantidad de valores ingresados. El primer valor será el de referencia,a partir del segundo valor se comenzará a comparar.

```javascript
var valor,
    minimo,
    maximo,
    contador = 0;
do {
    valor = prompt('Ingrese un número');
    if (contador == 0) {
        minimo = valor;
        maximo = valor;
    } else {
        minimo == valor < minimo ? valor : minimo;
        maximo == valor > maximo ? valor : maximo;
    }
    contador++;
} while (valor != 0);
```
