---
layout: post
title:  "Estructuras de control cíclicas"
date:   2021-06-08 16:40:39
categories: Estructuras
---
<html>
<head>
</style>
<script type="text/x-mathjax-config">
    MathJax.Hub.Config({
      tex2jax: {
        skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
        inlineMath: [['$','$']]
      }
    });
  </script>
  <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script> 	
</body>
</html>
	
	

# Estructuras de control cíclicas

Este tipo de estructuras permiten ejecutar de manera repetida una sección de intrucciones, mientras se cumpla una condición.

_Python_ dispone del ciclo **while** y del **for**:

## Ciclo while (mientras)

Ejecuta una sección de instrucciones mientras que una determinada condición (expresión lógica) se cumpla; se pueden construir los siguientes tipos de ciclo _while_:

**Controlado por conteo**

**Controlado por evento**

**Combinado con la sentencia else**

1. Ciclo while controlado por conteo:
> **Sintaxis:**

~~~
contador = valor_inicial
while contador expresión_logica:
    instrucción_1
    instrucción_2
    instrucción_n
    contador = contador + incremento
~~~

2. Ciclo while controlado por evento
> **Sintaxis**

~~~
evento = valor_inicial
while evento expresión_lógica:
    instrucción_1
    instrucción_2
    instrucción_n
    evento = nuevo_valor
~~~

3. Ciclo while combinado con la sentencia _else_.
> **Sintaxis**

~~~
evento = valor_inicial
while evento expresión_lógica:
    instrucción_1
    instrucción_2
    instrucción_n
    evento = nuevo_valor
else:
    instrucción_1
    instrucción_2
    instrucción_n
~~~

## Ciclo for (para)

Esta estructura permite iterar sobre elementos o unidades que forman parte de un conjunto (listas, tuplas o cadenas de caracteres) en la misma secuencia en que están ordenados. Dependiendo del conjunto sobre el que se quiere iterar, se pueden construir los siguientes tipos de ciclo _for_:

**Con listas**

**Con listas y la función range (intervalo, serie) y len ()**

**Con tuplas**

**Con diccionarios**

**Con la sentencia else**

1. Ciclo for con listas.

> **Sintaxis**

~~~
lista = [elemento_1, elemento_2,...,elemento_n]
for variable in lista:
    instrucción_1
    instrucción_2
    instrucción_n    
~~~

2. Ciclo for con listas y la función range y len.

> **Sintaxis**

~~~
lista = [elemento_1, elemento_2,...,elemento_n]
for variable in range(len(lista)):
    instrucción_1
    instrucción_2
    instrucción_n    
~~~

3. Ciclo for con tuplas.

> **Sintaxis**

~~~
tupla = (elemento_1, elemento_2,...,elemento_n)
for variable in tupla:
    instrucción_1
    instrucción_2
    instrucción_n    
~~~

4. Ciclo for con diccionarios.

> **Sintaxis**

~~~
diccionario = {
    "clave_1": datos_1 
    "clave_2": datos_2
    "clave_n": datos_n
    }
clave = diccionario.keys()  # Devuelve una lista de las claves ["clave_1", "clave_2","clave_n"]
valor = diccionario.values()  # Devuelve una lista de los datos ["datos_1", "datos_2","datos_n"]
cantidad_datos = diccionario.items()  # Develve una lista de los elementos del diccionario
for clave, valor in cantidad_datos:
    instrucción_1
    instrucción_2
    instrucción_n    
~~~

5. Ciclo for con la sentencia else.

> **Sintaxis**

~~~
lista = [elemento_1, elemento_2,...,elemento_n]
for variable in lista:
    instrucción_1
    instrucción_2
    instrucción_n
else:
    instrucción_1
    instrucción_2
    instrucción_n
~~~


### Ejemplo de la estructura while controlado por conteo:

Dados los n números $ \{ x_{1},x_{2},\ldots ,x_{n} \} $, la media aritmética se define como:

$$\bar {x} = \frac{1}{n}\sum_{i=1}^{n}{x_i}=\dfrac{x_1+x_2+\ldots+x_n}{n} $$ 

**Escribir un programa que calcule la media aritmética de $n$ números.**

> ¿Qué se requiere para calcular la media aritmética?

>> Se requiere el número de elementos $(n)$ que componen la serie de datos.

> ¿Qué tipos de datos se ocupan para calcular la media aritmética?

>> Se ocupan datos numéricos, del tipo _int_ para $n$, y del tipo _float_ para los elementos de la serie de datos.


```python
"""
SEUDOCÓDIGO
Algoritmo media_aritmetica
	Escribir "¿Cuántos elmentos componen tus datos?"
	Leer n
	contador <- 1
	suma <- 0
	Mientras contador <= n Hacer
		Escribir "Introduce el elemento", contador
		Leer elemento
		suma <- suma + elemento
		contador <- contador + 1
	Fin Mientras
	
	prom <- suma / n
	Escribir prom
	
FinAlgoritmo
"""
# CODIGO PYTHON
print ("¿Cuantos elmentos componen tus datos?")
N = int(raw_input())
contador = 1
suma = 0.0
while contador <= N:
    print("Introduce el elemento"," ", contador)
    elemento = float(raw_input())
    suma = suma + elemento
    contador = contador + 1

prom = suma / N
print(prom)
```

    ¿Cuantos elmentos componen tus datos?
    3
    ('Introduce el elemento', ' ', 1)
    10
    ('Introduce el elemento', ' ', 2)
    10
    ('Introduce el elemento', ' ', 3)
    10
    10.0
    

### Ejemplo de la estructura while controlado por evento

Escribir un programa que calcule e imprima la suma de tres números; una vez impreso el resultado preguntar al usuario si requiere hacer la suma nuevamente.


```python
"""
Algoritmo suma_tres_numeros
	
	resp <- 1
	
	Mientras resp == 1 Hacer
		Escribir "Introduce el primer número"
		Leer num1
		Escribir "Introduce el segundo número"
		Leer num2
		Escribir "Introduce el tercer número"
		Leer num3
		
		suma <- num1 + num2 + num3
		
		Escribir "La suma es", " ", suma
		
		Escribir "¿Quieres realizar la suma nuevamente?"
		Escribir "En caso afirmativo teclea 1, de lo contrario cualquier otra tecla"
		Leer resp		
	Fin Mientras	
	
FinAlgoritmo

"""

resp = 1
while resp == 1:
    print("Introduce el primer número")
    num1 = float(raw_input())
    print("Introduce el segundo número")
    num2 = float(raw_input())
    print("Introduce el tercer número")
    num3 = float(raw_input())
    
    suma = num1 + num2 + num3
    print("La suma es", ' ', suma)
    
    print("¿Quieres realizar la suma nuevamente?")
    print("En caso afirmativo teclea 1, de lo contrario cualquier otra tecla")
    resp = int(raw_input())
```

    Introduce el primer número
    8
    Introduce el segundo número
    9
    Introduce el tercer número
    10
    ('La suma es', ' ', 27.0)
    ¿Quieres realizar la suma nuevamente?
    En caso afirmativo teclea 1, de lo contrario cualquier otra tecla
    9
    

### Ejemplo de la estructura while combinado con la sentencia else.

Escriba un programa que calcule tu promedio de calificaciones. El programa debe pedir tu calificación en cada ciclo, una vez termines de intriducir tus datos, el programa debe calcular el promedio.


```python
cal = 0.0
contador = 0
suma = 0.0
while cal != -1:
    suma = suma + cal
    contador = contador + 1  
    print("¿Introduciendo tu calificación?")
    print("Teclea -1 para terminar y calcular tu promedio")
    cal = float(raw_input())      
    
else:
    promedio = suma / (contador - 1)
    print ("Tu promedio es:" + str(promedio))

```

    ¿Introduciendo tu calificación?
    Teclea -1 para terminar y calcular tu promedio
    9
    ¿Introduciendo tu calificación?
    Teclea -1 para terminar y calcular tu promedio
    8
    ¿Introduciendo tu calificación?
    Teclea -1 para terminar y calcular tu promedio
    10
    ¿Introduciendo tu calificación?
    Teclea -1 para terminar y calcular tu promedio
    -1
    Tu promedio es:9.0
    

### Ejemplo de ciclo for con listas


```python
lista1 = [1,2,3,4,5,6,7,8,9,10]
for i in lista1:
    print i
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    10
    


```python
lista2=["Fulano","Zutano", "Perengano", "Mengano"]
for i in lista2:
    print i
```

    Fulano
    Zutano
    Perengano
    Mengano
    

### Ejemplo de ciclo for con listas y la función range y len


```python
"""
La función len(Nombre_Lista) devuelve el número de elementos de la lista, 
por ejemplo, la lista1 tiene diez elementos, mientras que lista2 contiene 
cuatro elementos, a saber: "Fulano","Zutano", "Perengano", "Mengano".
"""
tamano_lista1 = len(lista1)
tamano_lista2 = len(lista2)
print("Elementos lista1=" + str(tamano_lista1),
      "Elementos lista2=" + str(tamano_lista2))
```

    ('Elementos lista1=10', 'Elementos lista2=4')
    


```python
range(tamano_lista1)
```




    [0, 1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
"""
La función range(Número) crea una lista con una serie de n elementos, 
empezando en cero. Por ejemplo, el tamaño de la lista2 se almacenó en 
tamano_lista2, y con el tamano_lista2 se creo la lista serie_lista2.
"""
serie_lista2 = range(tamano_lista2)
```


```python
serie_lista2
```




    [0, 1, 2, 3]




```python
"""
También la funcion range() puede crear series considerando un punto inicial 
y final, más un tamaño de paso

SINTAXIS

range(punto_inicial, punto_final, tamaño de paso)

El siguiente ejemplo crea una lista con una serie que inicia en 1 y termina 
en 9, no considera al 10, el tamaño de paso es 1.
"""

range(1,10,1)
```




    [1, 2, 3, 4, 5, 6, 7, 8, 9]




```python
"""
También se puede ir en en sentido contrario, por ejemplo, que inicie en 10 y 
terminen en 1, con un decremento de -1.
"""
range(10,1,-1)
```




    [10, 9, 8, 7, 6, 5, 4, 3, 2]




```python
"""
En este ejemplo se utiliza la función range junto con el ciclo for
"""

for i in range(1,10,1):
    print i
```

    1
    2
    3
    4
    5
    6
    7
    8
    9
    

### Ejemplo de ciclo for con tuplas.

Funciona igual que con listas, nada más que ahora se itera sobre una tupla.


```python
tupla=("Fulano","Zutano", "Perengano", "Mengano")
for i in tupla:
    print i
```

    Fulano
    Zutano
    Perengano
    Mengano
    

### Ejemplo de ciclo for con diccionarios.


```python
carbono = {
    "Nombre": "Carbono",
    "Simbolo" :"C",
    "Serie" : "No metales",
    "Grupo": "12",
    "Masa_atomica":"12.0107"
}
clave = carbono.keys()
valor = carbono.values()
cantidad_datos = carbono.items()

for clave, valor in cantidad_datos:
    print clave + ": " + valor
```

    Nombre: Carbono
    Grupo: 12
    Masa_atomica: 12.0107
    Simbolo: C
    Serie: No metales
    

### Ejemplo de ciclo for con la sentencia else.


```python
tupla_datos = "Zutano", "castillo", "Av. Juanda de Arco", "No 32"

for generales in tupla_datos:
    print generales
else:
    print ("Una vez que se termine de iterar sobre la tupla o lista," )
    print ("se ejecutan las instrucciones de la sentencia else, o bien,")
    print ("cuando la expresión condicional del ciclo for sea False")
    
    
    
```

    Zutano
    castillo
    Av. Juanda de Arco
    No 32
    Una vez que se termine de iterar sobre la tupla o lista,
    se ejecutan las instrucciones de la sentencia else, o bien,
    cuando la expresión condicional del ciclo for sea False
    


```python

```
