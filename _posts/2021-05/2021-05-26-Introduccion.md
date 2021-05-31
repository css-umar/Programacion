---
layout: post
title:  "Introduccion"
date:   2021-05-26 13:50:39
categories: jekyll
---



# Introducción a la edición de texto en Google Colab

El texto en Google Colab se maneja en código _Markdown, Latex_ y _html_.

## Edicción de texto

Para escribir texto en negritas, se encierra el texto entre dobles asteriscos `**texto**`.

El siguiente código _Markdown_

```
**Este es un texto en negritas**
```

arroja:

**Este es un texto en negritas**

Para escribir texto en cursivas, se encierra el texto entre asteriscos `*texto*` o entre guiones bajos `_texto_`.

El siguiente código _Markdown_

```
*Este un texto en cursiva*
_Este un texto en cursiva_
```
arroja:

*Este un texto en cursiva*

_Este en un texto en cursiva_

Para crear un texto que combine fuentes cursivas y negritas, el texto se encierra en entre dobles asteriscos y entre guiones bajos (``**_texto_**``).

El siguiente código _Markdown_

```
**_Este un texto en negrita y cursiva_**
```
arroja:

**_Este un texto en negrita y cursiva_**

### Superíndice y subíndice

Para escribir texto en _superíndice y subíndice_ se usa código _html_. 

+ Para superíndice, se usa el siguiente código `<sup>texto<\sup>`
+ Para subíndice, se usa el siguiente código `<sub>texto<\sub>`

**Ejemplo**

La fórmula del agua se escribe con el siguiente código

```html
H<sub>2</sub>O
```
el cual arroja el siguiente resultado: H<sub>2</sub>O

**Otro ejemplo**

La fórmula del peróxido de hidrógeno se obtiene con el siguiente código html

```html
H<sub>2</sub>O<sub>2</sub>
```

el resultado es H<sub>2</sub>O<sub>2</sub>.

**Uno ejemplo más**

Para escribir X elevado a potencia 2, se usa el siguiente código html

```html
X<sup>2</sup>
```
el resultado es X<sup>2</sup>.

## Listas 

### Listas numeradas

Para crear listas númeradas se usan simplemente números. 

El siguiente código _Markdown_

```
1. Elemento 1
2. Elemento 2
3. Elemento 3
```

arroja la lista numerada:

1. Elemento 1
2. Elemento 2
3. Elemento 3

### Listas con viñetas

Para crear listas con viñetas se usa el símbolo de suma (+)

El siguiente código _Markdown_

```
+. Elemento 1
+. Elemento 2
+. Elemento 3
```
arroja la siguiente lista con viñetas:

+ Elemento 1
+ Elemento 2
+ Elemento 3

### Listas anidadas

Para crear listas anidadas se usa el símbolo de mayor que (>).

El siguiente código _Markdown_

```
+ Elemento 1
> + Elemento 1.1
>> + Elemento 1.1.1
>> + Elemento 1.1.2
>> + Elemento 1.1.3
> + Elemento 1.2
> + Elemento 1.3
+ Elemento 2
> + Elemento 2.1
> + Elemento 2.2
> + Elemento 2.3
+ Elemento 3
```

arroja la siguiente lista anidada:


+ Elemento 1
> + Elemento 1.1
>> + Elemento 1.1.1
>> + Elemento 1.1.2
>> + Elemento 1.1.3
> + Elemento 1.2
> + Elemento 1.3
+ Elemento 2
> + Elemento 2.1
> + Elemento 2.2
> + Elemento 2.3
+ Elemento 3

## Creación de listas usando código html

### Listas ordenadas personalizadas 

Se usa el siguiente código hmtl

```html
<ol type="Opcion">
  <li>Elemento 1</li>
  <li>Elemento 2</li>
  <li>Elemento 3</li>
  <li>Elemento 4</li>
  <li>Elemento 5</li>
</ol>
```
Donde *type = opción* puede ser:
+ type = "1", para listas decimales
+ type = "a", para listas alfabéticas en minúsculas
+ type = "A", para listas alfabéticas en mayúsculas
+ type = "i", para listas en romanos minúsculas
+ type = "I", para listas en romanos mayúsculas.

**Ejemplo**

El siguiente código muestra una lista con números.

```html
<ol type="1">
  <li>Julio</li>
  <li>Carmen</li>
  <li>Ignacio</li>
  <li>Elena</li>
  <li>America</li>
</ol>
```
<ol type="1">
  <li>Julio</li>
  <li>Carmen</li>
  <li>Ignacio</li>
  <li>Elena</li>
  <li>America</li>
</ol>

El siguiente código muestra una lista con letras mayúsculas.
```html
<ol type="A">
  <li>Julio</li>
  <li>Carmen</li>
  <li>Ignacio</li>
  <li>Elena</li>
</ol>
```
<ol type="A">
  <li>Julio</li>
  <li>Carmen</li>
  <li>Ignacio</li>
  <li>Elena</li>
</ol>

### Lista de definiciones

Se usa el siguiente código hmtl:

```html
<dl>
  <dt>Palabra 1</dt>
  <dd>Definición de Palabra 1</dd>
  <dt>Palabra 2</dt>
  <dd>Definición de Palabra 2</dd>
  <dt>Palabra 3</dt>
  <dd>Definición de Palabra 3</dd>
  <dt>Palabra 4</dt>
  <dd>Definición de Palabra 4</dd>
</dl>
```

**Ejemplo**

El siguiente código muestra una lista de definiciónes

```html
<dl>
  <dt>Pizpireta</dt>
  <dd>Dicho de una mujer: Viva, pronta y aguda.</dd>
  <dt>Polular</dt>
  <dd>Dicho de las personas, animales o cosas: Abundar y bullir en un lugar.</dd>
  <dt>Concupiscencia</dt>
  <dd>En la moral católica, deseo de bienes terrenos y, en especial, apetito desordenado de placeres deshonestos.</dd>
</dl>
```

El resultado es

<dl>
  <dt>Pizpireta</dt>
  <dd>Dicho de una mujer: Viva, pronta y aguda.</dd>
  <dt>Polular</dt>
  <dd>Dicho de las personas, animales o cosas: Abundar y bullir en un lugar.</dd>
  <dt>Concupiscencia</dt>
  <dd>En la moral católica, deseo de bienes terrenos y, en especial, apetito desordenado de placeres deshonestos.</dd>
</dl>

## Edición de ecuaciones 

Para editar ecuaciones se usa código _Latex_. Existen dos formas en las cuales se pueden presentar las ecuaciones en Google colab, a saber:

+ Modo linea: 
> Para usar modo linea, el código _Latex_ se encierra entre signos de pesos `$fórmula$`.
+ Modo presentación: 
> Para usar modo presentación, el código _Latex_ se encierra entre dos signos de pesos `$$fórmula $$`.

**Ejemplo**:

La ecuación más famosa de Albert Einstein es $$E = mc^2$$ (`$E = mc^2$`), la ecuación de la relatividad.

La fórmula general para resolver ecuaciones del tipo $$aX^2+bX + c$$(`$aX^2+bX + c$`) es:

$$x = \dfrac{-b\pm\sqrt{b^2-4ac}}{2a}$$

`$$x = \dfrac{-b\pm\sqrt{b^2-4ac}}{2a}$$`

Consulte [Overleaf](https://es.overleaf.com/learn/latex/Mathematical_expressions) para mayores detalles de cómo editar expresiones matemáticas.

### Edición de ecuaciones químicas

Para escribir ecuaciones químicas se usa estilo de fuente _mathrm_ dentro código _Latex_.

**Ejemplo**

El siguiente código _Latex_

```latex
$$\mathrm{H_2O\rightleftarrows H_2 + \frac{1}{2}O_2}$$
$$\mathrm{CH_4 + 2\,O_2\rightarrow CO_2 + 2\,H_2O}$$
```
muestra las reacciones químicas

$$\mathrm{H_2O\rightleftarrows H_2 + \frac{1}{2}O_2}$$

$$\mathrm{CH_4 + 2\,O_2\rightarrow CO_2 + 2\,H_2O}$$


También funciona en modo linea, por ejemplo, la fórmula del agua es $$\mathrm{H_2O}$$.

## Edición de tablas

Para crear tablas, los campos (celdas) y cabeceras se separan con una barra vertical |.

El siguiente código _Markdown_

```
Cabecera 1 | Cabecera 2
---        | ---
Celda 1,1  | Celda 1,2
Celda 2,1  | Celda 2,2
```

muestra la siguiente tabla:

Cabecera 1 | Cabecera 2
---        | ---
Celda 1,1  | Celda 1,2
Celda 2,1  | Celda 2,2

### Alineación de texto en tablas

La alineación de texto en cada columna se hace mediante la adición de dos puntos a las líneas de separación.
+ Dos puntos a la izquierda de la línea punteada (`:---`) hará que la columna esté alineada a la izquierda.
+ Dos puntos a la derecha de la línea punteada (`---:`) hará que la columna esté alineada a la derecha.
+ Dos puntos en ambos lados de la línea punteada (`:---:`) significa que la columna se alinea al centro.

El siguiente código _Markdown_

```
Cabecera 1                     | Cabecera 2      | Cabecera 3
:---                           | :---:           | ---:
Texto alineado a la izquierda  | Texto centrado  | Texto alinaeado a la derecha
Celda 2,1                      | Celda 2,2       | Celda 2,3
Celda 3,1                      | Celda 3,2       | Celda 3,3
```

muestra la siguiente tabla:

Cabecera 1                     | Cabecera 2      | Cabecera 3
:---                           | :---:           | ---:
Texto alineado a la izquierda  | Texto centrado  | Texto alinaeado a la derecha
Celda 2,1                      | Celda 2,2       | Celda 2,3
Celda 3,1                      | Celda 3,2       | Celda 3,3

### Fórmulas matemáticas y químicas en tablas

Para escribir fórmulas matemáticas y químicas dentro de tablas, se usa el modo en linea para representar ecuaciones en _Latex_.

El siguiente código _Markdown_

```
Fórmula química | Fórmula matemática
---             | ---
$\mathrm{H_2O}$   |$E = mc^2$
```

muestra la siguiente tabla con fórmulas químicas y matemáticas:

|Fórmula química | Fórmula matemática|
|---             | ---|
|$$\mathrm{H_2O}$$ | $$E = mc^2$$|

### Tablas usando código html

#### Tablas por filas

Se usa el siguiente código html
 
 ```html
 <table class="egt">
  <tr><td>Fila 1</td><td>Elemento 1 Fila 1</td><td>Elemento 2 Fila 1</td><td>Elemento 3 Fila 1</td></tr>
  <tr><td>Fila 2</td><td>Elemento 1 Fila 2</td><td>Elemento 2 Fila 2</td><td>Elemento 3 Fila 2</td></tr>
</table>
 ```

 El resultado del código anterior es:

 <table class="egt">
  <tr><td>Fila 1</td><td>Elemento 1 Fila 1</td><td>Elemento 2 Fila 1</td><td>Elemento 3 Fila 1</td></tr>
  <tr><td>Fila 2</td><td>Elemento 1 Fila 2</td><td>Elemento 2 Fila 2</td><td>Elemento 3 Fila 2</td></tr>
</table>

**Ejemplo**


```html
<table class="egt">
  <tr><td>Tiempo $t(s)$</td> <td>$15$</td><td>20</td><td>22</td></tr>
  <tr><td>Velocidad $v(m/s)$</td><td>365</td><td>520</td><td>600</td></tr>
</table>
```

<table class="egt">
  <tr><td>Tiempo $$t(s)$$</td> <td>$15$</td><td>20</td><td>22</td></tr>
  <tr><td>Velocidad $$v(m/s)$$</td><td>365</td><td>520</td><td>600</td></tr>
</table>

#### Tablas encabezado

Para generar tablas con encabezado, se usa el siguiente código:

```html
<table>
  <tr>
    <th>Cabecera 1</th>
    <th>Cabecera 2</th>
    <th>Cabecera 3</th>
  </tr>
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
  </tr>
</table>
```
el cual arrroja la tabla que se muestra a continuación

<table>
  <tr>
    <th>Cabecera 1</th>
    <th>Cabecera 2</th>
    <th>Cabecera 3</th>
  </tr>
  <tr>
    <td>Fila 1 Columna 1</td>
    <td>Fila 1 Columna 2</td>
    <td>Fila 1 Columna 3</td>
  </tr>
</table>

#### Tablas con título
Para generar tablas con título, se usa el siguiente código:

```html
<table class="egt">
  <caption>Título de la tabla</caption>
  <tr><th scope="col">Cabecera 1</th><th>Cabecera 2</th><th>Cabecera 3</th><th>Cabecera 4</th></tr>
  <tr><th>Celda 1,1</th><td>Celda 1,2</td><td>Celda 1,3</td><td>Celda 1,4</td></tr>
  <tr><th>Celda 2,1</th><td>Celda 2,2</td><td>Celda 2,3</td><td>Celda 2,4</td></tr>
</table>
```
el cual arrroja la tabla que se muestra a continuación

<table class="egt">
  <caption>Título de la tabla</caption>
  <tr><th scope="col">Cabecera 1</th><th>Cabecera 2</th><th>Cabecera 3</th><th>Cabecera 4</th></tr>
  <tr><th>Celda 1,1</th><td>Celda 1,2</td><td>Celda 1,3</td><td>Celda 1,4</td></tr>
  <tr><th>Celda 2,1</th><td>Celda 2,2</td><td>Celda 2,3</td><td>Celda 2,4</td></tr>
</table>

## Inserción de imágenes

### Desde _Google drive_

Se usan los siguientes pasos:

**Paso 1**: Dirigirse a la carpeta en _Google drive_ donde se desea subir la imágen.

**Paso 2**: Subir al _Google drive_ la imágen que se desea insertar.

**Paso 3**: Seleccionar la imágen con el botón derecho del mouse. Se abrirá un menú.

**Paso 4**: Seleccionar la opción _Obtener vínculo_.

**Paso 5**: Cambiar la opción de _Restringido_ a _Cualquier personal que tenga el vínculo_.

**Paso 6**:  Dar clic a _Copiar vínculo_.

**Paso 7**: Pegar el vínculo en un editor de texto. El vículo tendrá una forma similar al siguiente ejemplo

`https://drive.google.com/file/d/1YCaUgY5ziIR_P7DGoXwx-_Epqfdk--QY/view?usp=sharing`

**Paso 8**: Del vínculo pegado, seleccionar y copiar el texto entre `https://drive.google.com/file/d/` hasta `/view?usp=sharing`

**Paso 9**: Se obtendrá un _código_ como el siguiente `1YCaUgY5ziIR_P7DGoXwx-_Epqfdk--QY`

**Paso 10**: El código obtenido en el paso anterior se reemplaza por la palabra código en 

```html
<img src="https://drive.google.com/uc?id=código&export=download" width="70%">
```
Quedando de la forma siguiente

```html
<img src="https://drive.google.com/uc?id=1YCaUgY5ziIR_P7DGoXwx-_Epqfdk--QY&export=download" width="40%">
```
El resultado obtenido es el siguiente:

<img src="https://drive.google.com/uc?id=1YCaUgY5ziIR_P7DGoXwx-_Epqfdk--QY&export=download" width="40%">

**Paso 11**: Para cambiar el tamaño de la imagen, hay que modificar el valor de `width = "valor"` al que usted desee.

### Desde la web

Se usan los siguientes pasos:

**Paso 1**: Buscar la imágen en la web.

**Paso 2**: Selecionar con el botón derecho del mouse la imagen deseada. se abrirá un menú.

**Paso 3**: Seleccionar _Copiar dirección de imagen_. 

**Paso 4**: Reemplazar en el siguiete código _html_ la palabra vínculo con dirección obtenida en el **Paso 3**. La dirección cotiene un código muy extenso. ¡No se preocupe!

```html
![](vínculo)
```
**Ejemplo**

```html
![](data:image/jpeg;base64,/9j/4AAQSkZJRgABAQAAAQABAAD/2wCEAAkGBxIREA8QEBATFRAVEQ8VEA8XFRUQFQ8RFhIWFxURFRUYHSggGBolGxgVJTEhJSkrLi8uFx8zODMsOCgtLisBCgoKDg0OGxAQGi8lICYtMCstLS0tLS0tLzUtLi0tNS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS0tLS8tLS0tLf/AABEIAOEA4QMBEQACEQEDEQH/xAAcAAEAAgMBAQEAAAAAAAAAAAAABAUBAwYHAgj/xABREAABAgMBCggICggF...UQEhksAgNwaAgMoAgCAIAgCAIAgCAIAgCAIAgCAwQgMGGMyA+TAbmQHzxZuZAY4q3MgHFW5kBnizcyA+hAbmQGRDGZAfQCAygCAIAgCAIAgCAIAgCAIAgCAIAgCAIAgCAIAgCAIAgCAIAgCAIAgCAIAgCAIAgCAID//2Q==)
```
