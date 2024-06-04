# Tarifas compra circuito

Estas tarifas son las condiciones y precios de compra de cada proveedor para los circuitos. Las tarifas las vamos a encontrar en **Circuitos - Tarifas compra** esta opción abre la lista de tarifas, para trabajar con la información de una tarifa tendremos que abrir la ficha. Antes de abrirse el programa nos va a pedir con que tipo de proveedor queremos trabajar:

![alt text](.\images\TiposdeProveedor.png)

![alt text](.\images\FichaTarifaCompra.png)

Cuando creemos una tarifa nueva, la delegación y el número de tarifa se asignan automáticamente.

- **Periodo de fechas**, periodo de vigencia de la tarifa.
- **Proveedor**, seleccionar la ficha de proveedor que usar al generar los costes.
- **Circuito**, podemos asociar una tarifa de compra a un circuito o dejarlo en blanco para generar una tarifa de compra genérica para el proveedor.
- **Nombre restaurante**, texto libre que solo veremos en las tarifas de tipo **Restaurante**, el contenido de este campo será visible en las prestaciones de los circuitos.
- **Grupo registro IVA prod.**, código de IVA/IGIC de producto que juntamente con el código IVA/IGIC de negocio del proveedor va a permitir obtener el porcentaje de impuestos que se aplicará en la factura de compra.
- **Cod. Terminos pago**, este dato vendrá de la ficha de proveedor y solo se tendrá que personalizar si es necesario para las facturas de circuitos.
- **Cod. Formas pago**, este dato vendrá de la ficha de proveedor y solo se tendrá que personalizar si es necesario para las facturas de circuitos.
- **Cod. Serie**, código de la serie de numeración que se usará para las facturas de compra, conviene (aunque no es obligatorio) que todas las tarifas de compra de circuito apunten a la misma serie.
- **Impuestos incluidos**, esta marca indica si los precios que vamos a tener en la tarifa ya llevan incluido el IVA/IGIC correspondiente. Independientemente de cual sea este porcentaje de impuestos.
- **Pax Maximo**, cantidad máxima de personas que puede manejar un solo **Guia oficial** (el campo solo se verá en este tipo de tarifas). En caso de superarse esta cantidad, el programa automáticamente calcula una linea extra de coste por la cantidad de personas que superen este máximo. 

El campo **Confirmado** se mantiene automáticamente mientras se introduce la información en la tarifa (El programa va a controlar que no podamos confirmar tarifas para un proveedor que se solapen), una tarifa que no está confirmada no puede utilizarse en el cálculo. Se puede forzar la comprobación de una tarifa utilizando la opción **Confirmar** del botón **Tarifa compra**.

## Definir precios de compra

En la tarifa se definen los precios de compra que aplican a los servicios prestados por este proveedor. La definición de los precios puede variar levemente en función del tipo de proveedor:

### Transportistas

![alt text](.\images\PreciosCompraTransportista.png)

- **Periodo de fechas**, todo precio debe tener un periodo de fechas y ese periodo debe estar dentro de la vigencia de la tarifa.
- **Rango de personas**, podemos crear diferentes precios en base a la cantidad de personas que vayan en el circuito. 
- **Precio**, precio para las condiciones del registro.
- **Tipo Precio**, indica como se aplica el precio, puede ser por vehículo o por persona.
- **Efectivo**, marcar el precio para incluirlo en el cálculo de la cantidad de dinero en efectivo que tenemos que entregar al guia acompañante para que pague los servicios.

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Tarifas**.

### Restaurantes

![alt text](.\images\PreciosCompraRestaurante.png)

- **Menu**, código de servicio del precio. Relacionado con el código que se asigna a las prestaciones de los circuitos.
- **Periodo de fechas**, todo precio debe tener un periodo de fechas y ese periodo debe estar dentro de la vigencia de la tarifa.
- **Rango de personas**, podemos crear diferentes precios en base a la cantidad de personas que vayan en el circuito. 
- **Precio**, precio para las condiciones del registro.
- **Precio bebida**, precio aparte de las bebidas no incluidas en el menu. Este campo es solo informativo ya que no se utiliza en los procesos de cálculo de costes.
- **Tipo Precio**, indica como se aplica el precio, puede ser por fijo o por persona.
- **Efectivo**, marcar el precio para incluirlo en el cálculo de la cantidad de dinero en efectivo que tenemos que entregar al guia acompañante para que pague los servicios.

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Tarifas**.

### Visitas 

![alt text](.\images\PreciosCompraVisita.png)

- **Visita**, código de servicio del precio. Relacionado con el código que se asigna a las prestaciones de los circuitos.
- **Periodo de fechas**, todo precio debe tener un periodo de fechas y ese periodo debe estar dentro de la vigencia de la tarifa.
- **Rango de personas**, podemos crear diferentes precios en base a la cantidad de personas que vayan en el circuito. 
- **Precio**, precio para las condiciones del registro.
- **Tipo Precio**, indica como se aplica el precio, puede ser por fijo o por persona.
- **Efectivo**, marcar el precio para incluirlo en el cálculo de la cantidad de dinero en efectivo que tenemos que entregar al guia acompañante para que pague los servicios.

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Tarifas**.

### Guias acompañantes y oficiales

![alt text](.\images\PreciosCompraGuiaAcom.png)

- **Periodo de fechas**, todo precio debe tener un periodo de fechas y ese periodo debe estar dentro de la vigencia de la tarifa.
- **Rango de personas**, podemos crear diferentes precios en base a la cantidad de personas que vayan en el circuito. 
- **Precio**, precio para las condiciones del registro.
- **Tipo Precio**, indica como se aplica el precio, puede ser por fijo o por persona.
- **Efectivo**, marcar el precio para incluirlo en el cálculo de la cantidad de dinero en efectivo que tenemos que entregar al guia acompañante para que pague los servicios.

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Tarifas**.

### Extras

Estos precios se aplican a las prestaciones con tipo de proveedor Extra. No confundir con los extras dentro de algunas tarifas de compra.

![alt text](.\images\PreciosCompraExtras.png)

- **Periodo de fechas**, todo precio debe tener un periodo de fechas y ese periodo debe estar dentro de la vigencia de la tarifa.
- **Rango de personas**, podemos crear diferentes precios en base a la cantidad de personas que vayan en el circuito. 
- **Precio**, precio para las condiciones del registro.
- **Tipo Precio**, indica como se aplica el precio, puede ser por fijo o por persona.
- **Efectivo**, marcar el precio para incluirlo en el cálculo de la cantidad de dinero en efectivo que tenemos que entregar al guia acompañante para que pague los servicios.

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Tarifas**.

## Definir extras

En caso de que existan costes por conceptos extra se pueden definir sus precios en la opción **Extras** del botón **Tarifas Compra**. Si hay extras definidos en la tarifa, se aplicarán automáticamente sin necesidad de indicar nada en el circuito. Solo las tarifas de Restaurantes y Visitas tienen la opción de definir extras

![alt text](.\images\ExtrasTarifasCompra.png)

- **Codigo**, código del extra del precio.
- **Periodo de fechas**, todo precio debe tener un periodo de fechas y ese periodo debe estar dentro de la vigencia de la tarifa.
- **Rango de personas**, podemos crear diferentes precios en base a la cantidad de personas que vayan en el circuito. 
- **Precio**, precio para las condiciones del registro.
- **Precio bebida**, precio aparte de las bebidas no incluidas en el menu. Este campo es solo informativo ya que no se utiliza en los procesos de cálculo de costes.
- **Tipo Precio**, indica como se aplica el precio, puede ser por fijo o por persona.
- **Efectivo**, marcar el precio para incluirlo en el cálculo de la cantidad de dinero en efectivo que tenemos que entregar al guia acompañante para que pague los servicios.

El campo **Activo** se mantiene automáticamente mientras se introduce la informacion en el precio (el programa comprueba que no se produzcan solapamientos). Un precio sin la marca de Activo es como si no existiera a efectos del cálculo del circuito. Se puede forzar la comprobación de un precio utilizando la opción **Activar** del botón **Tarifas**.

## Utilidades

Dentro del botón **Tarifas compra** tenemos dos utilidades que no hemos comentado hasta ahora.

### Imprimir tarifa

Informe que muestra el detalle de toda la información de la tarifa de compra, incluyendo la cabecera y los precios.

### Copiar tarifa

Crear una copia completa de la tarifa en la que estamos, podemos utilizar esta acción para crear tarifas nuevas para otra temporada o para un nuevo proveedor que tenga condiciones similares a las del proveedor actual.