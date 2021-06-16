---
layout: post
title:  "Uso de Jupyter Notebook o Google Colaboratory como calculadora"
date:   2021-06-15 14:52:39
categories: jekyll
---

# Uso de Jupyter Notebook o Google Colaboratory como calculadora

Jupyter Notebook o Google Colaboratory pueden utilizarse como una simple calculadora. Basta con escribir la expresión (operación) en una celda, y ejecutar ésta para que se muestre el resultado.


```python
2 + 2
```
    4

## Números 

El núcleo de Jupyter Notebook y Google Colaboratory es el lenguaje Python; por lo tanto los números se van manejar conforme a éste lenguaje de programación.

Python puede manejar números enteros, racionales, irracionales, reales, imaginarios y complejos. Todos estos números se van a manejar en tres categorias, a saber:

+ Enteros positivos y negativos: Python los maneja como tipo *int*.
> + Enteros poitivos: $$\mathrm{(1,20,100, \text{etc})}$$
> + Enteros negativos: para indicar que un número es negativo se le antepone el guión medio "-", por ejemplo $$\mathrm{(-1,-20,-100, \text{etc})}$$. 


```python
1
```

    1

```python
20
```

    20

```python
100
```

    100

Los números se pueden almacenar (asignar) a una variable, para ello se usa el signo de igualdad $$\mathrm{(=)}$$.

**Sintaxis**

```
nombre_variable = valor_numérico
```


```python
a = 100
```

Una vez asigando un valor a una varible, posteriormente se puede hacer uso de ella para realizar operaciones.


```python
2*a
```




    200



+ Coma o punto flotante: Python los maneja como tipo *float*, y en esta categoría se agrupan a los números reales, racionales e irracionales, por ejemplo $$\mathrm{(0.5,3.141516,6.5, \text{etc})}$$. 



```python
0.5
```




    0.5




```python
3.141516

```




    3.141516




```python
6.5
```




    6.5



+ Números complejos: Python los maneja como *complex*, y en esta categoría se agrupan los números imaginarios y complejos: $$\mathrm{(3+5i,20i, \text{etc})}$$. 
> + Para indicar que es un número imaginario se le debe agregar al final la letra j.


```python
20j
```




    20j



> + Para indicar que es un número complejo, a la parte real se le debe sumar la parte imaginaria.

**Sintaxis**

```
parte_real + parte_imaginariaj
```


```python
3.0 + 5j
```




    (3+5j)



Asignemos a una variable el número complejo $$\mathrm{3.0 + 5i}$$:


```python
numero_complejo = 3.0 + 5j
```

+ Si sólo se desea la parte real del número complejo asignado a la variable *numero_complejo*, al nombre de la variable se le agrega un *punto* y la palabra *real*; es decir se hace uso del método *real*.

**Sintaxis**
```
nombre_varible.real
```



```python
numero_complejo.real
```




    3.0



+ Si sólo se desea la parte imaginaria del número complejo asignado a la variable *numero_complejo*, al nombre de la variable se le agrega un *punto* y la palabra *imag*.

**Sintaxis**
```
nombre_varibel.imag
```


```python
numero_complejo.imag
```




    5.0



### ¿Cómo sabemos qué tipo número estamos manejando?

La función *type()* permite saber que tipo de número u objeto se está manejando.

**Sintaxis**

```
type(objeto)
```


```python
type(1)
```




    int




```python
type(6.5)
```




    float




```python
type(20j)
```




    complex




```python
type(3+5j)
```




    complex



También puede indicar el tipo de número que contiene una variable:


```python
type(numero_complejo)
```




    complex



## Operaciones básicas

Para indicar las cuatro operaciones básicas, se usan los siguientes operadores:

> **Suma**

>> Se usa el símbolo $$\mathrm{+}$$ para realizar ésta operación.

> **Resta o sustracción**

>> Se usa el símbolo $$\mathrm{-}$$ para realizar ésta operación.

> **Multiplicación**

>> Se usa el símbolo $$\mathrm{\text{*}}$$ para realizar ésta operación.

> **División**

>> Se usa el símbolo $$\mathrm{/}$$ para realizar ésta operación.

```python
a = 5
b = 10
```


```python
a + b
```




    15




```python
a - b
```




    -5




```python
a * b
```




    50




```python
b / a
```




    2.0



### Potencias y raíces

#### Potencias

Para realizar la potenciación $$(x^y)$$ se utiliza el operador $$\mathrm{**}$$



```python
x = 2
y = 2
```


```python
x**y
```




    4




```python
x**3
```




    8



En el caso de potencias inversas $$\dfrac{1}{a^b}$$, se usan exponentes negativos. Recuerde que:

$$\dfrac{1}{a^b} = a^{-b}$$


```python
10**-1
```




    0.1




```python
10**-2
```




    0.01




```python
10**-3
```




    0.001



También se puede hacer uso de la función integrada *pow()*.

**Sintaxis**

```
pow(a,b)

donde a es la base y b la potencia.
```


```python
pow(a,b)
```




    9765625




```python
pow(a,3)
```




    125



#### Raíces

Para calcular raíces se usan decimales (fracciones). Recuerde que:

$$\sqrt[n]{a} = a^{\frac{1}{n}} $$


```python
a = 4
```


```python
a**(1/2)
```




    2.0




```python
27**(1/3)
```




    3.0



### Cociente (división sesgada) y resto de una división (módulo)

#### Cociente

Para obtener el cociente de una división se usa el operador $$\mathrm{//}$$.


```python
a = 10
b = 2
```


```python
a//b
```




    5




```python
a//3
```




    3



#### Resto de una división (módulo)

Para obtener el resto de una división se usa el operador %.


```python
a%b
```




    0




```python
a%3
```




    1



## Jerarquía de operaciones

Las operaciones se realizan de izquierda a derecha, considerando que las potencias y radicales tienen mayor jerarquía que la multiplicación, división, cociente y módulo; la suma y resta se realizan al último por ser las de menor jerarquía.

1. Potencias y radicales
2. Multiplicación, división, cociente y módulo
3. Suma y resta

¿Cuál es el resultado de la siguiente operación?

$$4+8\times 2\div 4 - 3^2 + \sqrt{4}$$


1. Empezamos a realizar las operaciones de izquierda a derecha considerando la jerarquía.
2. Como la potencia y el radical tiene la misma jerarquía,  se resuelve de izquierda a derecha, primero la potencia y después el radical. 

$$4+8\times 2\div 4 - 3^2 + \sqrt{4}$$

$$4+8\times 2\div 4 - 9 + \sqrt{4}$$

$$ 4+8\times 2\div 4 - 9 + 2 $$

3. Continuando con la jerarquía de las operaciones, ahora se realizan la multiplicación y la división, justo en ese orden. Siempre de izquierda a derecha.

$$ 4+8\times 2\div 4 - 9 + 2 $$

$$ 4+16\div 4 - 9 + 2 $$

$$ 4 + 4 - 9 + 2 $$

4. La suma y la resta tienen la misma jerarquía, las operaciones se realizan de izquierda a derecha.

$$ 4 + 4 - 9 + 2 $$

$$ 8 - 9 + 2 $$

$$ -1 + 2 $$

$$ 1 $$

**¡Veamos qué resultado arroja Pyhton!**


```python
4 + 8 * 2 / 4 - 3**2 + 4**(1/2)
```




    1.0



### Agrupamiento con paréntesis

Las operaciones que estén agrupadas dentro de paréntesis tienen mayor prioridad. Sin embargo, las operaciones dentro del paréntesis deben obedecer a la jerarquía de operaciones.

Considerando las operaciones anteriores, pero agrupando $$(4+8\times 2)$$

$$(4+8\times 2)\div 4-3^2+\sqrt{4}$$

¿Cuál es el resultado?

1. Empezando de izquierda a derecha y considerando que las operaciones entre paréntesis tienen prioridad.
2. Dentro del paréntesis hay una suma y una multiplicación; la multiplicación se realiza primero porque tiene mayor jeraquía que la suma.

$$(4+8\times 2)\div 4-3^2+\sqrt{4}$$

$$(4+16)\div 4-3^2+\sqrt{4}$$

$$20\div 4-3^2+\sqrt{4}$$

3. En las operaciones restantes, la potencia y el radical tienen mayor jerarquia; continuando de izquierda a derecha, primero se realiza la potencia y luego el radical.

$$20\div 4-3^2+\sqrt{4}$$

$$20\div 4-9+\sqrt{4}$$

$$20\div 4-9+2$$

4. Ahora se tiene una división, una resta y una suma. La división tiene mayor jerarquía

$$20\div 4-9+2$$

$$5-9+2$$

5. Por último se tiene una resta y una suma, operaciones con la misma jerarquía ¿Qué operación se realiza primero? Esto se resuelve haciendo las operaciones de izquierda a derecha.

$$5-9+2$$

$$-4+2$$

$$-2$$

¡Veamos qué dice Python!


```python
(4+8*2)/4-3**2+4**(1/2)

```




    -2.0



## Funciones internas

Python 3.8.5 cuenta con funciones internas que siempre están disponibles, es decir, sin la necesidad de cargar una biblioteca.

Para mayor referencia, se recomienda consultar el siguiente [link.](https://docs.python.org/es/3/library/functions.html)


**¡Veamos algunas funciones!**

### abs()

**Sintaxis**

```
abs(x)

Devuelve el valor absoluto de un número.
```


```python
abs(-3)
```




    3



### divmod(a,b)

**Sintaxis**

```
divmod(a,b)

Devuelve el cociente y el resto de a/b.
```


```python
divmod(10,2)
```




    (5, 0)




```python
divmod(10,3)
```




    (3, 1)




```python
divmod(2,3)
```




    (0, 2)




```python

divmod(6.5,3.0)
```




    (2.0, 0.5)



### round(x,n)

**Sintaxis**

```
round(x,n)

Devuelve el valor de x redondeado a n digitos tras el punto decimal. Si se omite n toma el valor de cero.
```


```python
round(3.141516,4)
```




    3.1415




```python
round(3.141516,2)
```




    3.14




```python
round(3.141516)
```




    3




```python
round(0.5)
```




    0




```python
round(0.6)
```




    1




```python
round(2.5)
```




    2




```python
round(2.6)
```




    3




```python
round(-0.5)
```




    0




```python
round(-0.6)
```




    -1



### list()

**Sintaxis**
```
list((n1,n2,n3,...))

Crea una lista de n objetos.
```


```python
lista = list((2,2,2,2,8))
```

### max()

**Sintaxis**
```
max(n1,n2,n3,...)

Deveulve el elemento con el máximo valor.
```


```python
max(2,10,5,9,15,51)
```




    51



También se la función *max* se puede aplicar a listas. 


```python
max(lista)
```




    8



### min()

**Sintaxis**
```
min(n1,n2,n3,...)

Deveulve el elemento con el mínimo valor.
```


```python
min(2,10,5,9,15,51)
```




    2



También la función *min* se puede aplicar a listas.


```python
min(lista)
```




    2



### sum()

**Sintaxis**
```
sum(iterable,inicio)

Deveulve la suma de todos los elementos del iterable.
```


```python
sum(lista)
```




    16



Al resultado de la suma de los elementos de lista, se le va a sumar 3


```python
sum(lista,3)
```




    19




```python

```
