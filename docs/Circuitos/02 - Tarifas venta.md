# Tarifas venta circuito

Estas tarifas son las condiciones y precios de venta de cada touroperador para los circuitos. Las tarifas las vamos a encontrar en **Circuitos - Tarifas venta** esta opción abre la lista de tarifas, para trabajar con la información de una tarifa tendremos que abrir la ficha.

![alt text](.\images\ListaTarifasVenta.png)

![alt text](.\images\FichaTarifaVenta.png)

Cuando creemos una tarifa nueva, la delegación y el número de tarifa se asignan automáticamente.

- **Periodo de fechas**, periodo de vigencia de la tarifa.
- **Touroperador**, para facilitar la selección de los touroperadores, se ha añadido un nuevo campo en la ficha de los touroperadores para indicar si trabaja con circuitos. 

![alt text](.\images\FichaTouroperador.png)

- **Cliente**, ficha de cliente a la que se harán las facturas de este módulo.
- **Grupo registro IVA prod.**, código de IVA/IGIC de producto que juntamente con el código IVA/IGIC de negocio del cliente va a permitir obtener el porcentaje de impuestos que se aplicará en la factura de venta.
- **Cod. Terminos pago**, este dato vendrá de la ficha de cliente y solo se tendrá que personalizar si es necesario para las facturas de circuitos.
- **Cod. Formas pago**, este dato vendrá de la ficha de cliente y solo se tendrá que personalizar si es necesario para las facturas de circuitos.
- **Cod. Serie**, código de la serie de numeración que se usará para las facturas de venta, conviene (aunque no es obligatorio) que todas las tarifas de venta de circuito apunten a la misma serie.
- **Impuestos incluidos**, esta marca indica si los precios que vamos a tener en la tarifa ya llevan incluido el IVA/IGIC correspondiente. Independientemente de cual sea este porcentaje de impuestos.

El campo **Confirmado** se mantiene automáticamente mientras se introduce la información en la tarifa (El programa va a controlar que no podamos confirmar tarifas para un touroperador que se solapen), una tarifa que no está confirmada no puede utilizarse en el cálculo. Se puede forzar la comprobación de una tarifa utilizando la opción **Confirmar** del botón **Tarifa Venta**.

## Definir Habitaciones

Dentro de la tarifa se tienen que definir los tipos de habitación que se van a poder usar en las pre-reservas y reservas de circuitos.

![alt text](.\images\ListaHabitacionesTarifa.png)

Los campos **Habitacion TO** y **Habitacion cupo** pueden tener el mismo valor, con la única limitación de que los dos primeros caracteres deben existir en la tabal de habitaciones básicas. El **Pax Legal** se utiliza en el cálculo del módulo de hotel para indicar el mínimo de adultos que se calcularán para ese tipo de habitación, mientras que **Paxes ocupacion** se entiendo como el máximo de personas que puede haber en la habitacion.

## Definir precios de venta

En la tarifa se definen los precios de venta que aplican a los circuitos que vendemos a este touroperador.

![alt text](.\images\ListaPreciosVenta.png)

- **Circuito**, relación con el circuito, es obligatorio que el precio tenga circuito.
- **Cod. Categoria**, categoria del circuito, normalmente relacionado con la categoria de los alojamientos, es obligatorio que un precio tenga categoria. Las categorias se dan de alta como códigos circuito.
- **Periodo de fechas**, todo precio debe tener un periodo de fechas y ese periodo debe estar dentro de la vigencia de la tarifa.
- **Rango de personas**, podemos crear diferentes precios en base a la cantidad de personas, del touroperador, que vayan en el circuito. 
- **Tipo habitacion**, uno de los códigos de habitación creados en la tarifa, es obligatorio que un precio tenga habitación.  
- **Precio**, Precio por persona para las condiciones del precio 

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Tarifas**.

## Definir hoteles

Para cada combinación de **Circuito** y **Categoria** se va a crear un itinerario de hoteles en los que se alojarán los clientes durante el circuito.

![alt text](.\images\ListaHotelesTarifa.png)

- **Hotel**, código de hotel para el que se creará la reserva en el módulo de hotel de la aplicación.
- **Periodo de fechas**, este periodo debe estar dentro de la vigencia de la tarifa.
- **Dia inicio**, referencia para calcular los días de estancia en base a la fecha de inicio del circuito, 1 para el primer día del circuito.
- **Estancia**, días de estancia en el hotel.
- **Dias PC**, cuantos días estarán los clientes alojados en pensión completa. El programa entiende que el resto de días se alojan en media pensión. 

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el registro del hotel (el programa comprueba que no se produzcan solapamientos). Un registro sin la marca de Activo es como si no existiera y no se tendrá en cuenta en la creación del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Hoteles**.

Cada vez que se añaden reservas, de este touroperador, se crea una copia de esta tabla en el circuito, más adelante veremos como se maneja la información de los hoteles en el circuito.

## Definir extras

En caso de que existan ingresos por conceptos extra se pueden definir sus precios en la opción **Extras** del botón **Tarifas Venta**. Estos precios van a aplicar a los extras que se definan dentro de la salidas de los circuitos, siempre asociados a un touroperador.

![alt text](.\images\ExtrasTarifasVenta.png)

- **Cod. Extra**, código del extra al que aplicaremos el precio.
- **Cod. Circuito**, relación con el circuito, se pueden crear precios genericos, dejando el circuito en blanco.
- **Cod. Categoria**, relación la categoria del circuito, se pueden crear precios genéricos, dejando la categoria en blanco.
- **Periodo de fechas**, campos obligatorios que deben estar dentro de la vigencia de la tarifa.
- **Precio**, importe del precio.
- **Tipo precio**, indicación del modo de aplicación, puede ser un precio fijo o por persona.

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando el botón **Activar**.

## Utilidades

Dentro del botón **Tarifas venta** tenemos dos utilidades que no hemos comentado hasta ahora.

### Imprimir tarifa

Informe que muestra el detalle de toda la información de la tarifa de venta, incluyendo la cabecera, los precios y la definición de los hoteles.

### Copiar tarifa

Crear una copia completa de la tarifa en la que estamos, podemos utilizar esta acción para crear tarifas nuevas para otra temporada o para un nuevo touroperador que tenga condiciones similares a las del touroperador actual.