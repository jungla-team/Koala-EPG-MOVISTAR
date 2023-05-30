## Koala EPG en EPGIMPORT Enigma2

Epgimport es un plugins para receptores enigma2 que nos permite crear listado de programacion de los canales TV a traves de un archivo XMLTV, para soporte y ayuda nos podeis encontrar:
*   **Grupo telegram de ayuda y soporte:** [https://t.me/joinchat/AFo2KEfzM5Tk7y3VgcqIOA](https://t.me/joinchat/AFo2KEfzM5Tk7y3VgcqIOA)
*   **Web oficial jungle-team:** https://jungle-team.com/

## Colabora con el projecto
La descarga del epg koala  **es gratuita**, no obstante si te gusta y deseas colaborar Para el mantenimiento de los servidores y Blog que gestiona jungle-team puedes realizar una donacion:

## [![](https://jungle-team.com/wp-content/uploads/2022/08/paypal-logo-4.png)](https://www.paypal.me/jungleteam)


## Formato EPG Koala

Koala epg esta diseñado para obtener el EPG (guia de eventos), de la plataforma Movistar+, donde ponemos a disposición de los usuarios diferentes opciones de visualizacion: 

 - Visualizacion de 3 dias de programacion
 - Visualizacion de 7 dias de programacion
 - Visualizacion de 15 dias de programacion
 - Visualizacion de 30 dias de programacion

Todas las versiones de KOALA-EPG llevan insertada una modificacion que nos **permite visualizar mediante caracteres tipo estrella** en el epg, la valoracion que votan los abonados a Movistar+ sobre los diferentes eventos.

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/epg1.jpeg)

## Instalacion EpgImport
Para poder realizar la descarga de epg-koala para la guia de programacion de Movistar+ es necesario previamente realizar la instalacion de epgimport, que lo podemos realizar de una manera muy sencilla mediante comandos una vez hemos accedido al receptor por terminal, para ello ejecutamos:

    opkg update
    
![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/Captura%20de%20pantalla%202022-08-27%20a%20las%2011.06.21.png)

    opkg install enigma2-plugin-extensions-epgimport

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/Captura%20de%20pantalla%202022-08-27%20a%20las%2011.07.02.png)

***Nota: Una vez realizada la instalacion es recomendable reiniciar la interfaz del receptor enigma2***

## Añadir sources epg-koala
Epg koala **forma parte de los sources oficales de rytec,** esto conlleva que en la **mayoria de imagenes por defecto tras instalar epgimport ya esta disponible nuestro epg**. En el caso contrario que sea una imagen en la que ***no aparezca koala epg o no este actualizado, podemos realizar este proceso para añadir/actualizar los sources epg koala de una manera facil por comando***, accediendo al receptor por terminal:

    wget --no-check-certificate -N https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/spainKoala.sources.xml -P /etc/epgimport

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/Captura%20de%20pantalla%202022-08-27%20a%20las%2011.32.11.png)

## Obtener epg de los canales con koala
Para obtener el epg de los canales de movistar con epg-Koala, una vez hemos realizada la instalacion de epgimport y añadidos/actualizado los sources koala es bastante facil que vamos a explicar a continuacion un uso basico.

**Paso 1:** Accedemos a epgimport, la zona de menu puede variar dependiendo la imagen, en este caso **lo vamos realizar desde imagen Openatv**, que su acceso es **menu + configuracion + EPG + epgimport**
![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/2.jpeg)

**Paso 2:** Tras acceder a la interfaz grafica de epgimport, pulsamos boton azul para seleccionar las fuentes koala el tipo epg que deseamos usar

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/3.jpeg)

**Paso 3:** Tras pulsar boton azul, como hemos comentado marcamos el tipo de epg koala que deseamos usar

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/4.jpeg)

**Paso 5:** Para comenzar a realizar la descarga pulsamos boton amarillo, tras realizar esta accion nos solicitara si realmente deseamos realizar la descarga, en este caso seleccionamos si

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/5.jpeg)

Automaticamente comenzara la descarga de eventos mostrandonos el proceso asi como los eventos descargados al finalizar

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/6.jpeg)

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/7.jpeg)

## Desactivar EIT
Las imagenes enigma2 por defecto tienen activado lo que se denomina EIT, que el evento actual y siguiente los datos del epg lo muestran a traves del transponedor y no del epg xmltv descargado, para evitar en caso que lo deseemos esta circustancia vamos a realizar lo siguiente.

**Paso 1:** Accedemos al menu epg de la imagen que tengamos instalada.

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/20.jpeg)

**Paso 2:** Pulsamos en configuracion

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/21.jpeg)

**Paso 3:** Debemos deshabilitar las opciones:

 - Mostrar EIT ahora/siguiente en la barra informacion
 - Habilitar EPG EIT

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/23.jpeg)

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/24.jpeg)


## Capturas de pantalla
![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/10.jpeg)

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/11.jpeg)

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/12.jpeg)

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/13.jpeg)

![enter image description here](https://raw.githubusercontent.com/jungla-team/Koala-EPG-MOVISTAR/main/Enigma2-epgimport/capturas-manual/14.jpeg)

## Borrar epg
Si deseamos borrar el epg descargado, en el caso que observemos algun compartamiento erratico lo mas recomendable es realizarlo mediante comando tras conectarnos al receptor enigma2 por terminal, para ello realizamos lo siguiente.

**Paso 1:** El epg en enigma2 se guarda en un archivo llamado epg.dat que se puede encontrar en diferentes directorios del recepto segun tengamos configurado el lugar de descarga, por lo que primero es saber donde esta ubicado, para ello lo podemos realizar facilmente buscandolo con el siguiente comando:

    find -name epg.dat

**Paso 2:** Una vez sabemos la ubicacion, antes de borrar debemos parar enigma2 para ello con el siguiente comado:

    init 4
    
**Paso 3:** Una vez hemos parado enigma2 procedemos a borrar el archivo epg.dat:

    rm -r <directorio>epg.dat

Paso 4: Una vez borrado, volvemos a arrancar enigma2:

    init 3
