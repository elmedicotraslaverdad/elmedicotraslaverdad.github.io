---
title: "'espeak', texto a voz directamente desde la terminal de GNU Linux" 
author: ign
date: 2022-01-30 +0800
categories: [Computación, Software, utilidades, texto-voz, espeak]
tags: [linux, software libre, open source, gpl, texto-voz, espeak]
render_with_liquid: false
pin: false
math: false
mermaid: false
toc: true
comments: false
---
'Espeak' es un programa que tiene la capacidad de leer un texto o escrito, introducido en el mismo comando/orden. También es capaz de expresar marcas de entonación como son los signos de interrogación o de exclamación. Tiene varias voces de diferentes idiomas y con varios acentos, aunque me parece que (sin desmerecer al programa) su pronunciación es algo pobre, aunque se entiende bastante bien.  

<br>
El comando 'espeak' suele venir instalado por defecto en algunas distribuciones GNU Linux y, de no estar presente en la nuestra, se puede incorporar ejecutando:
~~~bash
sudo apt-get update
sudo apt install espeak
~~~

<br>
Para descubrir en profundidad todos los entresijos de este comando basta con consultar su manual, como haríamos con cualquier otro comando: `man espeak`  

<br>
Los parámetros que suelo emplear con 'espeak' son los siguientes:

<br>
Para que lea en español un texto escrito a continuación entre comillas:
~~~bash
espeak -v es "texto_que_quiero_que_lea"
~~~

Si se desea que lo lea (en español) a menor velocidad (la velocidad por defecto es '160')
~~~bash
espeak -v es -s 120 "texto_que_quiero_que_lea"
~~~

Para que lea en español el contenido de un archivo
~~~bash
espeak -v es -f nombre_del_archivo
~~~

Si se quiere guardar la locución en un archivo de sonido '.wav'
~~~bash
espeak -v es -w "texto_que_quiero_que_lea"
~~~
No he descubierto aún cómo, en la misma orden, codificar el archivo, en lugar de formato '.wav' en formato '.mp3', aunque siempre es posible una transcodificación a posteriori con el socorrido 'ffmpeg'.  

<br>
Todos estos parámetros pueden combinarse en la misma orden.  

<br>
<br>
Entradas relacionadas:  
- []()
- []()  

<br>
<br>
<br>
--- --- ---  
<small>Fuentes:  
<a href="https://kacharreando.com/ubuntu/texto-voz-ubuntu/">kacharreando</a></small>  

<br>
<br>
<br>
<br>
<br>
<br>
