# Gestión de circuitos

Una vez se han asignado las reservas a la salida del circuito comienza su gestión operativa, vamos a empezar en la **Circuitos** de la carpeta **Circuitos**.

![alt text](.\images\ListaCircuitos.png)

Con la opción **Ficha** vamos a poder ver todo el detalle del registro sobre el que está el cursor.

## Gestión hoteles

Cuando se asignan reservas a un circuito se crea una copia de los hoteles definidos en la tarifa de venta del touroperador de esas reservas [Hoteles Tarifa](02%20-%20Tarifas%20venta.md#HotelesTarifaVenta). Esta información la vamos poder gestionar desde la opción **Hoteles** del botón **Circuitos**.

![alt text](.\images\ListaHotelesCircuito.png)

La columna **Hotel** será la única información que podremos cambiar en esta consulta para poder utilizar un hotel diferente al programado inicialmente, cuando se cambie se va a marcar la columna **Modificado manual**. En la lista de hoteles tenemos la opción Ficha para poder ver en detalle el estado cada uno de los hoteles

### Generar rooming previo

Desde la lista de hoteles podemos generar un listado rooming previo para todos los hoteles del circuito, usando la opción **Generar listado** del botón **Hoteles**, al ejecutarla se va a crear un fichero excel para cada hotel, si se configura el servidor de SMTP esos ficheros se enviarán a la dirección de correo electrónica configurada en la ficha del hotel. Los ficheros se almacenarán en la carpeta definida en el campo **Carpeta ficheros** de los parámetros de circuito, el nombre del fichero se comprondrá con circuito más el código interno más la fecha y hora de creación.

![alt text](images\EjemploRoomingPrevioHotel.png)

La fecha y hora de envío se almacena en cada registro de hotel del circuito, así como el usuario que hizo el envío.

### Confirmar hoteles

Cuando obtengamos la confirmación de las reservas, por parte del hotel, tenemos que marcarlo en el sistema ya que el programa va a controlar que no podamos pasar las reservas a los modulos de Transfer y Hotel hasta no tener la confirmación de todos los hoteles, usaremos la opción **Confirmar hoteles** del botón **Hoteles**, esta acción solo trabaja con los hoteles seleccionados en la pantalla para poder ir marcando las confirmaciones a medida que vayan llegando. Para cada hotel se almacena la fecha y hora de confirmación y el usuario que lo hizo.

En caso de ser necesario podemos retroceder esta marca, usando la opción **Desconfirmar hoteles** de ese mismo botón, también trabajaremos únicamente con los hoteles seleccionados en la pantalla.

### Crear Cabeceras de reserva

Este es el proceso que genera, a partir de las reservas de circuito, las reservas para el resto de módulos, como requisito previo tenemos que haber marcado como confirmados los hoteles del circuito. Para ejecutarlo usaremos la opcion **Generar Cabeceras (F11)** del botón circuitos que tenemos en la lista de circuitos y en la ficha de circuito. Si lo hacemos desde la lista podemos seleccionar varios circuitos antes de ejecutar la accion. Recordad que después hay que ir al modulo **Reservas** para ejecutar la opción **Generar detalle** para completar el traspaso a los módulos de hotel y transfer.

### Generar bonos cliente

Desde la lista de los hoteles podemos generar el bono para que el guia lo entregue en el hotel, como justificante del servicio. Como requisito previo tenemos se tienen que haber generado las reservas de hotel. Para hacerlo usaremos la opción **Generar bonos cliente** del botón **Hoteles**, esta acción trabaja con los hoteles seleccionados en la pantalla. A continuación un ejemplo de estos bonos.

![alt text](.\images\BonoClienteHotel.png)

### Imprimir Documentacion circuito

La documentación del circuito son los bonos para el resto de los servicios asociados al circuito, excepto aquellos marcados como **Servicio prepagado**. Para imprimirla tenemos dos opciones:

* La acción **Imprimir documentacion** que tenemos en la consulta de cálculo de los circuitos.
* Imprimir la documentación al terminar el proceso de cálculo del circuito. El programa nos preguntará si queremos hacerlo.

El impreso muestra un resumen de la información de los servicios asociados al circuito y sus costes, a continuación un bono para cada servicio, como el que podemos ver de ejemplo a continuacion:

![alt text](.\Images\BonoServiciosCircuito.png)

