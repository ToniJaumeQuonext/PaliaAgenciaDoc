# Reservas de circuitos

## Crear una prereserva

Cuando el touroperador envia la información, de una reserva de circuitos, la creamos dentro de circuitos como una pre-reserva. Las pre-reservas se irán numerando automáticamente.

![alt text](.\images\ListaPrereservas.png)

- **Touroperador**, para facilitar la selección de los touroperadores, se ha añadido un nuevo campo en la ficha de los touroperadores para indicar si trabaja con circuitos.
- **Localizador touroperador**, número de dossier de los clientes, este datos viajará a las reservas de los módulos de transfer y hotel para facilitar la identificacion de los pasajeros.
- **Fecha inicio circuito**, día de inicio del circuito (solo podremos asignar estos clientes a circuitos que salgan ese día).
- **Fecha entrada**, dia de llegada al destino, este día afecta a la reserva de transfer ya que hay que recogerlos ese día en el aeropuerto.
- **Fecha salida**, día de salida del vuelo, este día afecta a la reserva de transfer ya que hay que acompañarlos ese día al aeropouerto.
- **Nombre completo**, este campo lo vamos a descomponer en dos campos (ocultos por defecto) Nomrbre y Apellido, para que esto funcione bien, el nombre debemos indicarlo siempre en el mismo formato: APELLIDOS NOMBRE o APELLIDOS, NOMBRE.
- **Num. Documento identificación**, número de pasaporte o documento nacional de identidad, aquí podemos indicar en de la persona responsable y luego en reservas podremos indicar el documento de cada uno de los pasajeros.
- **Cod. Categoria**, código de la categoria contratada por los clientes, afectará al precio de venta.
- **Tipo habitacion**, tipo de habitación contratada por los clientes, si un localizador tiene más de un tipo de habitación tendremos que crear tantas pre-reservas como tipos de habitación haya.
- **Paxes**, cantidad de personas, cuando se introduce la cantidad el programa crea automáticamente esa cantidad de registros de reserva circuito y los relaciona con la pre-reserva.
- **Fecha venta**, se rellena con la fecha de creación pero es editable para reflejar la fecha real de venta, este dato se envía a las reservas de los módulos de transfer y hotel.

## Información de reservas

Como hemos comentado, al indicar la cantidad de pasajeros en la pre-reserva, se crean los registros de las reservas de circuito donde vamos a poder añadir alguna información que es propia de cada persona. Desde la lista que se abre el usuario tiene la opción de abrir la ficha para ver la información más en detalle.

![alt text](.\images\ListaReservas.png)

- **Nombre completo**, este campo lo vamos a descomponer en dos campos (ocultos por defecto) Nomrbre y Apellido, para que esto funcione bien, el nombre debemos indicarlo siempre en el mismo formato: APELLIDOS NOMBRE o APELLIDOS, NOMBRE.
- **Num. Documento identificación**, número de pasaporte o documento nacional de identidad.
- **Tipo Persona**, indicar si se trata de un adulto o un niño. 
- **Edad**, habitualmente solo necesitamos este dato en los niños por si hay que aplicar algún tipo de oferta en el contrato de compra del hotel.

## Cuadrante de circuitos

Esta opción es la que vamos a utilizar para crear las salidas de los circuitos y asignar las reservas a su salida correspondiente. Cuando el usuario entra verá una línea por cada touroperador que tenga reservas, con una columna por cada código de categoria. En la parte inferior verá el listado de las salidas de circuito que tengan fecha de salida posterior o igual a hoy (también aparecerán aquellas salidas que aun no tengan fecha de salida asignada). 

El cuadrante tiene dos opciones, para ver los clientes pendientes de asignar o los clientes ya asignados a una salida de circuito, para alternar este ambas opciones están los botones P y A en la esquina inferior izquierda o usando las opciones que hay en el botón **Circuito**.

En la parte superior de la consulta el usuario puede establecer filtros de fecha y de tipos de habitación para limitar la cantidad de reservas que se suman en los cruces entre touroperador y categoria.

![alt text](.\images\CuadranteCircuitos.png)
