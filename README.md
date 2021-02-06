# MESA DE MEZCLAS

## GRUPO_MIXER_1500 (Irene, Aritz y Amaia)

### Este proyecto consiste en una mesa de mezclas. La mesa de mezcla de audio o mezcladora de sonidos es un dispositivo electrónico al cual se conectan diversos elementos emisores de audio, tales como micrófonos etc. 

### Antes de profundizar en nuestro proyecto aquí tenéis  introducción de lo que vamos a ver:

![Mesa](https://www.softzone.es/app/uploads-softzone.es/2019/10/Mesa-de-mezclas-DJ.jpg)

## 1.- Introducción

## 2.- Cómo funciona una mesa de mezclas (con sus partes)

### a- Micrófono y preamplificación

### b- Control de tono

### c- Fader y módulo de panorama

### d- Indicador de sobrecarga overload indicator

## 3.-Prototipo y diseño del chasis

### a-Planos y medidas
### b-Materiales

## 4.- Componentes importantes/distintos
### a-Potenciómetros
### b-Conmutadores

## 5.- Programas que hemos utilizado

### a-Proteus
### b-Circuit Cam

## 6.- Como hicimos el proyecto

## 7.- Futuras mejoras

## 8.- Conclusiones
### *

### *

### *

## 1.- Introducción

### Este proyecto ha sido desarrollado por alumnos de Mantenimiento Electrónico de Don Bosco (Errenteria). El proyecto tuvo inicio a mediados de Diciembre del 2020 y finalizo a mediados de Febrero del 2021.

### Esta mesa está alimentada a +15V y -15V  y tendrá un overload por si hay alguna sobrecarga. La mesa se compone de 3 canales de audio con entradas Jac y XLR cada una.

### En cuanto a su chasis se hizo de parte de madera y parte metacrilato de 8mm de ancho.

## 2.- Cómo funciona una mesa de mezclas (con sus partes)

### a.- MICRÓFONO Y PREAMPLIFICACIÓN

### Conexionado entradas:

#### Para el micrófono se ha puesto un conector XLR o Jac ya que son para insertar cables con señal balanceada, es decir, el bus tiene tres conectores. En un conductor se manda la señal de audio (positivo o Hot) y en el otro se manda la misma señal, pero de forma invertida es decir, con un desfase de 180º (negativo o Cold), el tercer conductor sería la tierra de nuestra entrada de audio. 

##### En está imagen podéis ver el conexionado de los extremos del cable XLR

![Conexionado_XLR](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROKoNDMT6zFwQGYu7mYIKWsKl9cmmbP66WJA&usqp=CAU)

##### En está imagen podéis ver el conexionado del cable Jac comparado y con los XLR

![Jac](https://images-na.ssl-images-amazon.com/images/I/61-UcVEf4fL._AC_SL1500_.jpg)


#### Con este tipo de conexión logramos eliminar el ruido y obtener un audio de mayor volumen y amplitud, que se logra de la siguiente manera: al momento de conectar el cable a un preamplificador, el equipo invierte la señal que viene en el conductor &quot;Cold&quot; convirtiéndola en una señal igual a la señal &quot;Hot&quot;, con la característica de que el ruido que lleva se queda en la misma forma.

#### El equipo suma la señal del conductor &quot;Hot&quot; con la señal &quot;Cold&quot;, el resultado es una señal de audio del doble de amplitud y una cancelación de ruido, ya que están en sentido contrario. Con la siguiente imagen vemos de forma gráfica lo que sucede:
![Hot y COLD](https://ickrom.com.mx/wp-content/uploads/2016/07/suma_se%C3%B1ales.jpg)

![](RackMultipart20210205-4-pet1t6_html_7e812fab18ce96f4.jpg)

### En la preamplificación tenemos dos switches:

#### Primer switch:Se encarga de conmutar la señal. Si se quiere conectar un instrumento de línea, se activa el switch para el otro lado, la señal hot pasa por R5 y la señal cold pasa por R6, y además, se quedan Cold y hot conectados entre ellos. En esa configuración se consigue un desgaste de 20dB. O dicho de otra forma, a la hora de conectar un instrumento con una tensión mayor se activa una resistencia adicional para que nuestro circuito pueda soportarla.

#### Segundo switch: Se encarga de hacer la suma de las señales la de entrada hot y la entrada cold (con un desfase de 180º). Si hay dos micrófonos si uno está muy cerca del otro, es posible que se solapen esto hace que las señales se anulen entre sí. Para que esto no pase la señal de un micrófono se desfasa 180º.

CONTROL DE TONO

Para explicar el funcionamiento, se descompone en dos partes: el circuito que equivale al amplificador operacional y por otro lado el circuito de los filtros.

![](RackMultipart20210205-4-pet1t6_html_6de6735750b1682e.png)

- Circuito de amplificación: Se basa en un amplificador no invertido.

La resistencia variable RV1 tiene una masa conectada. Cuando el cursor está en el medio de RV1, 50% de la trayectoria de RV1, las ondas de salida y entrada son las mismas, con ganancia = 1 o 0 dB.

Cuando el cursor se coloca en el 75% de la trayectoria RV1, la masa se acerca a la entrada positiva y la señal se cancela. Si los valores R1, RV1 y R2 tienen los valores correctos, como se muestra en la figura, colocando el cursor en esta posición, la señal de salida será la mitad de la entrada, la ganancia es = 0.5 o -6db.

Cuando coloca el cursor en el 25% de la trayectoria RV1, la masa se acerca a la entrada negativa. Cuando la señal se cancela en la entrada negativa, se amplificará en la salida. Ganancia = 2db-6db.

![](RackMultipart20210205-4-pet1t6_html_d911d00d01c44544.png)

- Circuito de filtro: la reactancia capacitiva disminuye con la frecuencia. Entonces habrá más voltaje en la entrada positiva del amplificador operacional, y la salida será el mismo voltaje.

Juntando ambos circuitos, esta es la respuesta final que se consigue (aprox).

![](RackMultipart20210205-4-pet1t6_html_8715f4feb5b659ad.png)

FADER Y MÓDULO DE PANORAMA

El volumen de la señal se controla con el fader VR1. Su cursor está conectado a la entrada positiva del amplificador operacional. El potenciómetro debe ser logarítmico, y el lado con mayor resistencia en el potenciómetro debe estar en la parte superior para igualar las variaciones de resistencia con las mayores diferencias de presión en volúmenes altos.

La salida es Vout = ((R2 + R3) / R3) • Vin = 2 • Como es Vin, la señal de entrada será dos veces mayor.

Con el potenciómetro panorámico VR2 se puede enviar la señal a los canales izquierdo y derecho, en la proporcionalidad deseada.

En resumen, Rv1 tiene la función de subir o bajar el volumen de nuestra señal y Rv2 tiene la función de dar prioridad al canal izquierdo o canal derecho de audio.

INDICADOR DE SOBRECARGA O `OVERLOAD INDICADOR´

Para ello vamos a usar un led para que sea visible para el usuario, que está habiendo una sobrecarga. Este led se encenderá cuando la tensión sea mayor a 45V o cuando esté por encima de los 6 Db.

CAJA PROTECTORA

Nuestra caja se hizo parte de madera y parte de metacrilato.

La parte de abajo iba a ser lisa, un lateral llevaría los conectores XLR, Switch y alimentación, y la parte de arriba llevaría los canales. Estos canales estarían anclados por tornillos . El resto de placas irían dentro de la caja por lo que no se ven.

Para empezar, se decidió los canales superiores y el lateral donde iban colocados el conector de alimentación, el switch de ON/OFF y los conectores XLR, iban a ser de madera.

Para hacerlas, se cogen las medidas de altura, anchura y profundidad de los conectores y así sacas todas las medidas de la placa lateral.

Sin embargo, para la placa de abajo, se tienen que sacar las medidas de la placa superior primero, y lo que midan la profundidad de los conectores de la placa lateral se suma a cuánto mide la placa superior y así salen las medidas de la inferior.

La medida de los canales se cogen midiendo el fader y los 6 potenciómetros que se verán arriba.

Por último los laterales que faltan, se hicieron de metacrilato, para que se viese la electrónica interior.

Nuestra caja midió lo siguiente:

**3.- Componentes importantes/distintos**

- Fader
- Potenciómetros logarítmicos/lineales
- Switches

**4.- Programas que hemos utilizado**

Proteus: con este programa podremos crear los diferentes circuitos que necesitamos y podremos simularlos en el. De esta forma podremos comprobar de antemano posibles fallos que pueden aparecer, además, hay un apartado donde podemos hacer una PCB y descargar el archivo en modo que podamos hacerlo en CircuitCam, y así poder fresar en una LPKF con un archivo .lmd.

Todos los Proteus que hemos utilizado están subidos también a esta plataforma, pero aun así explicaremos un poco como hemos hecho todo. También subiremos el instalador de Proteus.

En el Proteus tenemos que hacer el esquema que queremos hacer ( os dejamos un vídeo de como usar Proteus por si no sabeis [https://www.youtube.com/watch?v=zb5OJxtPjvw](https://www.youtube.com/watch?v=zb5OJxtPjvw) )

Después si queremos hacer una PCB, tenemos que darle al icono rojo que aparece debajo de design.

![](RackMultipart20210205-4-pet1t6_html_edc303760c5283d4.png)

Aparecerá una nueva página en negro donde habrá que hacer la PCB. Dejamos un video de un ejemplo de como hacer una PCB ( [https://youtu.be/78GVsMHJnPg](https://youtu.be/78GVsMHJnPg) )

Una vez terminada la PCB, hay que sacar los ficheros para poder llevarlo al Circuit Cam. Para ello, hay que clicar `Output´ (que está arriba a la izquierda), darle a `Generate Gerber/Excellon file´, le damos a Yes, y aparecerá una pantalla como la de a continuación.

![](RackMultipart20210205-4-pet1t6_html_c909ba6a4b857e58.png)

A continuación nos saldrá la pantalla donde podemos escoger donde guardar nuestros archivos.

Circuit Cam: Con este programa podremos hacer el archivo para poder fresar después en una fresadora (LPKF).

Abrimos el Circuit Cam (pondremos link también para poder descargarlo)

Una vez abierto, tenemos que clicar en el icono que aparece en la imagen siguiente, para ir poniendo las capas de nuestra placa.

![](RackMultipart20210205-4-pet1t6_html_116ac18aeef3eec8.png)

Cuando clicamos nos aparecerá una pantalla como la siguiente:

![](RackMultipart20210205-4-pet1t6_html_1cfaa249785cd876.png)

Clicamos en Bottom Copper.GBR y aparecerá esta pantalla:

![](RackMultipart20210205-4-pet1t6_html_3122ac607640a15d.png)

En el apartado de capas, tenemos que buscar la que ponga Bottom Layer, y le damos a Importar.

![](RackMultipart20210205-4-pet1t6_html_920d3eca554e28a6.png)

Si tenéis Circuit Cam pirata, os saltará un error, pero le dais a aceptar y la capa se habrá hecho igualmente.

Saldrá algo tal que así:

![](RackMultipart20210205-4-pet1t6_html_d4fbf2e4c64c21d9.png)

Se hace los mismo con el resto de capas en este orden:

1.- Bottom Copper → Bottom Layer

2.- Top Cooper → Top Layer

3.- Drill Top-Bot → DrillPlated

Una vez terminadas estas capas, se hace el contorno para el recorte. Para ello se la da al icono de al lado del que hemos clicado antes.

![](RackMultipart20210205-4-pet1t6_html_7c38645689fe538b.png)

En la pantalla que aparece a continuación yo recomiendo poner las siguientes características y después hay que clicar en `Ejecutar´.

![](RackMultipart20210205-4-pet1t6_html_fb8f1286b62b6ca4.png)

Por último aislamos todas las capas dándole al botón indicado en azul, y guardamos nuestro proyecto dándole al botón indicado en morado. Se nos formarán dos archivos, pero el que se usa para la LPKF es el archivo .LMD

![](RackMultipart20210205-4-pet1t6_html_e953ff2b2ea9abac.png)

**5.- Como hicimos el proyecto**

Para

**6.- Fotos de nuestro prototipo final**

**7.- Futuras mejoras**

Mediante este apartado explicaremos los cambios que se podrían hacer para tener una mejor funcionalidad del proyecto.

**WIFI/Bluetooth**

Pensamos que la mesa podría tener incorporada un chip de Wifi o Bluetooth para así conectar el móvil a la mesa y poner la música que uno quiera.

**Fuente de alimentación Phantom**

La mesa de mezclas tiene un preamplificador. Para alimentar este preamplificador se puede usar el phantom power que proviene de una unidad externa. La idea detrás de esto es que la mesa no necesite una fuente de alimentación propia, haciendo además que disminuya el tamaño, el peso y la practicidad general de la mesa. La denominación proviene del hecho de que la alimentación es «invisible» es decir que se encuentra dentro del dispositivo al que vamos a conectar la mesa y no por fuera o como parte de la mesa.

**Poner un conector USB**

Se podría añadir a la mesa un conector USB.

**Carcasa de fuera de madera**

La carcasa para la mesa de mezclas, en nuestro proyecto se hizo de aluminio, aunque en un principio nuestra idea fue hacerla de madera, ya que no es conductora, y además la mesa quedaría con un estilo más clásico. También tuvimos la idea de imprimir la carcasa en una impresora 3D, pero no tuvimos tiempo suficiente para aprender a diseñar la caja en el programa 3D y para imprimirla. Todas las mesas que veíamos en internet eran de plástico o de algún metal, con un estilo moderno, así que al final decidimos hacerla de aluminio, y lo más parecido al resto de mesas que se venden.

**8.- Conclusiones**

A pesar de ser un reto desafiante, ha sido agradable para todos trabajar en este proyecto. Nos ha aportado conocimientos que hemos obtenido unos de otros.

Al reunir todos los procesos, podemos concluir que el proceso ha sido positivo en todos los aspectos. El trabajo realizado ha dado como resultado una variada mesa de mezclas.

