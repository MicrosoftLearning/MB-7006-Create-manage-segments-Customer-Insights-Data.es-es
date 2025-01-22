---
lab:
  title: 'Laboratorio 5: Generación de información'
---

# Laboratorio 5: Generación de información 

Estos son los objetivos del laboratorio:
- Generación de información sobre los segmentos 
- Visualización de diferenciadores y superposición entre segmentos 
- Creación de segmentos sugeridos en función de un segmento 

## Ejercicio 1: Generación de información sobre los segmentos
### Tarea 1: Diferenciadores de segmentos
A menudo, tendrás clientes que existen en varios segmentos. Puede resultar útil comprender cuándo se superponen entre ellos. Intentaremos descubrir los clientes comunes que pertenecen a los segmentos **Customer from Texas** y **Fall Closeout Promotion**, y también las diferencias de ambos segmentos en términos de **puntos de recompensa** y **LifetimeSpend**.

1. Selecciona **Información > Segmentos** en el menú de navegación izquierdo. Selecciona la pestaña **Conclusiones (versión preliminar)** y selecciona **+ Nuevo** en la barra de comandos o selecciona el botón **+ Nueva conclusión**.

1. Verás dos opciones: Primero usaremos los **diferenciadores** para ver lo que distingue ambos segmentos. Selecciona **Diferenciadores**.

1. Elige **Fall Closeout Promotion** como segmento principal. Selecciona **Siguiente**.

1. Elige **Customers from Texas** como otro segmento y selecciona **Siguiente**.

1. Ahora elige **Puntos de recompensa** en **Campos de cliente** y **LifetimeSpend** en **Campos de medida** para ver cómo los segmentos anteriores difieren entre sí con respecto a los **puntos de recompensa** y **LifetimeSpend**. Borra todos los demás campos de cliente y medida.

1. Selecciona **Siguiente** y denomina la información **Fall Promotion vs Customers from Texas**.

1. Comprueba que el **nombre de la entidad de salida** se establece en **FallPromotionvsCustomersfromTexas**. Selecciona **Guardar**.

1. Una vez finalizada la actualización de la conclusión, abre la conclusión creada. Selecciona las pestañas **Atributos** o **Medidas** para ver cómo difieren los segmentos entre sí con respecto a los campos seleccionados. Observe la **puntuación de diferencia**, que significa el grado de diferencia. Cuanto mayor sea la puntuación, más diferencias habrá.

1. Selecciona cada medida y atributo para ver información más detallada.

### Tarea 2: Superposición de segmentos
Ahora que hemos creado correctamente una conclusión de segmento mediante **diferenciadores**, crearemos una conclusión mediante **Superposición**.

1. Asegúrate de que te encuentras en la pestaña **Segmentos > Conclusiones (versión preliminar)** y selecciona **+ Nuevo** en la barra de comandos. Elige **Superposición**.

1. Selecciona los segmentos **Fall Closeout Promotion** y **Customers from Texas** para descubrir los clientes compartidos.

1. Selecciona **Siguiente**.

1. Denomina el segmento **Fall Promotion Customers Overlapped with Texas Customers** y comprueba que el **nombre de la tabla de salida** sea **FallPromotionCustomersOverlappedwithTexasCustomers**. Selecciona **Guardar**.

1. Una vez finalizada la actualización de la conclusión, abre la conclusión creada para ver el diagrama de Venn que muestra el total y el porcentaje de clientes compartidos entre estos dos segmentos.

## Ejercicio 2: Ampliación de segmentos y segmentos sugeridos
### Tarea 1: Ampliación de segmentos
La ampliación de segmentos se puede usar para buscar clientes similares a la base de clientes del segmento mediante inteligencia artificial. Anteriormente, creamos un segmento denominado **Fall Promotion Customers**, que contiene clientes millennial con compras en la tienda muy por encima de la media. Ahora, vamos a ampliar ese segmento y buscar clientes similares a ellos para que comercialicemos el Cold Brew Coffee recién lanzado.

1. Selecciona **Información > Segmentos** en el menú de navegación izquierdo y selecciona la pestaña **Todos los segmentos**.

1. Elige el segmento **Fall Promotion Customers**. Esto se convertirá en el segmento de origen.

1. En la barra de comandos, selecciona **Buscar clientes similares**.

1. Denomina el segmento **FallPromoExpansion**.

1. Selecciona **Agregar campos** en el paso siguiente para seleccionar los atributos y las medidas que se usarán para buscar clientes similares. Nos dirigiremos a clientes con una ubicación similar y una compra media en la tienda, por lo que elegiremos **PostCode** y **AverageStorePurchase**. Selecciona **Aplicar**.

1. A continuación, debes elegir quién se debe tener en cuenta. De momento, selecciona **Todos los clientes excepto el segmento de origen**.

1. Ahora debes seleccionar el número máximo de clientes que se van a incluir. Seguiremos con el **20 %**.

1. Si también deseas incluir miembros del segmento de origen, activa la última opción. De lo contrario, déjalo desactivado. Para nuestros propósitos, podemos dejarla desactivada.

1. Selecciona **Ejecutar**.

1. Una vez que el segmento termine de actualizarse, abre el segmento para buscar las **puntuaciones de similitud** y explora la **vista previa de los miembros del segmento**.

### Tarea 2: Obtención de segmentos sugeridos 
Usa Segmentos sugeridos para detectar segmentos interesantes basados en un atributo de cliente o medida de interés.

1. Selecciona **Información > Segmentos** en el menú de navegación izquierdo y selecciona la pestaña **Sugerencias (versión preliminar)**.

1. Selecciona **Obtener sugerencias** para comenzar la experiencia de configuración.

1. Elige **Mejorar una medida o métrica** y selecciona **Iniciar**.

1. En **Campos de medida**, selecciona **LifetimeSpend** como atributo de destino. Selecciona **Siguiente**.

1. A continuación, seleccionarás los atributos que pueden influir en el atributo de destino (**LifetimeSpend**) para que el modelo de IA pueda encontrar patrones interesantes entre el atributo de influencia y el de destino. El modelo sugerirá segmentos basados en esos patrones. Selecciona **Suscriptor de correo electrónico**, **Ingresos**, **Nivel de lealtad**, **Ocupación** y **Estado** como atributos de influencia.

1. Selecciona **Ejecutar**. El modelo de IA comenzará a buscar patrones entre los atributos de influencia y de destino seleccionados para mostrar sugerencias de segmento. Espera unos minutos para que el modelo finalice su análisis.

1. Una vez que el modelo haya terminado de ejecutarse y si es capaz de descubrir patrones entre los atributos de influencia y el atributo de destino, se mostrarán las sugerencias de segmento en la pestaña **Sugerencias (versión preliminar)**.

1. Para guardar el segmento, selecciona **Guardar como segmento** en el panel **Detalles del segmento sugerido**. Selecciona **Guardar**.

1. A continuación, el segmento guardado se puede ver en la pestaña **Todos los segmentos** y se puede usar para los procesos descendentes como cualquier otro segmento dinámico. Si deseas ver las reglas que ha aprendido el modelo después de guardar un segmento, puedes hacerlo seleccionando **Editar** en la pestaña **Todos los segmentos**.
