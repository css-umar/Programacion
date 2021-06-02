---
layout: post
title:  "Estructuras de control condicionales"
date:   2021-05-31 16:40:39
categories: Estructuras
---

# Estructuras de control condicionales

Se definen mediante el uso de tres palabras claves:

**if** (si)

**elif** (sino, si)

**else** (sino)

Con las cuales se pueden construir las siguientes estructuras:

1. If simple:

> **Sintaxis**

>```
> if expresiones_logicas:
>     acciones_por_verdadero
>```

2. if else

> **Sintaxis**

>```
> if expresiones_logicas:
>     acciones_por_verdadero
> else:
>     aciones_por_falso   
>```

3. if elif else (anidado)

> **Sintaxis**

>```
> if expresiones_logicas:
>     acciones_por_verdadero
> elif expresiones_logicas:
>     aciones_por_falso
> else:
>     aciones_por_falso   
>```



### Ejemplo de la estructura: if else


```python
"""
Algoritmo Alumno
	Leer calificacion
	Si calificacion > 5.0  Entonces
		Escribir "Aprobado"
	SiNo
		Escribir "Reprobado"
	Fin Si
FinAlgoritmo
"""
calificacion= float(raw_input("Calificacion :")) 
if calificacion > 5.0:
    print ("Aprobado")
else:
    print("Reprobado")
```

### Ejemplo de la estructura: if elif else

![](https://github.com/css-umar/Programacion/blob/master/images/AlgoritmoAlumno.png)

```python
"""
Algoritmo Supermecado
	Leer compra
	Si compra <= 100 Entonces
		Escribir "Pago en efectivo"
	SiNo
		Si compra > 100 & compra <= 500 Entonces
			Escribir "Pago con tarjeta de debito"
		SiNo
			Escribir "Pago con tarjeta de credito"
		Fin Si		
	Fin Si
	
FinAlgoritmo
"""
compra = float(raw_input("Compra "))
if compra <= 100:
    print ("Pago en efectivo")
elif compra > 100 and compra < 300:
    print("Pago con tarjeta de debito")
else:
    print("Pago con tarjeta de credito")

```


```python

```

![](https://github.com/css-umar/Programacion/blob/master/images/AlgoritmoSupermercado.png)

### Ejemplo de la estructura: if 


```python
"""
Algoritmo Exento
	Leer parcial_1
	Leer parcial_2
	Leer parcial_3
	
	suma = parcial_1 + parcial_2 + parcial_3
	promedio = suma / 3
	
	Si promedio > 8.5  Entonces
		Escribir "Exento"
	Fin Si	
FinAlgoritmo
"""

parcial_1 = float(raw_input("Calificacion del parcial 1: "))
parcial_2 = float(raw_input("Calificacion del parcial 2: "))
parcial_3 = float(raw_input("Calificacion del parcial 3: "))

suma = parcial_1 + parcial_2 + parcial_3
promedio = suma / 3

if promedio > 8.5:
    print "Exento"
```

    Calificacion del parcial 1: 9
    Calificacion del parcial 2: 8
    Calificacion del parcial 3: 9
    Exento
    

![](https://github.com/css-umar/Programacion/blob/master/images/AlgoritmoExento.png)
