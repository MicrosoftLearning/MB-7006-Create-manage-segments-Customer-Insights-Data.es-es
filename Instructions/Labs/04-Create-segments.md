---
lab:
  title: 'Laboratorio 4: Creación de segmentos'
---

# Laboratorio 4: Creación de segmentos

Estos son los objetivos del laboratorio:
- Creación de un segmento a partir de un perfil de cliente
- Creación de un segmento mediante medidas
- Creación de un segmento desde cero

## Ejercicio 1: Creación de segmentos a partir de varios orígenes 
### Tarea 1: Creación de un segmento a partir de un perfil de cliente
En esta primera tarea crearemos un segmento basado en el perfil de cliente. Identificaremos a los clientes que residen en el estado de Texas. 

1. Amplía **Información** y selecciona **Segmentos** en el menú de navegación izquierdo.

1. Selecciona **+ Nuevo > Crear a partir de perfiles**.

1. En **Campo**, selecciona **Estado** y, en **Valor**, elige **Texas**.

1. Selecciona **Revisar**.

1. Denomina el segmento **Customers from Texas** y comprueba que el **nombre de la tabla de salida** se ha rellenado automáticamente con **CustomersFromTexas**.

1. Selecciona **Guardar**.

### Tarea 2: Creación de un segmento mediante medidas 
El marketing de Contoso Coffee quiere llevar a cabo una nueva promoción. En función de los datos históricos, marketing ha identificado que desean dirigirse a los clientes de preparar en casa con un valor de compra en línea superior a la media para hacerlo. Esta vez crearemos el segmento mediante la opción **Crear a partir de medidas**. 

1. Selecciona **Información > Segmentos** en el menú de navegación izquierdo.

1. Selecciona **+ Nuevo > Crear a partir de medidas**.

1. Selecciona el atributo **Compra media en tienda ($).**

1. Establece el **operador** en **Mayor que**.

1. Establece el **valor** en **100**. El gráfico se debe rellenar con **Compra media en web ($)** por percentil.

1. Selecciona **Revisar**.

1. Denomina el segmento **Premiere Customers** y comprueba que el **nombre de la tabla de salida** se ha rellenado automáticamente con **PremiereCustomers**.

1. Selecciona **Guardar**.

### Tarea 3: Creación de un segmento desde cero
Cada temporada, Contoso Coffee lleva a cabo diferentes promociones. Este año, quieren llevar a cabo una promoción de finales de otoño diseñada para vender los modelos de fin de año restantes. Buscan dirigirse a la generación X con una compra superior a la media en tienda con el Cold Brew Coffee lanzado recientemente. Dado que hay varios criterios necesarios para este segmento, lo crearemos desde cero.

1. Selecciona **Información > Segmentos** en el menú de navegación izquierdo. Selecciona **+ Nuevo > Crear tu propio**.

1. Junto al texto del encabezado **Segmento sin título**, selecciona **Editar detalles** y cambia el **nombre** a **Fall Closeout Promotion**.

1. Comprueba que el **nombre de la tabla de salida** se ha rellenado automáticamente con **FallCloseoutPromotion** y selecciona **Listo**.

1. Con el panel **Agregar a la regla 1** en el lado derecho de la pantalla, amplía **Customer : CustomerInsights** y selecciona **DateofBitrh**. 

1. Selecciona **is** y **on or after**, y escribe la fecha **1/1/1965**.

1. Agrega otra condición con un calificador **and**.

1. Establece esta condición como **DateOfBirth** en **on or before 31/12/1979**.

1. Agrega otra condición con un calificador **and**. 

1. Amplía **Customer_Measure : CustomerInsights**.

1. Selecciona la medida **Compra media en web ($)** y agrégala a la **Regla 1**. 

1. Selecciona **is** y **greater than or equal to 125**.

1. Agrega otra condición con un calificador **and**. 

1. En el campo **Escribir un nombre de atributo o agrega desde el panel**, escribe **Gender** y selecciónalo en la lista que aparece. 

1. Selecciona **is** y **equal to male**.

1. Activa la casilla **Omitir caso**.

1. En **Regla 1**, seleccione **+ Agregar regla**. 

1. Selecciona el cuadro **Unión** y cámbialo a **Excepto**.

1. En el panel **Agregar a la regla 2**, amplía **Customer : CustomerInsights** y selecciona **Estado**. 

1. Selecciona **is** y **equal to Florida**.

1. Selecciona **Guardar**.

1. Selecciona **Ejecutar**.
