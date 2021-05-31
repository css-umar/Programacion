---
layout: post
title:  "Variables, datos y operadores"
date:   2021-05-31 16:40:39
categories: Programacion
---

# Variables

Es el nombre de un objeto que está en la memoria de la computadora. El objeto puede ser de algún tipo de dato.

Por defecto, python maneja las variables como locales, al menos que se indique lo contrario a través de la sentencia global. 
En python no es necesario declarar el tipo de variable al momento de crearla.

**Sintaxis**
```
nombre_de_la_variable = valor_de_la_variable
```

Utilizar nombres descriptivos y en minúsculas. Para nombres compuestos, separar las palabras por guiones bajos. Antes y después del signo de asignación (=), debe haber uno (y solo un) espacio en blanco.

#### Ejemplos de variables
```python
"""
Las variables pueden almacenar datos numéricos, cadena de texto, o bien datos booleanos.
"""
mi_variable = 20
resp = "si"
condición = False    
```
Se pueden asignar valores a varias constantes en una sola línea.

```python
x_int, y_float, z_complex, cadena = 5, 3.1416, 4.0+3.0j, "texto"
print(x_int, y_float, z_complex,cadena)
```
```
(5, 3.1416, (4+3j), 'texto')
```
También se le puede asignar un solo valor a múltiples variables.
```python
x = y = z = 1.0
print(x,y,z)
```
```
(1.0, 1.0, 1.0)
```
## Constantes

A diferencia de las variables, una constante no puede ser cambiada durante la ejecución del programa.

**Sintaxis**
```
NOMBRE_DE_LA_CONSTANTE = VALOR_DE_LA_CONSTANTE
```
Utilizar nombres descriptivos y en mayúsculas separando palabras por guiones bajos.

## Datos
Toda información que requiere el algoritmo para funcionar correctamente. Por ejemplo, datos de tipo numéricos, alfanumérico, o bien del tipo booleano (verdadero o falso).

### Numéricos

Almacena números. En el caso de Python, maneja tres tipos de datos numéricos:

1. Enteros, int para números de precisón fija, y long en caso de overflow.
2. Punto o coma flotante, float
3. Complejos, complex

#### Ejemplos de datos tipo entero

```python
a_entero = 7    # Creamos una variable que almacena un dato del tipo entero
type (a_entero)    # La función type devuelve el tipo de dato que almacena la variable a_entero
```
```
int
```

```python
"""
El dato int tipo long permite almancenar números muy grandes, su precisión está limitada por la memoria de la máquina.
"""
a_long = 187687654564658970978909869576453    
print(a_long), type(a_long)
```
```
187687654564658970978909869576453 <type 'long'>
```
Otra forma de indicar a Python que un número es de tipo **long**, es añadiendo una L al final del número.

```python
entero_long = 18L
print(entero_long), type(entero_long)
```
```
18 <type 'long'>
```
#### Ejemplos de datos tipo punto o coma flotante

```pyhton
real = 3.1416    # Creamos la variable real, la cual almacena el número real 3.1416.
otro_real = 0.5076    # 0.5076 es otro número real.
otro_real2 = 5.076e-1    # Utilizando notación científica para el número 0.5076
```

```pyhton
type(real), type(otro_real), type (otro real2)
```
```
(float, float, float)
```
Las constantes $\pi$ y $e$ son del tipo float

```python
import numpy as np
print(np.pi), type(np.pi)
```
```
3.14159265359 <type 'float'>
```
```python
print(np.e),type(np.e)
```
```
2.71828182846 <type 'float'>
```
#### Ejemplos de datos tipo complejos

Se agrega una j a la parte imaginaria de un número complejo, siguiendo la sintaxis:

**Sintaxis**
```
nombre_variable_compleja = parte_real + parte_imaginariaj
```
```pyhton
numero_complejo = 2.0 + 8.0j
print(numero_complejo), type(numero_complejo)
```
```
(2.0+8.0j) <type 'complex'>
```
Si nada más se desea ingresar la parte imaginaria:

```pyhton
otro_complejo = 5.0j
print (otro_complejo), type(otro_complejo)
```
```
5.0j <type 'complex'>
```
Si se desea utilizar la parte imaginaria de un número complejo:
```python
numero_complejo.imag
```
```
8.0
```
Si se desea utilizar la parte real de un número complejo:
```python
numero_complejo.real
```
```
2.0
```
### Alfanuméricos
Se utiliza para almacenar cadena de caracteres. En el caso de python, son del tipo "str". Para indicar que es una cadena de caracteres, el texto debe estar entre comillas simples ('cadena de caracteres') o dobles ("cadena de caracteres"). 

#### Ejemplos de datos tipo alfanuméricos

```python
cadena = "cadena está formada por 6 letras"
print(cadena), type(cadena)
```
```
cadena está formada por 6 letras <type 'str'>
```
Otro ejemplo:
```python
otra_cadena = 'otra_cadena está formada por 11 caracteres'
print(otra_cadena), type(otra_cadena)
```
```
otra_cadena está formada por 11 caracteres <type 'str'>
```
### Booleano
Este tipo de datos sólo puede tener uno de los dos valores, False o True.

```python
type(False), type(True)
```
```
(bool,bool)
```
Otro ejemplo:
```python
a,b = 5,5
resp = a == b
print(resp),type(resp)
```
```
False <type 'bool'>
```
Uno más:
```python
a,b =6,5
resp = a == b
print(resp), type(resp)
```
```
False <type 'bool'>
```
```python
resp = a != b
print(resp), type(resp)
```
```
True <type 'bool'>
```

## Operadores relacionales

Permiten comparar valores de los diferentes tipos de datos

### Operador ==

Evalúa que los valores sean iguales. Si se cumple la igualdad, devuelve el booleano True, en caso contrario False.

```python
4 == 3,5 == 6,7 == 6.99, 6==6
```
```
(False, False, False, True)
```

```python
"A1" == "A1", "A2" == "A1"
```
```
(True, False)
```
```python
Dato="Alfa"
type(Dato)==str
```
```
True
```
```python
type(Dato)== int
```
```
False
```
### Operador !=
Evalúa si los valores son distintos. Si los valores son iguales, devuelve el booleano False, en caso contrario True.

```python
4!=3,5!=6,7!=6.99, 6!=6
```
```
(True, True, True, False)
```
```python
"A1"!="A1", "A2"!="A1"
```
```
(False, True)
```
### Operador <

Evalúa si el valor del lado izquierdo es menor que el valor del lado derecho.

```python
1 < 2, 5 < 4, 10 < 9
```
```
(True, False, False)
```

### Operador >
Evalúa si el valor del lado izquierdo es mayor que el valor del lado derecho.

```python
1 > 2, 5 > 4, 10 > 9
```
```
(False, True, True)
```
### Operador <=
Evalúa si el valor del lado izquierdo es menor o igual que el valor del lado derecho.

```python
1 <= 2, 2 <= 2, 10 <= 9
```
```
(True, True, False)
```

### Operador >=
Evalúa si el valor del lado izquierdo es mayor o igual que el valor del lado derecho.

```python
1 >= 2, 2 >= 2, 10 >= 9
```
```
(False, True, True)
```

## Operadores aritméticos
Siempre hay que colocar un espacio en blanco, antes y después de un operador.

<center>

|Símbolo|Significado|
|---|---|
|+ |Suma|
|-|Resta|
|-|Negativo(negación)|
|*|Multiplicación|
|**|Exponente|
|/|División|
|//|División entera|
|%|Módulo|

</center>
