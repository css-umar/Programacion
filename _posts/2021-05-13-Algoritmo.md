---
layout: post
title:  "Algoritmo"
date:   2021-05-13 16:40:39
categories: Programación
---

# Algoritmo

Es un método general de resolución, que consiste en un **_conjunto ordenado y finito de instrucciones_**, para resolver problemas del mismo tipo. 

> + Al conjunto ordenado y finito de instrucciones se le llama **_sentencia_**. 
> + Una sentencia es una combinación de palabras, variables, constantes y símbolos que al ser traducido por un lenguaje de programación a lenguaje maquina, son utilizados por ésta para realizar el conjunto de sentencias que componen el algoritmo.

## Ejemplo: algoritmo de la solución general de ecuaciones de segundo grado $$Ax^2+Bx+C=0$$

Para una ecuación cuadrática con coeficientes reales existen siempre dos soluciones, no necesariamente distintas, llamadas raíces, que pueden ser reales o complejas. 

Fórmula general para la obtención de raíces:

$$x=\dfrac{-B\pm\sqrt{B^2-4\,A\,C}}{2\,A}  $$

### Pseudocódigo 

```
Algoritmo Chicharronera
	Escribir "Ingrese A,B, y C"
	Leer A, B, C
	Disc<-B^2-(4*A*C)
	Si Disc = 0 Entonces
		x<-B/(2*A)
	SiNo
		Si Disc > 0 Entonces
			x1=(-B-RC(Disc))/(2*A)
			x2=(-B+RC(Disc))/(2*A)
			Escribir "Tiene soluciones reales"
			Escribir x1,x2
		SiNo
			Escribir "Tiene soluciones complejas"			
		Fin Si
	Fin Si	
FinAlgoritmo
```
### Diagrama de flujo

<img src="https://github.com/css-umar/Programacion/blob/master/images/AlgoritmoChicahrronera.png?raw=true" width="70%">


### Código python

```python
from math import sqrt

print "Ingrese A,B, y C"
A = float(raw_input())
B = float(raw_input())
C = float(raw_input())
disc = B**2-(4*A*C)
if disc==0:
    x = B/(2*A)
	else:
             
		if disc>0:
            x1 = (-B-sqrt(disc))/(2*A)
			x2 = (-B+sqrt(disc))/(2*A)
			print "Tiene soluciones reales"
			print x1,x2
		else:
			print "Tiene soluciones complejas"
```





