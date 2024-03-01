# Integrantes

- Lluc Omella Sampera
- Eric Guillen Artacho
- José Antonio Pineda Fernandez

## Abstract

Nuestra iniciativa se centra en la creación de una herramienta con varios aspectos que fusionan un sistema de captura de tokens con una potente botnet. El componente denominado "TokenGrabber" está diseñado para recopilar los datos de las máquinas infectadas y enviarlos en formato JSON a un servidor central, donde se dispone de un panel de control para visualizar la información de todas las "víctimas". Por otro lado, la botnet incorporada dentro del troyano está equipada con un virus capaz de realizar conexiones de "reverse Shell", otorgándonos un amplio abanico de posibilidades, desde ejecutar ataques DDoS hasta llevar a cabo el minado de criptomonedas.

El camuflaje del troyano se efectuará dentro de un popular videojuego conocido como "Superfetch Dog". Esta elección no es aleatoria, pues este juego destaca por su atractivo comercial, su capacidad para entretener a los usuarios y su demanda de recursos moderada, lo cual lo convierte en una opción altamente atractiva para nuestro propósito. De esta manera, nuestra estrategia apunta a maximizar nuestras posibilidades de éxito al ocultar nuestras operaciones dentro de un entorno aparentemente inofensivo y atractivo para nuestro público objetivo.

## Introducción

La estructura del proyecto consiste en un servidor y varias máquinas virtuales dentro. Una de las máquinas llevará la herramienta BeEF (véase apartado BeEF), con la web y allí el troyano (véase apartado troyano). Otra tendrá la base de datos (véase apartado base de datos), en otra habrá el visor de la base de datos (véase apartado visor) y el botmaster (véase apartado botmaster).

## Gestión del proyecto

El proyecto lo hemos dividido en tres partes ya que somos tres integrantes en el grupo. Eric se encarga de toda la parte de la botnet y ejecutará el ataque. Lluc clonará la página de un videojuego donde estará el malware. También cambiará el HTML de la herramienta BeEF para que no se muestre nada que no se deba ver y parezca una página normal. José migrará la base de datos de la herramienta BeEF a MySQL y hará que los datos de la herramienta BeEF pasen a la base de datos.

## Teoría

Lo primero que hay que entender de nuestro proyecto es que todo lo que estamos haciendo está en un entorno seguro y que nadie externo al proyecto se ve afectado por el malware. Las víctimas que vamos a utilizar para recabar los datos seremos nosotros mismos o cuentas ficticias para que nadie se vea afectado. La herramienta BeEF es la encargada de recopilar la información del ordenador que ha entrado en la página web. Luego esos datos pasan a la base de datos, la cual ha migrado José. Gracias a los datos recopilados por la herramienta BeEF, Eric podrá realizar el ataque. Aparte, otra manera de recopilar información de los ordenadores es con el videojuego con el malware, que es lo que se ha encargado Lluc de hacer.
