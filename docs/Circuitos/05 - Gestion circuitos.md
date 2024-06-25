# Gestión de circuitos

Una vez se han asignado las reservas a la salida del circuito comienza su gestión operativa, vamos a empezar en la opción **Circuitos** de la carpeta **Circuitos**.

![alt text](.\images\ListaCircuitos.png)

Con la opción **Ficha** vamos a poder ver todo el detalle del registro sobre el que está el cursor y consultar el estado de las distintas acciones que tenemos que ejecutar con cada circuito.

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

## Imprimir Documentacion circuito

La documentación del circuito consiste en la impresión de los bonos para el resto de los servicios asociados al circuito, excepto aquellos marcados como **Servicio prepagado**. Para imprimirla tenemos dos opciones:

* La acción **Imprimir documentacion** que tenemos en la consulta de cálculo de los circuitos.
* Imprimir la documentación al terminar el proceso de cálculo del circuito. El programa nos preguntará si queremos hacerlo.

El impreso muestra un resumen de la información de los servicios asociados al circuito y sus costes, a continuación un bono para cada servicio, como el que podemos ver de ejemplo a continuacion:

![alt text](.\images\BonoServiciosCircuito.png)

Una vez impresa la documentación, el circuito queda marcado **Documentacion emitida** y se rellena la fecha de emisión. Si se modifica la fecha de salida del circuito se desmarca el circuito para que el usuario sepa que tiene que volver a imprimir la documentación con las fechas correctas.

## Notificar servicios a proveedores

El programa dispone de una herramienta para notificar todos los servicios de la semana a los proveedores asociados a los circuitos, para generar este notificación tenemos que usar la opción **Notificar semana proveedores** que está en el botón **Circuitos** de la lista de circuitos. El proceso nos pedirá la fecha de salida de los circuitos que debe tener en cuenta y genera un fichero que se tratará de enviar por correo al proveedor, a continuación, un ejemplo:

![alt text](.\images\NotificacionSemanalProveedor.png)

Solo se enviarán notificaciones de los servicios que no estén marcados como **Servicio prepagado**. En caso de poderse enviar la notificación, porque el proveedor no tenga correo o porque el servicio de correo no esté configurado, se va a guardar el fichero excel en una carpeta indicada en los parametros de circuitos. En todo caso, el circuito queda marcado y se puede ver la fecha y hora que ha ejecutado está acción.

## Asignar Guia al circuito

Para poder asignar el guia acompañante del circuito podemos usar la acción **Asignar Guia Acompañante** del botón **Circuitos** de la ficha del circuito. Esta acción abre la siguiente ficha:

![alt text](.\images\FichaAsignarGuiaCircuito.png)

* **Efectivo guia** es el importe calculado por el programa de las prestaciones donde se ha indicado Efectivo. Este campo se rellena con el proceso de cálculo, por lo que, antes de poder asignar el guia, debemos haber calculado el circuito, al menos una vez.
* **Guia efectivo** será el proveedor relacionado con el guía acompañante.

El proceso genera la linea de coste en efectivo que, más adelante, podremos validar.

## Compra entradas monumentos

En el menu de Circuitos se ha incluido una opción **Prestaciones por dia** que los usuarios pueden utilizar para tener una visión de los servicios que requieren compra anticipada, al abrirse, la lista tiene un filtro para que nos muestre las prestaciones con fecha de operacion en dos semanas a partir de hoy. Esta consulta nos muestra los datos informativos del servicio, que hemos introducido en la definición del circuito y permite rellenar los datos correspondientes a cada compra de entradas:

![alt text](.\images\ListaServiciosSemana.png)

* **Entradas compradas**, cantidad de entradas que se utilizará a la hora de calcular el coste del servicio.
* **Fecha compra**, día de la compra, se puede utilizar para facilitar el cuadre de las tarjetas de crédito.
* **Hora visita**, dato informativo
* **Num. Operación tarjeta**, datos inforamtivo, se puede utilizar para facilitar el cuadre de las tarjetas de crédito.
* **Compra realizada**, cuando se hayan rellenado todos los datos anteriores pondremos la marca. Solo se podrá marcar si todo está rellenado y una vez marcado, el registro queda protegido contra cambios.

En aquellas ocasiones, en que una sola compra no sea suficiente para cubrir a todos los pasajeros, hay una acción **Duplicar prestacion** que sirve para crear una nueva prestación, a partir del registro sobre el que está el cursor, dejando en blanco los campos correspondientes a los datos de la compra. Esta misma acción está disponible en la opción **Prestaciones** que podemos encontrar en la lista y en la ficha de circuitos.