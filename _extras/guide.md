---
layout: page
title: "Instructor Notes"
---

## Workshop Structure

This Workshop is divided in 3 lessons: 
1. Introduction to Bash.    
2. Introduction to Python.      
3. Pangenome Analysis in Prokaryotes.  

The sixteen hours workshop workshop is designed for a whole weekend. Nevertheless 
it could be used as a reference manual for students learning pangenomics or TDA.
Lesson is divided in an introduction to pangenome analysis 
and some topological data analysis episodes.

<a href="{{ page.root }}/fig/01-01-01.png">
   <img src="{{ page.root }}/fig/PanWorkshopWorkflow.png" alt=" Venn diagram of a) a closed pangenome and b) an open pangenome, comparing the sizes of their core and accessory genomes. c) Graphic depicting the differences between closed and open pangenomes regarding their size, total genes in pangenome, and the number of sequenced genomes." />
  </a>
  
# General notes for the whole workshop

## Technical tips and tricks

The parent directory of everything that we will be using during the lesson is `/home/dcuser/dc_workshop`❓. At the beginning of the workshop make sure it looks like this: 

FIXME: `tree` command of the `dc_workshop`❓ folder. 💢

## Slides
Here you can find a set of [slides](https://docs.google.com/presentation/d/1MYsxgJ8rOu4cmGQw4S9EXcRtvd8CNNlEtgzbeuBiJgE/edit#slide=id.p)
with the figures of the lesson.  
## Installation

This workshop is designed to be run on pre-imaged Amazon Web Services (AWS) instances. See the 
[Setup page](https://czirion.github.io/comparative-genomics-workshop/setup.html) for complete setup instructions. If you are
teaching these lessons, and would like an AWS instance to practice on, please contact [team@carpentries.org](mailto: team@carpentries.org).

## Common problems

✳️
This workshop introduces an analysis pipeline, where each step in that pipeline is dependent on the previous step.
If a learner gets behind, or one of the steps doesn't work for them, they may not be able to catch up with the rest of the class. 
To help ensure that all learners are able to work through the whole process, we provide the solution files. This includes all
of the output files for each step in the data processing pipeline, as well as the scripts that the learners write collaboratively
with the Instructors throughout the workshop. These files are available on the hidden `.backup_dc_workshop`directory.

Make sure to tell your helpers about the `.backup_dc_workshop` directory so that they can use these resources to help
learners catch up during the workshop. 
# Notes for the Workshop
The tree of the directories whe you download the data should look like:

If you are teaching the lesson with the CCM-UNAM server you can use this [spreadsheet](https://docs.google.com/spreadsheets/d/1uiBMjlIh3U5JufVoDl9BTncHPCmYm9GT-LHUkOwWnnU/edit#gid=0) to ask the participants to choose their user:

# Notes for the Pangenome Analysis in Prokaryotes lesson

FIXME: Add 💢

# Developement guidelines

## Formato de los encabezados y del texto

### Formato de los encabezados (El anterior es un encabezado nivel 2 y este es un encabezado nivel 3)

El título de la lección corresponde al mayor nivel de encabezado, el que se especifica con un gato `#`.
No debe haber ningún encabezado de este nivel en los episodios.  
Las secciones se deben delimitar con encabezados de nivel 2, es decir con doble gato `##`.

#### Subsecciones (Este es un encabezado nivel 4)

Y si hay subsecciones se deben poner con el nivel 3 (`###`) y dentro de ellas se puede usar el nivel 4
(`####`).
Es decir, que no debe haber saltos entre niveles de encabezados (p. ej. usar un nivel 4 despues de un nivel 2).  
Siempre deja un renglón vacío antes y después de cada encabezado.

### Formato del texto

Cada línea de texto debe ser de 100 caracteres máximo. Al terminar los 100 caracteres puedes pasar
a una siguiente línea, 
y aún así se va a ver como un párrafo normal.  
Para que se vea un salto de línea debes dejar dos espacios al final de la línea.

## Formato para insertar figuras

Todas las figuras deben de estar dentro de la carpeta `fig/` del repositorio y deben tener su nombre en formato `LL-EE-FF.png`
(Número de lección-Número de episodio-Número de figura dentro del episodio.png).  
Debes utilizar el siguiente código para insertar las figuras en el cuerpo del episodio:  
~~~
<a href="{{ page.root }}/fig/01-01-01.png">
  <img src="{{ page.root }}/fig/01-01-01.png" alt="Aquí va el texto que describe a la imagen." />
</a>
~~~
{:language-html}

Si no queda bien el tamaño de la figura se pueden incluir los parámetro `height` y `width` así:  
~~~
<a href="{{ page.root }}/fig/01-01-01.png">
  <img src="{{ page.root }}/fig/01-01-01.png" width="435" height="631" alt="Aquí va el texto que describe a la imagen." />
</a>
~~~
{:language-html}

### Accesibilidad de las imágenes

Las personas con discapacidades visuales pueden utilizar lectores de pantalla, éstos son programas que leen en voz alta el
contenido de una página. Para que las imágenes logren su objetivo cuando las utiliza alguien con un lector de pantalla deben
de estar descritas en el texto alternativo. Éste va en el parámetro `alt=` dentro del código con el que se inserta la imagen 
(como se ve en las cajas de código anteriores). 

- Cuando la imagen es **decorativa** el texto alternativo debe de estar vacío de
esta manera:`alt=""`, para que el lector de pantalla no lea nada, ya que en ausencia del parámetro `alt=` se leería el
nombre del archivo, lo cual no es útil. 
- El texto alternativo debe ser **breve** y enfocado al mensaje que se quiere dar con la imagen.
- No debe haber **pies de figura**.

Sigue las recomendaciones de las páginas [Accesible Images Best Practices](https://it.ucsf.edu/how-to/accessible-images-best-practices)
y [Avoid these common alt-text mistakes](https://bighack.org/avoid-these-mistakes-when-writing-alt-text-descriptions-for-images/) para aprender a escribir texto alternativo útil.

Para evaluar la accesibilidad de una página puedes utilizar la herramienta [WAVE](https://wave.webaim.org/).

## Formato de las cajas de código

Para insertar una caja de código usa el siguiente código y modifícalo según el tipo de caja que necesites.

{% raw %}
    ~~~
    Aquí va el código.
    ~~~
    {: .aqui-va-el-tipo-de-caja}
{% endraw %}

Para una caja sencilla utiliza: `{: .source}`  
Para una caja de *Output* utiliza: `{: .output}`  
Para una caja de *Error* utiliza: `{: .error}`  
Para que tenga el formato de sintaxis de algún lenguage de programación y el nombre del lenguage
en la cajita usa el nombre del lenguage así:  
  `{: .language-html}`  
  `{: .language-bash}`  
  `{: .language-make}`  
  `{: .language-matlab}`  
  `{: .language-python}`  
  `{: .language-r}`  
  `{: .language-sql}`  
  
## Formato para las cajas especiales

Existen muchos tipo de cajas para contenido especial. Según el tipo de caja va a tener un color y un símbolo
diferente.

Para insertar una caja todo el contenido debe de tener un símbolo `>` antes de cada línea y el título
debe tener `##`. Debe haber líneas vacías entre la línea del título y el texto, y entre el texto y las 
cajas de código. El tipo de caja se especifica al final. Así:  

~~~
> ## Título de la caja
>
> texto
> texto
> texto
>
> ~~~
> código
> ~~~
> {: .tipo-de-caja-de-codigo}
{: .tipo-de-caja-especial}
~~~
{: .source}  

Los tipos de caja son los siguientes:  

> ## Notas extra o comentarios
>
> El tipo de esta caja es: `{: .callout}`
{: .callout}  
  
> ## Lista de tareas
>
> El tipo de esta caja es: `{: .checklist}`
{: .checklist}  

> ## Discusiones
>
> El tipo de esta caja es: `{: .discussion}`
{: .discussion}   

> ## Puntos clave
>
> El tipo de esta caja es: `{: .keypoints}`
{: .keypoints}  

> ## Objetivos
>
> El tipo de esta caja es: `{: .objectives}`
{: .objectives}  

> ## Prerequisitos
>
> El tipo de esta caja es: `{: .prereq}`
{: .prereq}  

> ## Alguna cita interesante
>
> El tipo de esta caja es: `{: .testimonial}`
{: .testimonial}  

> ## Ejercicio 1: Título del ejercicio
> 
> Los ejercicios deben tener número de ejercicio y título.
> El tipo de esta caja es: `{: .challenge}`
> 
> > ## Solución
> > 
> > Esta es la solución del ejercicio. Todos los ejercicios deben tener solución.
> > ~~~
> > Este es el código de la solución. El tipo de las cajas de solución es `{: .solution}`
> > ~~~
> > {: .source}
> > Para anidar una caja dentro de otra como en este caso el código es así:
> > ~~~
> > > ## Ejercicio 1: Título del ejercicio
> > > 
> > > Este es un ejercicio.
> > > 
> > > ~~~
> > > ls
> > > ~~~
> > > {: .language-bash}
> > > 
> > > > ## Solución
> > > > 
> > > > Esta es la solución.
> > > {: .solution}
> > {: .challenge}
> > ~~~
> > {: .source}
> {: .solution}
{: .challenge}

Así queda la caja de ejercicio hecha con el código que se ve en la solución anterior:

> ## Ejercicio 1: Título del ejercicio
> 
> Este es un ejercicio.
> 
> ~~~
> ls
> ~~~
> {: .language-bash}
> 
> > ## Solución
> > 
> > Esta es la solución.
> {: .solution}
{: .challenge}


## Diseñar ejercicios

Los ejercicios de una lección deben mezclar ejercicios de **aplicación directa** (implementación
de un concepto que se acaba de exponer) y ejercicios de **síntesis** (integración de habilidades
recién adquiridas con habilidades que se vieron previamente en la lección).  
Los ejercicios deben ser una forma de **evaluación formativa**; se deben poner en práctica las habilidades
aprendidas y deben servir para identificar malentendidos.
Es útil empezar por diseñar el ejercicio **final** y más complejo del episodio.  
Idealmente hay un ejercicio por **cada 10 o 15 minutos** de enseñanza. (Una sesión de dos horas necesitaría
~ 6 ejercicios). Planea que el tiempo de enseñanza entre ejercicios sea de 12 minutos y el tiempo de
resolución del ejercicio sea de 8 minutos.

### Tipos de ejercicios

- Preguntas de opción múltiple: Intenta que las opciones incorrectas revelen algún posible problema
de entendimiento.
- Problemas de Parsons: Consiste en pedirle al aprendiz que ordene las líneas de código de tal manera que
resulte un código completo funcional. Una versión difícil es incluir líneas de código que no forman parte de
la solución.
- Problemas de rellenar los vacíos: Consiste en pedir que agreguen las palabras o comandos faltantes a
un enunciado o línea de código, respectivamente. Se puede hacer más fácil agregando un banco de palabras y
más difícil poniendo muchos vacíos que llenar.
- Usar un concepto en otro contexto: Aplicar un concepto en un contexto distinto al que se enseñó puede
requerir que el estudiante haga búsquedas en internet o en los manuales del código. Por ejemplo, se puede
pedir que utilicen diferentes parámetros para modificar una gráfica previamente mostrada.

{% include links.md %}

