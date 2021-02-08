# MESA DE MEZCLAS

## GRUPO_MIXER_1500 (Irene, Aritz y Amaia)

### Este proyecto consiste en una mesa de mezclas. La mesa de mezcla de audio o mezcladora de sonidos es un dispositivo electrónico al cual se conectan diversos elementos emisores de audio, tales como micrófonos etc. 

### Antes de profundizar en nuestro proyecto aquí tenéis la introducción de lo que vamos a ver:
![Mesa](https://www.softzone.es/app/uploads-softzone.es/2019/10/Mesa-de-mezclas-DJ.jpg)

# Introdución

## 1.- Presentación General

## 2.- Cómo funciona una mesa de mezclas (con sus partes)

### a- Entrada de audio

### b-Preamplificación

### c- Control de tono

### d- Fader y módulo de panorama

### e- Indicador de sobrecarga overload indicator

### f-Master
### g-Salida circuito
## 3.-Fuente de alimentación 
## 4.-Prototipo y diseño del chasis

### a-Planos y medidas
### b-Materiales

## 5.- Componentes importantes/distintos
### a-Potenciómetros
### b-Conmutadores

## 6.- Programas que hemos utilizado

### a-Proteus
### b-Circuit Cam

## 7.- Como hicimos el proyecto

## 8.- Futuras mejoras

## 9- Conclusiones
### -

### -

### -

## 1.- Presentación General

### Este proyecto ha sido desarrollado por alumnos de Mantenimiento Electrónico de Don Bosco (Errenteria). El proyecto tuvo inicio a mediados de Diciembre del 2020 y finalizo a mediados de Febrero del 2021.

### Esta mesa está alimentada a +15V y -15V  y tendrá un overload por si hay alguna sobrecarga además de un master. La mesa se compone de 3 canales de audio con entradas Jac y XLR cada una y salidas RCA en el Master.

### En cuanto a su chasis se hizo de parte de madera y parte metacrilato.

## 2.- Cómo funciona una mesa de mezclas (con sus partes)

### a.- MICRÓFONO Y PREAMPLIFICACIÓN

### Conexionado entradas:
![ENTRADA_AUDIO](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/ENTRADA_AUDIO.PNG)
### Para el micrófono se ha puesto un conector XLR o Jac ya que son para insertar cables con señal balanceada, es decir, el bus tiene tres conectores. 
#### En un conductor se manda la señal de audio (positivo o Hot) y en el otro se manda la misma señal, pero de forma invertida es decir, con un desfase de 180º (negativo o Cold), el tercer conductor sería la tierra de nuestra entrada de audio. 
#### Nuestro conector:

<img src="https://quecamarareflex.com/wp-content/uploads/2019/11/sonido-conectores-niveles-cables.jpg" alt="drawing" width="30%"/>

##### En está imagen podéis ver el conexionado de los extremos del cable XLR


<img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcROKoNDMT6zFwQGYu7mYIKWsKl9cmmbP66WJA&usqp=CAU" alt="drawing" width="30%"/>

##### En está imagen podéis ver el conexionado de los extremos del cable XLR

##### En está imagen podéis ver el conexionado del cable Jac comparado y con los XLR

<img src="https://images-na.ssl-images-amazon.com/images/I/61-UcVEf4fL._AC_SL1500_.jpg" alt="drawing" width="50%"/>



#### Con este tipo de conexión logramos eliminar el ruido y obtener un audio de mayor volumen y amplitud, que se logra de la siguiente manera: al momento de conectar el cable a un preamplificador, el equipo invierte la señal que viene en el conductor &quot;Cold&quot; convirtiéndola en una señal igual a la señal &quot;Hot&quot;, con la característica de que el ruido que lleva se queda en la misma forma.

#### El equipo suma la señal del conductor &quot;Hot&quot; con la señal &quot;Cold&quot;, el resultado es una señal de audio del doble de amplitud y una cancelación de ruido, ya que están en sentido contrario. Con la siguiente imagen vemos de forma gráfica lo que sucede:
![Hot y COLD](https://ickrom.com.mx/wp-content/uploads/2016/07/suma_se%C3%B1ales.jpg)

![](RackMultipart20210205-4-pet1t6_html_7e812fab18ce96f4.jpg)

### En la preamplificación tenemos dos switches:
![](https://lh3.googleusercontent.com/proxy/U8R-kC8FNKZ_UHuoRO9dYIgbRD8dxCAuUWR3rQgWbPv9Y3Vag0xpptAsUsug__7P4dRtKl2MGG1MUCVY57NkNQJ7Hi5lePomFsL8BWota-vb7FxbSyIh_22StZ5MQy0CEFtp6WL5ctodHS_XU3doG8N9HfblTvXI6Knhabfxnw)
### Primer switch: 
#### Se encarga de conmutar la señal. Si se quiere conectar un instrumento de línea, se activa el switch para el otro lado, la señal hot pasa por R5 y la señal cold pasa por R6, y además, se quedan Cold y hot conectados entre ellos. En esa configuración se consigue un desgaste de 20dB. O dicho de otra forma, a la hora de conectar un instrumento con una tensión mayor se activa una resistencia adicional para que nuestro circuito pueda soportarla.
![sw1](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/sw1.PNG)



### Segundo switch: 
#### Se encarga de hacer la suma de las señales la de entrada hot y la entrada cold (con un desfase de 180º). Si hay dos micrófonos si uno está muy cerca del otro, es posible que se solapen esto hace que las señales se anulen entre sí. Para que esto no pase la señal de un micrófono se desfasa 180º.

![sw2](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/sw2.PNG)
<img src="https://www.redmaule.com/diarios_en_red/site/artic/20200120/imag/foto_0000000420200120113844/microfonos-escenario-concierto-sobre-fondo-ilum.jpg" width="40%"/>

### b.-Preamplificación
![preamp](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/PREAMPLIFICACI%C3%93N.PNG) 

### En está etapa como podéis ver contaremos con el INA217 o tambien llamado amplificador instrumental, el cual, se compone interiormente por 3 amplificadores, su función principal es unir las dos señales La hot y cold para así solo optener una a la salida amplificada de está etapa.

#### El INA217 es ideal para señales de audio de bajo nivel, como baja impedancia balanceada micrófonos. Muchos instrumentos industriales, médicos y de instrumentación Las aplicaciones también se benefician de su bajo nivel de ruido y amplio ancho de banda. Los circuitos de cancelación de distorsión únicos reducen la distorsión a niveles extremadamente bajos, incluso en alta ganancia. 
<img src="https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/INA_FOTO.PNG" width="25%"/>

<img src="https://www.ti.com/ds_dgm/images/fbd_sbos360f.gif" width="45%"/>

### -Circuito de amplificación: Se basa en un amplificador no invertido.
#### La resistencia variable RV1 tiene una masa conectada. Cuando el cursor está en el medio de RV1, 50% de la trayectoria de RV1, las ondas de salida y entrada son las mismas, con ganancia = 1 o 0 dB.

#### Cuando el cursor se coloca en el 75% de la trayectoria RV1, la masa se acerca a la entrada positiva y la señal se cancela. Si los valores R1, RV1 y R2 tienen los valores correctos, como se muestra en la figura, colocando el cursor en esta posición, la señal de salida será la mitad de la entrada, la ganancia es = 0.5 o -6db.
#### Cuando coloca el cursor en el 25% de la trayectoria RV1, la masa se acerca a la entrada negativa. Cuando la señal se cancela en la entrada negativa, se amplificará en la salida. Ganancia = 2db-6db. 

![ina](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/INA217.PNG)

### En está etapa también es importante añadir que contamos con un potenciómetro. Pero no es un potenciómetro cualquiera sino uno logarítmico. Este tipo de potenciómetros los explicaremos con más detalle en componentes importes de nuestro circuito. Este potenciómetro tendrá que ser de 10 Ks.

<img src="https://i.ebayimg.com/images/g/WY4AAOSwYf9bAlEn/s-l300.jpg" width="20%"/>

### C-Módulo de tono
![cc](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/M%C3%93DULO_TONO.PNG) 
### Para esté circuito necesitaremos 2 amplificadores operacionales un NE5534 y un TL072
#### NE5534:

<img src="https://images-na.ssl-images-amazon.com/images/I/31xBGOjAhlL._SX342_.jpg" width="20%"/>

![](https://lh3.googleusercontent.com/proxy/9aEgTxghJpVxXU9ekmuZiN8th70voAFiwvZXsaQxTk0mvfzYpMVQcSatpSAk_scUZLTqW61iSP6yO6yzW3Fb-7rxFQ5URvTv0oECaa9PE3jM12iNxSFkmxQ)

#### TL072:

<img src="https://images-na.ssl-images-amazon.com/images/I/61yl5gXcnzL._SX385_.jpg" width="20%"/>

![](https://lh3.googleusercontent.com/proxy/M30C3jQO8HthNn8VVvilcqOA_-JKo2vMZLESvaip99FVQ-JcUlmB_KIcdKq7r3HxMWlJQemKfCh41S_PzbW5VY_iP48rDjop0-dFQy0sW3qlw6uTAWqQTg)

### En está etapa todos los potenciómetros serán linéales.
#### En esta etapa según la señal que recibamos bien sea de altos(Rv7), medios(Rv6) o bajos(Rv5)  podremos balancear la señal a la mejor calidad auditiva según a cuanta frecuencia esté llegando nuestra señal. Estos potenciómetros serán de 10Ks.

<img src="https://www.ecobadajoz.es/2606/potenciometro-de-plastico-10k-lineal-mod-p61020026.jpg" width="20%"/>

![s](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/BAJOS_MEDIOS_AGUDOS.PNG)

#### De la misma manera en este circuito contamos con un potenciómetro adicional de 1M:

<img src="https://mundoelectronica.net/905-large_default/potenciometro-lineal-monovuelta-1m-200mw-eje-36x6mm-plastico.jpg" width="20%"/>

#### Con este potenciómetro podremos balancear la señal en caso de que esté en el punto medio:
#### -bajo-medio
#### -medio-alto 
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/MEDIO_TONO.PNG)
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/GR%C3%81FICO_TONO.PNG)

#### En cuanto a las frecuencia que se adecua a cada etapa aquí tenéis un resumido esquema de estás frecuencias:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/tono_hz.PNG)
#### -Azul: Bajos
#### -Verde musgo: Medíos
#### -Rojo: Altos
#### -Verde pino: Potenciómetro balance (Bajo-Medio) y (Medio-Alto)

### d.-Fader y módulo de panorama

![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/FADER.PNG?raw=true)

### Para está etapa utilizaremos el amplificador NE5534 de nuevo y un fadder(logarítmico) y un potenciómetro lineal los dos de 10Ks.
### Fadder:

<img src="https://images-na.ssl-images-amazon.com/images/I/61tosb4eO7L._AC_SY450_.jpg" width="20%"/>

#### El volumen de la señal se controla con el fader VR1 el cual es un potenciómetro logarítmico . Su cursor está conectado a la entrada positiva del amplificador operacional. El potenciómetro debe ser logarítmico, y el lado con mayor resistencia en el potenciómetro debe estar en la parte superior para igualar las variaciones de resistencia con las mayores diferencias de presión en volúmenes altos. Su función principal es controlar el volumen del canal.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/VOLUMEN.PNG?raw=true) 

#### Con el potenciómetro panorámico VR2 se puede enviar la señal a los canales izquierdo y derecho, en la proporcionalidad deseada. En resumen, Rv1 tiene la función de subir o bajar el volumen de nuestra señal y Rv2 tiene la función de dar prioridad al canal izquierdo o canal derecho de audio.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/L_R.PNG?raw=true)
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/L_R_GRAFICO.PNG?raw=true)

### e.-Indicador de sobrecargas "Overload Indicator")
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/OVERLOAD.PNG )
#### Está etapa en la mesa de mezclas es opcional, su función principal es avisarnos cuando hay una sobrecarga en mi canal, este aviso no lo notificará a través de un led. Este led se encenderá cuando la tensión sea mayor a 3V o cuando esté por encima de los 6 Db. Esto sucederá cuando el transistor del esquema se excite. 
#### Esté circuito se compone principalmente de dos amplificadores LM1458 y del transistor BC549.
##### LM1458:

<img src="https://www.baudaeletronica.com.br/media/catalog/product/cache/1/image/800x/9df78eab33525d08d6e5fb8d27136e95/l/m/lm1458.jpg" width="30%"/>

<img src="https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/LM1458.PNG" width="45%"/>

##### BC549: 
<img src="https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/BC549.PNG" width="45%"/>

### f.-Master:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/Master.PNG)
### Para está etapa necesitaremos 2 amplificadores NE5532, un potenciómetro tandem o doble(a poder ser logarítmico) de 47K y dos faders a su salida de 10ks.
##### NE5532:

<img src="https://www.eeeshopbd.com/wp-content/uploads/2019/10/NE5532-Op-Amp-.jpg" width="30%"/>

<img src="https://www.eleccircuit.com/wp-content/uploads/2018/12/pin-configurations-of-ne5532.jpg" width="65%"/>

##### Potenciómetro tandem: 

<img src="https://www.cetronic.es/sqlcommerce/ficheros/dk_93/productos/452047013-1.jpg" width="25%"/>

#### Este circuito es esencial para que esto lo podamos llamar mesa de mezclas, es la ultima etapa, al unir todas las salidas de los canales, por una parte el oído derecho Right(R) y por otra parte el oido izquierdo Left(L). 
#### Además de unir todos los canales manipula la ganancia de las entradas L y R en el circuito a través de un potenciómetro tándem.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/TAMDEM_ESQUEMA.PNG)
#### Al final de este circuito también disponemos con dos fadders los cuales, le van ha dar o quitar prioridad auditiva a cada entrada L o R independientemente.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/L_R_GRAFICO.PNG)
### g.-Salida Circuito:
### La salida de nuestro circuito será mediante conectores RCA. El conexionado se haría de esta forma:
##### RCA:

<img src="https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/RCA.PNG" width="25%"/>

<img src="https://img-aws.ehowcdn.com/750x500/cpi.studiod.com/ehowmedia/a04/nk/c4/solder-rca-connectors-1.2-800x800.jpg" width="55%"/>

#### -Rojo:Señal
#### -Negro:GND
## 3-Fuente de alimentación:
### Nosotros hemos calculado que nuestro circuito tiene un consumo de menos de 1A y que su alimentación es de +15v y -15V.
### Con estos datos hemos comprado una fuente de alimentación a su medida
### Fuente:
<img src="https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/fuente.PNG" width="35%"/>

### Link de compra:
[https://es.rs-online.com/web/p/fuentes-de-alimentacion-de-modo-conmutado-smps-integradas/1227791/](https://es.rs-online.com/web/p/fuentes-de-alimentacion-de-modo-conmutado-smps-integradas/1227791/)
## 4- Prototipo y diseño del chasis
### Nuestra caja está echa parte de madera y parte de metacrilato.

### La parte  trasera, los 3 laterales son de metraquilato
#### -La partes restantes es decir, el lateral superior y la parte delantera son de madera.
#### -El lateral superior tiene los conectores  de alimentación y el interruptor
#### En la parte superior tenemos: Switches, potenciómetros, Fadder , Entradas Jack/XLR y salidas RCA


#### Estás serían las medidas de nuestra caja:


## 5- Componentes importantes/distintos

### a.- Potenciómetros logarítmicos/lineales:
![](https://3.bp.blogspot.com/-Uc-tN4kcKL0/Vris5dQXSPI/AAAAAAAABrY/sLkZeoC7VJc/s400/p9.png)
### -Lineales(B): En estos potenciómetros la resistencia es igual hacia ambas direcciones, hay que tomar en cuenta que el decremento de el valor de la resistencia se produzca de izquierda a derecha y no al revés.

<img src="https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/pot.PNG" width="40%"/>

### -Logarítmicos(A):  Estos potenciómetros se caracterizan por ser exclusivos para el audio puesto que se comportan de la misma forma que un oído humano. En tensiones bajas la resistencia sería alta y en tensiones altas la resistencia sería baja. Puesto que el oído humano diferencia mejor el volumen alto al bajo. Por lo tanto la resistencia no es igual a ambos lados y esto es una cosa que hay que tener en cuenta a la hora de hacer el conexionado de los potenciómetros a la placa.

<img src="https://www.cetronic.es/sqlcommerce/ficheros/dk_93/productos/451220008-1.jpg" width="20%"/>

![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/pot_log.PNG)

### b.- Fadder: Estos potenciómetros también son logarítmicos pero su patillaje es distinto. A la hora del conexionado es otro apartado a tomar en cuenta.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/fadeee.PNG)
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8tHVVdpEUYAHuWVtubn27rbdienan6Q88aw&usqp=CAU)
### c.- Switches: Los Switches del esquema y los físicos tienen un orden de patillaje lógico pero no es el mismo por lo tanto es otro apartado a tomar en cuenta. 
#### Su funcionamiento sería el siguiente, un Swich se compone de 6 pines. Cuando tu activas el interruptor los dos pines paralelos del lado opuesto se activan y salen cada uno por el pin contiguo del medio. Al cambiar de dirección el interruptor pararían los pines paralelos del otro lado opuesto por los pin contiguo del medio.
![](http://www.geekbotelectronics.com/wp-content/uploads/2015/06/Switch-de-palanca-mts-202-458x458.jpg)
![](http://www.geekbotelectronics.com/wp-content/uploads/2015/06/switch2p2t_diagrama.png)
##### COMPONENTES MÁS IMPORTANTES
COMPONENTES | Cantidad |
------------ | ------------ 
POTENCIMÉTROS LINEALES 10K | 12 unid
POTENCIMÉTROS LINEALES 1M| 3 unid
POTENCIMÉTROS LOG 10k | 3 unid
POTENCIMÉTRO Tamdem/lin 47K | 1 unid
FADERS    10k         | 5 unid
SWITCHES              | 6 unid
AMPLIFICADOR INA217  | 3 unid  
AMPLIFICADOR NE5534 | 6 unid
AMPLIFICADOR TL072 | 3 unid
AMPLIFICADOR LM1458 | 3 unid
AMPLIFICADOR NE5532 | 1 unid 
TRANSISTOR   BC549 |  3 unid
Entradas XLR/Jack            | 3unid
Salidas RCA     | 2 unid

## 6- Programas que hemos utilizado

### Proteus: con este programa podremos crear los diferentes circuitos que necesitamos y podremos simularlos en el. De esta forma podremos comprobar de antemano posibles fallos que pueden aparecer.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/proteus.PNG) 
![](https://i.postimg.cc/DzKKFRwX/Screenshot-2nn.png)
####  Además, hay un apartado en el proteus donde podemos hacer una de una PCB y descargar todas las capas que compone el  archivo.

![](https://file.pcbway.com/2014314175554866.jpg)
### CircuitCam: Cuando hallamos descargado estas capas anteriormente mencionadas podremos unificarlas en esté programa y hacer alguna pequeña modificación como un recorte al rededor de la placa o poner alguna nomenclatura en la propia placa. 
![](https://circuitcam.com/sites/circuitcam.eu/themes/circuitcam/logo.png) 
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/CIRCUIT.PNG)
### LPKF: Es la fresadora que hemos usado, una vez unificado el archivo en el CircuitCam nos lo pasará a formato .LMD y entoncen podremos fresarlo en está maquina.
![](https://img.directindustry.es/images_di/photo-g/9183-11896049.jpg) 

#### Todos los Proteus que hemos utilizado están subidos también a esta plataforma, pero aun así explicaremos un poco como hemos hecho todo. También subiremos el instalador de Proteus.

#### Os dejamos un vídeo de como usar Proteus por si queréis hacer vuestro propio diseño de este proyecto:
(https://www.youtube.com/watch?v=zb5OJxtPjvw)
#### En caso de que queráis modificar la PCB o hacer una nueva, aquí tenéis un vídeo de está explicación
(https://www.youtube.com/watch?v=XJa_qg5qkqw&feature=emb_logo&ab_channel=KrissElectronics)

### Después si queremos hacer una PCB, para poder pasarla al Circuit Cam los pasos son los siguientes:  
#### 1-Le daremos al icono rojo que aparece debajo de design.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/1.PNG)

#### 2-Aparecerá una nueva página en negro donde habrá que hacer la PCB. 
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/2.PNG)
#### 3-Una vez terminada la PCB, hay que sacar los ficheros para poder llevarlo al Circuit Cam. Para ello, hay que clicar `Output´ (que está arriba a la izquierda), darle a `Generate Gerber/Excellon file´, le damos a Yes, y aparecerá una pantalla como la de a continuación.


#### 4-A continuación nos saldrá la pantalla donde podemos escoger donde guardar nuestros archivos.

#### 5-Abrimos el Circuit Cam (pondremos link también para poder descargarlo)

#### 6-Una vez abierto, tenemos que clicar en el icono que aparece en la imagen siguiente, para ir poniendo las capas de nuestra placa.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/3.PNG)

#### 7-Cuando clicamos nos aparecerá esta pantalla:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/4.PNG)



#### 8-Clicamos en Bottom Copper.GBR y aparecerá esta pantalla:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/5.PNG)

#### 9-En el apartado de capas, tenemos que buscar la que ponga Bottom Layer, y le damos a Importar.

![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/6.PNG)

#### 10-Si tenéis Circuit Cam pirata, os saltará un error, pero le dais a aceptar y la capa se habrá hecho igualmente.
#### Saldrá algo tal que así:

![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/7.PNG)

#### 11- Se hace los mismo con el resto de capas en este orden:

##### 1.- Bottom Copper → Bottom Layer

##### 2.- Top Cooper → Top Layer

##### 3.- Drill Top-Bot → DrillPlated

#### 12-Una vez terminadas estas capas, se hace el contorno para el recorte. Para ello se la da al icono de al lado del que hemos clicado antes.
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/8.PNG)

#### 13-En la pantalla que aparece a continuación yo recomiendo poner las siguientes características y después hay que clicar en `Ejecutar´.

![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/9.PNG)

#### 14-Por último aislamos todas las capas dándole al botón indicado en azul, y guardamos nuestro proyecto dándole al botón indicado en morado. Se nos formarán dos archivos, pero el que se usa para la LPKF es el archivo .LMD

![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/10.PNG)
## 7- Como hicimos el proyecto
### 1-Inicialmente nos hicimos una planificación del proyecto
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/PLANING.PNG)
### 2-El siguiente paso fue hacer las simulaciones en proteus de la estapas y partes individuales del canal y demás circuitos cómo, el máster y el overload.
#### Canal:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/CANAL_GENERAL.PNG)
#### Master:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/MASTER%20GENERAL.PNG)
#### Overload:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/OVELOAD%20GENERAL.PNG)
### 3-Cuando todas las simulaciones funcionen se realizarán las PCBs de cada circuito, tomando en cuenta que queríamos que los potenciómetros y Swiches no estuvieran en la propia placa y así que ocupara menos espacio la placa.
#### Canal:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/PCB%20CANAL.PNG)
#### Master:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/PCB%20MASTER.PNG)
#### Overload:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/PCB%20OVERLOAD.PNG)
### 4-Habiendo echo todos los diseños, importaremos las distintas capas de cada placa al Circuit Cam.
#### Canal:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/CIRCUIT_CANAL.PNG)
#### Master:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/CIRCUIT_MASTER.PNG)
#### Overload:
![](https://github.com/Mesa-de-mezclas/Mesa-de-mezclas/blob/main/Im%C3%A1genes/CIRCUIT_OVERLOAD.PNG)
### 5-Una vez obtenido el LMD del Circuit Cam fresaríamos la placa en el LPKF.
### 6- Después de haberse fresado faltaría soldar correctamente cada componente a la placa, evitando lo mínimos cortos y puentes posibles.
### 7- Después de soldarlo todo correctamente lo conectaríamos a la fuente correctamente y miraríamos los posibles errores que puedan suceder corrigiendo con paciencia uno por uno.

## 8- Fotos de nuestro prototipo final

## 9- Futuras mejoras
### Mediante este apartado explicaremos los cambios que se podrían hacer para tener una mejor funcionalidad del proyecto.
### a.-Una PCB diseñada sin puentes con cables: al tener que hacer que hacer puentes con cablecitos, nos costó más encontrar algún que otro corto. Para la próxima, haríamos esos mismos puentes como pistas en la PCB.
### b.-Reajuste de elementos para una optimización de tamaño: nos hubiese gustado que la mesa fuese más pequeña.
### c.-Poner canales extras: en vez de 3 canales, hacer 4.
### d.-Una alimentación Phantom: para micrófonos que requieran de ella.
### e.-Tira de LEDs: para visualizar el volumen de la señal, así se mantiene en niveles óptimos para no distorsionar.
### a.-WIFI/Bluetooth: Pensamos que la mesa podría tener incorporada un chip de Wifi o Bluetooth para así conectar el móvil a la mesa y poner la música que uno quiera.
![](https://www.ibizasound.es/modules//smartblog/images/11-single-default.jpg)
### b.- Fuente de alimentación Phantom: La mesa de mezclas tiene un preamplificador. Para alimentar este preamplificador se puede usar el phantom power que proviene de una unidad externa. La idea detrás de esto es que la mesa no necesite una fuente de alimentación propia, haciendo además que disminuya el tamaño, el peso y la practicidad general de la mesa. La denominación proviene del hecho de que la alimentación es «invisible» es decir que se encuentra dentro del dispositivo al que vamos a conectar la mesa y no por fuera o como parte de la mesa.
![](https://www.audio-technica.com/es-us/media/catalog/product/cache/aee8318de9d8e245b6b604605849c7dc/c/p/cp8506_01.png)
### c.-Poner un conector USB: Se podría añadir a la mesa un conector USB.
![](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRjSi7y3uH1tEaec26_hcp_16PZdjzfGF0zE8L56kNKDIlbIKgpsh-QzfkH3oipn4GyHLV6ycw&usqp=CAc)
### d.- Carcasa de fuera de madera: La carcasa para la mesa de mezclas, en nuestro proyecto se hizo de aluminio, aunque en un principio nuestra idea fue hacerla de madera, ya que no es conductora, y además la mesa quedaría con un estilo más clásico. También tuvimos la idea de imprimir la carcasa en una impresora 3D, pero no tuvimos tiempo suficiente para aprender a diseñar la caja en el programa 3D y para imprimirla. Todas las mesas que veíamos en internet eran de plástico o de algún metal, con un estilo moderno, así que al final decidimos hacerla de aluminio, y lo más parecido al resto de mesas que se venden.

## 8.- Conclusiones
## En nuestra opinión, este reto nos ha parecido muy completo, y hemos aprendido mucho de él. Lo que más claro nos ha quedado, es que una PCB más limpia y sin puentes, los potenciómetros bien apuntados sus pines, y todos los conectores que van a las PCB iguales, nos hubiesen solucionado muchos problemas que hemos tenido y sobre todo nos hubiese ahorrado tiempo.
### Espero que este proyecto y su planteamiento os haya gustado. Os animamos a meteros en este mundo de jugar con el audio y las señales, puesto que es muy divertido y apasionante.
![](https://www.grupomotiva.es/wp-content/uploads/2018/05/700_FO44921268_e15135a8cbdffad7ff87122357149255.jpg)
