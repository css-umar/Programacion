---
layout: post
title:  "Introducción a la edición de texto en Google Colaboratory"
date:   2021-06-16 13:50:39
categories: Edición
---

# Cómo aprender a programar: Un método de cinco pasos

### Cristóbal Santos Santos

### 10 de septiembre de 2020

```
Nada es imposible para la persona que
no tiene que hacerlo.
Ley de Weiler
```
## 1. Introducción

En los últimos años el papel de la programación en la vida profesional de un ingeniero se ha vuelto muy importante porque la complejidad y diversidad de los problemas a los que se enfrenta es amplia. Imagínese todos los cálculos que se tuvieron que hacer para diseñar la presa de las tres gargantas en China; o simplemente, toda la información que se tuvo que analizar para que el Dr. López-Gatell todos los días a las 7:00 p.m informara el estado de
la pandemia por COVID-19. Detrás de estos logros seguramente hubo profesionistas que tuvieron que usar sus habilidades de programación para poder sacar avante estas actividades.

Saber programar permite agilizar tareas repetitivas, analizar datos (inspeccionar, limpiar y transformar) con el objetivo de resaltar información útil, resolver problemas que implican muchas operaciones, o bien, que contengan bastantes datos.

Indudablemente programar es una habilidad que todo profesionista requiere para realizar eficientemente sus labores; sin embargo, programar a muchos puede resultar una actividad difícil, pero ¿cuál es el motivo? Un error común es no tener una metodología apropiada para programar; otra causa, y posiblemente una consecuencia de la anterior, es pasar directamente a la computadora y empezar a escribir código sin entender el problema.

Comprender cómo cerrar la brecha entre cierta información inicial y la información deseada es importante, no solo para programar, sino para resolver cualquier otro problema.

## 2. ¿Cómo podemos aprender a programar?

Para aprender a programar debemos estar conscientes que esta actividad consta, entre otras <a id="footnote-1-ref" href="#footnote-1">[1]</a>., de las siguientes fases: i) entender el problema; ii) construir o implementar un algoritmo para resolver el problema; iii) traducir el algoritmo a un lenguaje de programación de computadora, para que ésta ejecute las instrucciones.

Es preciso recalcar que no se le puede dar indicaciones a la computadora, sin tener claros los pasos a seguir para resolver el problema. Por lo tanto, para programar, primero es necesario entender el problema para generar las ideas que permitan construir o implementar el algoritmo adecuado. Afortunadamente, el ser humano en su día a día implementa o construye algoritmos, sólo que por la cotidianidad no es consciente de ello.

En este escrito se propone un método para abordar las fases i) y ii) de una forma estructurada, y así poder implementar o construir un algoritmo que permita resolver un problema de la vida profesional. Pero antes, se analizará la similitud que existe entre resolver un problema de la vida cotidiana (algoritmos cotidianos) y uno de la vida profesional (algoritmo computacional).


### 2.1. Algoritmos informales

El ser humano sin darse cuenta, a diario aplica algoritmos informales[2] que le ayudan a resolver un problema, por ejemplo, cuando abre la puerta de su cuarto, o bien, cuando se lava las manos, o simplemente cuando prepara café. No presta atención a los detalles (pasos) al realizar estas actividades porque le son cotidianas; sin embargo, cuando se enfrenta a un nuevo problema, tiene que construir o implementar el algoritmo que lo resuelve, por ejemplo, aprender a manejar; para lograrlo, generalmente crea una secuencia, selección y repetición de acciones, resultado de aplicar una heurística basada en el uso del sentido común, experiencias con problemas similares, o simplemente por ensayo y error.

La secuencia, selección y repetición de acciones se logra gracias a que el pensamiento humano se mueve en estas tres estructuras básicas.

La primer estructura la desarrolla cuando proyecta alguna actividad, por ejemplo, la secuencia (orden) de acciones para cuando planea preparar café pueden ser:

1. Llenar la cafetera con agua.
2. Colocar seis cucharadas soperas de café en el filtro de la cafetera.
3. Encender la cafetera.

La segunda estructura (selección) la desarrolla cuando debe tomar una decisión, por ejemplo, cuando tiene que escoger entre café solo, con leche entera, deslactosada o light. La última estructura es la de ciclos de acciones, y posibilita tomar café todos los días a las 8:30 a.m, es decir, ayuda repetir una o varias acciones una cantidad repetida de veces.

Las estructuras mencionadas en el párrafo anterior se pueden expresar en forma de pseudocódigo (Ver PSEUDOCÓDIGO 2 y 3), el cual permiten escribir de una forma estructurada las acciones de los algoritmos.

En el PSEUDOCÓDIGO 1 se presenta un ejemplo de cómo se pueden aplicar las estructuras básicas para generar un algoritmo que permita tomar café.

```
El símbolo de numeral (#) indica que es un comentario que ayuda a entender el algoritmo.
Algoritmo para tomar café # Este es el nombre del algoritmo.
# Se coloca la palabra Inicio para indicar el inicio del algoritmo.
Inicio
# Aquí inician las acciones que permiten preparar el café.
# Las acciones se colocan en el orden preciso en que fueron
# planeadas es decir, la secuencia de ideas
Llenar la cafetera con agua
Colocar seis cucharadas soperas de café en el filtro
Encender la cafetera
# Aquí inicia una estructura de ciclo de acciones
Mientras la cafetera esté preparando el café Hacer
Leer las noticias
Fin Mientras
# Se utiliza la palabra Fin seguida del nombre de la estructura
# para indicar su finalización.
Apagar la cafetera
# Aquí finalizan las acciones que permiten preparar café.
# Aquí inician las acciones que permiten tomar café.
Servir café en taza favorita
# Aquí inicia otra estructura de ciclo de acciones Mientras.
Mientras la taza tenga café y el café esté caliente Hacer
Tomar sorbos de café
Leer las noticias
Fin Mientras
# Aquí finaliza la estructura de ciclo de acciones Mientras.
Fin
# Se coloca la palabra Fin para indicar el fin del algoritmo.
                                      PSEUDOCÓDIGO 1: Algoritmo para tomar café
```

Como se puede ver, por muy trivial que sea la actividad ¡A diario se está implementando o construyendo algoritmos informales! ¿Qué significa esto? Pues que continuamente el ser humano está añadiendo instrucciones (programando) a su cerebro, o bien, que utiliza instrucciones (programas) previamente añadidas para resolver problemas.

```
Si <condición> Entonces
Acciones
Si No
Acciones
Fin Si
                                      PSEUDOCÓDIGO 2: Estructura de selección en forma de sentencia.
```

```
Mientras <condición> Hacer
Acciones
Fin Mientras
                                      PSEUDOCÓDIGO 3: Estructura de repetición en forma de sentencia.
``` 
### 2.2. Algoritmos computacionales

Un algoritmo computacional utiliza las mismas estructuras básicas (secuencia, selección y re petición) que los informales, sin embargo, los problemas de la vida profesional son más complejos, porque para construir un algoritmo que pueda ser programado en una computadora,se requiere emplear un conjunto de conocimientos técnicos (física, matemáticas, estadística, etc.) y un análisis profundo para estructurar las acciones que permiten resolver el problema. Por lo tanto, es necesario una heurística más organizada que la utilizada para construir algoritmos informales.

### 2.3. Método de los cinco pasos

Como se comentó anteriormente, el objetivo de este escrito es presentar una estrategia que ayude en la fase de análisis del problema, y de construcción o implementación de un algoritmo. El método a seguir es el propuesto por Fogler y LeBlanc[4], éste consta de cinco pasos para resolver un problema genérico.


**Paso 1**: Definir el problema.
**Paso 2**: Generar posibles soluciones.
**Paso 3**: Decidir el curso de acción.
**Paso 4**: Implementar la solución.
**Paso 5**: Evaluar la solución.

Para entender el problema (**Fase I**), primero hay que definirlo (**Paso 1** de Flogler y Leblanc), es decir, saber en qué consiste el problema, con qué información se cuenta, qué información hace falta, qué restricciones presenta, identificar qué resultados se desean obtener, examinar si existen problemas similares.

El objetivo de la **Fase II** es obtener un algoritmo, es por ello que, entre más entendible quede el objetivo del problema, y más información se obtenga en la etapa anterior (**Paso 1**), hay más posibilidades de formular posibles soluciones (**Paso 2**) que permitan alcanzar el objetivo. El **Paso 3** consiste en seleccionar la mejor opción entre las posibles soluciones, para ello, se deben examinar los tiempos, conocimientos técnicos disponibles, infraestructura necesaria para llevar a cabo cada solución. En el **Paso 4** se lleva a cabo la planeación; aquí es donde se desarrolla la secuencia de pasos, de cómo se implementa la solución seleccionada. Se puede hacer uso de diagramas de flujo, o pseudocódigo para su representación. Para verificar la solución seleccionada (**Paso 5**) se puede hacer uso de pruebas de escritorio, las cuales consisten en seguir las instrucciones e ir generando tablas de datos con las variables que tiene el algoritmo. Esto permite detectar errores y omisiones.

Si la solución evaluada no es aceptable, entonces regresamos al **Paso 2** y seleccionamos otra de la lista. Por el contrario, si la solución es correcta, entonces se tiene un algoritmo, no obstante, seguramente más de una solución propuesta arrojará resultados satisfactorios; y por lo tanto, algoritmos diferentes. Encontrar el algoritmo óptimo está fuera del alcance de este documento.

A continuación se presenta un ejemplo sencillo para aplicar los cinco pasos <a id="footnote-2-ref" href="#footnote-2">[2]</a>.

Se desea encontrar el mínimo de la función $$f(x) =x^2$$ para cuando $$− 5 \leq x \leq 5$$.

**Paso 1:** Definir el problema a resolver

Para definir cuál es la situación actual y poder visualizar el objetivo del problema (estado final), en este paso se tiene que:

> 1. Analizar la información proporcionada: se sabe que la función es del tipo cuadrática $$(ax^2 +bx+c= 0)$$ con $$a= 1$$, $$b$$ y $$c$$ igual con cero. Su gráfica es una parábola que abre hacia arriba porque $a \geq 0$, además para funciones del tipo $f(x) =ax^2$ el vértice está en el origen.

> 2. Restricciones: la búsqueda del mínimo de la función se restringe al intervalo $$− 5 \leq x \leq 5$$.
> 3. Buscar información complementaria. Por ejemplo:
>> + Conceptos relevantes.
>>> + Mínimo: Valor más pequeño que acepta o puede tomar una variable[1].
>>> + Vértice de una parábola: es el punto más bajo o más alto en una parábola.
>> + Algoritmos: Verificar si ya existen algoritmos para resolver problemas de este tipo.
>>> + Aplicar el teorema sobre el valor máximo o mínimo de una función cuadrática[3].


**¿Cuál es el objetivo?** Es importante que el objetivo del problema quede exento de ambigüedades.

El objetivo es encontrar el valor mínimo que toma en específico la función cuadrática $$f(x)= x^2$$ en el intervalo $$− 5 \leq x \leq 5$$.

**Paso 2**: Generar posibles soluciones

Las ideas van a depender, tanto del conocimiento técnico del programador, como de la in formación recabada en el **Paso 1**. Se pueden plantear cuatro posibles soluciones, aunque seguramente existan más:

> **Solución 1**: Encontrar el valor mínimo por comparación de los valores que toma la función en el intervalo $$− 5 \leq x \leq 5$$.

> **Solución 2**: Aplicar el teorema sobre el valor máximo o mínimo de una función cuadrática:

>> Si $$f(x) =ax^2 +bx+c$$, donde $$a=0$$, entonces $$f(−b/ 2 a)$$ es

>>> el valor máximo de $$f$$ si $$a < 0$$

>>> el valor mínimo de $$f$$ si $$a > 0$$

> **Solución 3**: Aplicar los conceptos de cálculo diferencial (cálculo de extremos locales) para encontrar el mínimo de la función.

> **Solución 4**: Se sabe que para funciones del tipo $$f(x) =ax^2$$ el vértice (punto más altoo más bajo de una parábola) está en el origen.

**Paso 3**: Decidir el curso de acción

Si se elige la **Solución 1, 2** o **4** existe la posibilidad de que esa solución sólo sea válida para ese problema en particular. Por el contrario, la **Solución 3** es válida para cualquier función en una variable, pero se requiere de más conocimientos de cálculo diferencial y de más pasos (Ver Tabla 4). ¡Ojo! No se debe perder de vista el objetivo del problema, están pidiendo el mínimo de una función, en específico de $$f(x) =x^2$$. Por lo tanto, por rapidez y sencillez es más viable aplicar el teorema sobre el valor máximo o mínimo de una función cuadrática (**Solución 2**, Ver Tabla 3), o bien,la **Solución 4** (Tabla 5). Es más, se puede observar en la Tabla 5 que la **Solución 4** o requiere hacer ningún cálculo para hallar el mínimo de la función, la solución al problema es conceptual.

Paso 4: Implementar la solución

Suponiendo que se desconoce la **Solución 4** (¡pero no la olvide!), y que se optó por la **Solución 2**; los pasos para implementar esta solución están en el Pseudocódigo 4 y en forma de diagrama de flujo en la Figura 1 respectivamente.

Paso 5: Evaluar la solución

La prueba de escritorio para la Solución 2 se muestra en la Tabla 1. En dicha tabla se observa que el mínimo de la función $$f(x) =x^2$$ se encuentra, como es de esperarse, en el origen. Por lo tanto, la **Solución 2** es un algoritmo que permite encontrar el mínimo de una función del tipo $$f(x) =ax^2$$, siempre y cuando $a > 0$.

Retomando la **Solución 4**, si se hubiese escogido esa solución, no se requiere hacer cálculo alguno para obtener el mínimo de $$f(x) =x^2$$ porque para cualquier función cuadrática de la forma $$f(x) =ax^2$$ con $$a > 0$$ el mínimo está en el origen.


![Figura 1: Diagrama de flujo de la Solución 2.](https://github.com/css-umar/Programacion/blob/master/images/Solucion2.png)

```
Algoritmo Solución 2
Inicio
Leer a
Leer b
Si a > 0 Entonces
xv <- -b/(2*a)
fxv <- xv^
Escribir "El mínimo de fx es"
Escribir fxv
Escribir "El mínimo está en"
Escribir xv
Si No
xv <- -b/(2*a)
fxv <- xv^
Escribir "El máximo de fx es"
Escribir fxv
Escribir "El máximo está en"
Escribir xv
Fin Si
Fin
                                      PSEUDOCÓDIGO 4: Algoritmo Solución 2.
```
2.3.1. ¿Qué sigue?

Ahora toca traducir la planeación (pseudocódigo o diagrama de flujo) a un lenguaje que la computadora pueda interpretar, pero ¿cuál lenguaje? Un lenguaje de programación cuya elección depende del tipo de problema que se esté resolviendo. Existen lenguajes de programación enfocados al desarrollo de aplicaciones web, a base de datos, a videojuegos, al cálculo científico, y otros que son de propósito general.

En ingeniería, la mayoría de los problemas que hay que resolver involucran cálculos, por lo tanto, se debe optar por uno que esté enfocado al cálculo científico, por ejemplo Matlab, Mathematica, S-Plus, Octave, Scilab, Maxima, R, Julia, Python, Fortran, etc. La elección de uno u otro, dependerá en principio del capital con que se cuente; Matlab, Mathematica y S-Plus son costosos, los restantes son Software Libre<a id="footnote-3-ref" href="#footnote-3">[3]</a> por lo que resultan una buena opción para la docencia porque el alumno puede hacer uso de él sin tener que pagar.

Otra ventaja que presentan algunos de estos Software Libres es que se pueden trabajar en la nube, como es el caso de Octave<a id="footnote-4-ref" href="#footnote-4">[4]</a>, R<a id="footnote-5-ref" href="#footnote-5">[5]</a> , Python<a id="footnote-6-ref" href="#footnote-6">[6]</a> y Scilab<a id="footnote-7-ref" href="#footnote-7">[7]</a>. La mejor elección es aquella que se adapte a las necesidades para resolver el problema.

## 3. Conclusiones

La metodología propuesta permite, desde un inicio, enfocarse en la comprensión del problema, no en el código. Además, fomenta la creatividad para generar alternativas de solución; promueve el pensamiento analítico cuando se escoge la solución más viable al problema. Asimismo, ayuda a adquirir buenos hábitos de resolución de problemas.

Es importante que la materia de Programación se imparta en el primer año de la carrera, porque aprender a programar es aprender a pensar, a analizar, a estructurar ideas. Habilidades que serán útiles al alumno en las demás materias, y que posiblemente le permitirán ahorrar tiempo y frustraciones.

Básicamente la idea es convertir este método en un hábito cada vez que se vaya, no solamente a programar, si no a resolver un problema de cualquier otra materia.


```
El primer 10 % de la tarea requiere el
90 % del tiempo. El 90 % restante ocupa
el 10 % que queda.
Ley 90/
```

## 4. Anexo: Tablas

<table class="egt">
  <caption>Tabla 1: Prueba de escritorio para la Solución 2</caption>
  <tr><th scope="col">Instrucción</th><th>Condición</th><th>a </th><th>b </th><th>$x_v$ </th><th>$f(x_v)$ </th><th>Pantalla               </th></tr>
  <tr><th>Leer a                 </th><td>         </td><td>1 </td><td>  </td><td>      </td><td>         </td><td>                       </td></tr>
  <tr><th>Leer b                 </th><td>         </td><td>  </td><td>0 </td><td>      </td><td>         </td><td>                       </td></tr>
  <tr><th> a>0                   </th><td>Sí       </td><td>  </td><td>  </td><td>      </td><td>         </td><td>                       </td></tr>
  <tr><th> $x_v = -b/2a$         </th><td>         </td><td>  </td><td>  </td><td>0     </td><td>         </td><td>                       </td></tr>
  <tr><th> $f(x_v)$              </th><td>         </td><td>  </td><td>  </td><td>0     </td><td>         </td><td>                       </td></tr>
  <tr><th> El mínimo de $f(x)$ es</th><td>         </td><td>  </td><td>  </td><td>      </td><td>         </td><td>El mínimo de $f(x)$ es </td></tr>
  <tr><th> Escribir $f(x)$       </th><td>         </td><td>  </td><td>  </td><td>      </td><td>         </td><td>0                      </td></tr>
  <tr><th> El mínimo está en     </th><td>         </td><td>  </td><td>  </td><td>      </td><td>         </td><td>El mínimo está en      </td></tr>
  <tr><th> Escribir $x_v$        </th><td>         </td><td>  </td><td>  </td><td>      </td><td>         </td><td>0                      </td></tr>
</table>


<table class="egt">
  <caption>Tabla 2: Paso para implementar la Solución 1.</caption>
  <tr><td>Paso 1</td><td>Evaluar $f(x)=x^2$ en cada uno de los elementos del intervalo $-5\leq x \leq 5$.</td></tr>
  <tr><td>Paso 2</td><td>Ordenar de menor a mayor el valor que tomó $f(x)=x^2$ en el Paso 1. </td></tr>
  <tr><td>Paso 3</td><td>Seleccionar el menor valor como el mínimo de la función. </td></tr>
</table>

<table class="egt">
  <caption>Tabla 3: Paso para implementar la Solución 2.</caption>
  <tr><td>Paso 1</td><td>Calcular $x_v = -b/2a$.</td></tr>
  <tr><td>Paso 2</td><td>Evaluar $f(x_v)$. </td></tr>
  <tr><td>Paso 3</td><td>Si $a>0$ la función tiene un mínimo en $x_v$</td></tr>
  <tr><td>Paso 4</td><td>Si $a<0$ la función tiene un máximo en $x_v$</td></tr>
</table>

<table class="egt">
  <caption>Tabla 4: Paso para implementar la Solución 3.</caption>
  <tr><td>Paso 1</td><td>Hallar la primera derivada de $f(x)$.</td></tr>
  <tr><td>Paso 2</td><td>Hallar la segundaa derivada de $f(x)$.</td></tr>
  <tr><td>Paso 3</td><td>Hacer $f^'(x)=0$</td></tr>
  <tr><td>Paso 4</td><td>Resolver para la variable independiente $x$</td></tr>
  <tr><td>Paso 5</td><td>Evaluar $f^{''}(x)$ en las raíces obtenidas en el Paso 4.</td></tr>
  <tr><td>(a):</td><td>Si $f^{''}(x)>0$ la función tienen un mínimo en $m(x_i,f(x_i))$</td></tr>
  <tr><td>(b):</td><td>Si $f^{''}(x)<0$ la función tienen un máximo en $M(x_i,f(x_i))$</td></tr>
</table>

<table class="egt">
  <caption>Tabla 5: Paso para implementar la Solución 4.</caption>
  <tr><td>Paso 1</td><td>El vértice para ecuaciones cuadráticas de la forma $f(x)=ax^2$ con $a>0$ están en el origen.</td></tr>
</table>


## Notas
<p id="footnote-1">
   1. La programación es sólo una etapa del proceso de desarrollo de un programa informático.<a href="#footnote-1-ref">&#8617;</a> 
</p>

<p id="footnote-2">
   2. Aquí se están simplificando cada uno de los pasos. Para mayor detalle de las acciones y técnicas que involucra cada paso se recomienda consultar H.S. Fogler y S.E. LeBlanc, Strategies for Creative Problem Solving, Prentice-Hall, Englewood Cliffs, NJ, 1994.<a href="#footnote-2-ref">&#8617;</a> 
</p>

<p id="footnote-3">
   3. Significa libertad de usar, estudiar, distribuir y mejorar.<a href="#footnote-3-ref">&#8617;</a> 
</p>

<p id="footnote-4">
   4. https://octave-online.net/<a href="#footnote-4-ref">&#8617;</a> 
</p>

<p id="footnote-5">
   5. https://rstudio.cloud/<a href="#footnote-5-ref">&#8617;</a> 
</p>

<p id="footnote-6">
   6. colab.research.google.com <a href="#footnote-6-ref">&#8617;</a> 
</p>

<p id="footnote-7">
   7. https://cloud.scilab.in/ <a href="#footnote-7-ref">&#8617;</a> 
</p>

## Referencias

[1] Efraın Soto Apolinar.Diccionario Ilustrado de Conceptos Matemáticos. México: [http://www.aprendematematicas.org.mx](http://www.aprendematematicas.org.mx), 2011.

[2] Omar Iván Trejos Buriticá. Lógica de Programación. Ediciones de la U, 2017.ISBN:
9789587627206.

[3] Jeffery A Cole y col.Álgebra y Trigonometría con Geometría Analítica. Cengage Learning Editores, 2011.

[4] H.Scott Fogler y Steven E. Le Blanc. Strategies for Creative Problem Solving. Prentice Hall, 1994.ISBN: 9780130082794.
