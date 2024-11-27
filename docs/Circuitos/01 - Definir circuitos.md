# Definir maestro circuitos

El circuito es la unidad básica de este módulo, cada circuito está relacionado un código de circuito, su definición permitirá conocer los costes de cada una de las salidas de ellos. Las reservas se asocian a un circuito y estos códigos sirven de base para las tarifas de venta de los touroperadores.

## Crear circuito

Para crear un circuito iremos a **Circuitos - Configuración - Maestro circuitos**, se abre la lista de circuitos donde podemos crear un nuevo código, para terminar completar la definición tenemos que bajar a la ficha:

![alt text](.\images\FichaCircuito.png)

A la hora de definir el circuito debemos tener en cuenta lo siguiente:

- El código no se debe dejar en blanco, teniendo en cuenta que solo contamos con 10 caracteres no se recomienda dejar espacios en blanco, es mejor usar solo letras y números.
- La marca de **Fly Drive** tiene un efecto estadístico.

El programa no va a permitir borrar un código maestro de circuitos que ya se haya utilizado.

### Prestaciones

Las prestaciones representan los costes asociados al circuito, así como el itinerario que va a tener.

![alt text](.\images\PrestacionesCircuito.png)

La definición de cada prestación contiene la siguiente información:

- **Tipo proveedor**, es el indicativo del tipo de coste que usaremos para encontrar la tarifa y para seleccionar en la validación de los costes.****
- **Tarifa**, a trave de la tarifa vamos a asociar el coste al proveedor de contabilidad y definir los precios que aplicarán en el circuito.
- **Codigo**, en las prestaciones de los restaurantes o de las visitas, es el código del servicio solicitado al proveedor.
- **Dia inicio**, referencia para obtener la fecha del servicio, a partir de la fecha de salida del circuito (1 para el primer día del circuito). 
- **Servicio prepagado**, marcar los servicios que debemos tener contratados antes de la fecha de salida del circuito.
- **Max. personas por reserva**, indicación del proveedor del máximo de personas que se acepta en la compra de una reserva, en su página web.
- **Release compra entradas**, cantidad de días para calcular la fecha en la que debemos tener compradas las entradas, a partir de la fecha del servicio.
- **Requiere guia**, marcar los servicios (solo Visitas) que deben tener asociada una prestación de guia oficial que acompaña a los clientes durante la visita.
- **Max. personas por guia**, número máximo de personas a las que puede dar servicio el guía oficial asignado a la visita. De momento es un dato informativo para que el usuario lo tengo a la vista cuando toma deciones de negocio.
- **Prestación guia**, relación de la prestación de la visita con la prestación del guia oficial que la necesita

Eliminar o modificar una prestación en el maestro de prestaciones de un circuito solo va a afectar a las siguientes salidas de ese circuito.

## Revisión condiciones

Cuando el usuario quiere revisar todas las condiciones asociadas a un circuito puede utilizar la opcion **Imprimir** que hay dentro de la ficha del circuito. Esta informe muestra el detalle de todas las tarifas de compra asocidas a las prestaciones del contrato.

## Códigos de circuito

En la definición de las prestaciones hemos visto que algunas requieren de un código adicional, estos códigos se mantienen en **Circuitos - Configuración - Codigos circuito**, se abrirá una lista para crear, modificar o borrar esos códigos. Antes de abrir la lista el programa nos pedirá que tipo de código queremos crear:

![alt text](.\images\TipoCodigo.png)

![alt text](.\images\ListaCodigosCircuito.png)

El programa no va a permitir borrar un código de circuitos que esté en uso en una prestación de circuitos.



