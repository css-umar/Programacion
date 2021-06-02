---
layout: post
title:  "Datos complejos"
date:   2021-05-31 16:40:39
categories: Tipos de datos
---

# Tuplas 

Una tupla es una variable que permite almacenar varios datos inmutables (no pueden
ser modificados una vez creados) de tipos diferentes:

**Sintaxis** 

nombre_tupla = (dato_1, datos_2, datos_3, ..., dato_n)




```python
mi_tupla = ("cadena de texto", 10, 3.1416, 'otra cadena de texo')
```

Se puede acceder a cada uno de los datos mediante su índice correspondiente, siendo 0 (cero), el índice del primer elemento.


```python
mi_tupla[0]
```




    'cadena de texto'



También se puede acceder a una porción de la tupla, indicando (opcionalmente) desde el índice de inicio hasta el índice de fin:


```python
mi_tupla[0:3] 
```




    ('cadena de texto', 10, 3.1416)




```python
mi_tupla[1:4]
```




    (10, 3.1416, 'otra cadena de texo')




```python
mi_tupla[2:]
```




    (3.1416, 'otra cadena de texo')




```python
mi_tupla[:2]
```




    ('cadena de texto', 10)



Otra forma de acceder a la tupla de forma inversa (de atrás hacia adelante), es colocando un índice negativo:


```python
mi_tupla[-1]
```




    'otra cadena de texo'




```python
mi_tupla[-2]
```




    3.1416



# Listas

Una lista es similar a una tupla con la diferencia fundamental de que permite modificar los
datos una vez creados. A diferencia de las tuplas, los datos en una lista van entre corchetes.

**Sintaxis**

Nombre_de_la_lista = [dato_1, dato_2, dato_3,...,dato_n]


```python
mi_lista = ["cadena de texto", 10, 3.1416, 'otra cadena de texo']
```

A las listas se accede igual que a las tuplas, por su número de índice:


```python
mi_lista[0]
```




    'cadena de texto'




```python
mi_lista[0:4]
```




    ['cadena de texto', 10, 3.1416, 'otra cadena de texo']




```python
mi_lista[-1]
```




    'otra cadena de texo'




```python
mi_lista[-2]
```




    3.1416




```python
mi_lista[-4]
```




    'cadena de texto'



Las lista NO son inmutables, permiten modificar los datos una vez creados.


```python
type(mi_lista)
```




    list




```python
mi_lista[0] = 500  # Se cambió el elemento 0, el cual es una cadena de texto, por un número, 500
```


```python
mi_lista
```




    [500, 10, 3.1416, 'otra cadena de texo']




```python
mi_lista.append("cadena de texto")  # La función append permite añadir otro elemento a una lista. 
```


```python
mi_lista
```




    [500, 10, 3.1416, 'otra cadena de texo', 'cadena de texto']



# Diccionarios

Mientras que a las listas y tuplas se accede solo y únicamente por un número de índice, los diccionarios permiten utilizar una clave para declarar y acceder a un valor.


```python
mi_diccionario = {'clave_1': (1,2,4), 'clave_2': [1,2,4],
                  'clave_3': 1, 'clave_4': 3.1416,
                  'clave_5': "Cadena de texto"}
```


```python
mi_diccionario["clave_1"]
```




    (1, 2, 4)




```python
mi_diccionario["clave_5"]
```




    'Cadena de texto'



Un diccionario permite eliminar cualquier entrada utilizando la función **del**.


```python
del(mi_diccionario["clave_2"])
```


```python
mi_diccionario
```




    {'clave_1': (1, 2, 4),
     'clave_3': 1,
     'clave_4': 3.1416,
     'clave_5': 'Cadena de texto'}



Al igual que las listas, el diccionario permite modificar los valores.


```python
mi_diccionario["clave_5"] = 500
```


```python
mi_diccionario
```




    {'clave_1': (1, 2, 4), 'clave_3': 1, 'clave_4': 3.1416, 'clave_5': 500}




```python

```
