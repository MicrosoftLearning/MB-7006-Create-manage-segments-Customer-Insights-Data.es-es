---
lab:
  title: 'Laboratorio 3: Creación de medidas'
---

# Laboratorio 3: Creación de medidas

Estos son los objetivos del laboratorio:
- Definición de medidas empresariales para realizar un seguimiento del rendimiento y el estado de la empresa
- Definición de medidas de cliente para obtener información sobre los clientes individuales

## Ejercicio 1: Definición de medidas y atributos
### Tarea 1: Valor medio de compras en tienda
En esta primera tarea, crearemos una medida para definir el valor medio de todas las compras en tienda realizadas en **Contoso Coffee**.

1. Expande **Información** y selecciona **Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo** en la barra de herramientas y después **Crear tu propia medida**.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el **Nombre** en **Valor medio de compra en tienda ($)** y selecciona **Listo**.

1. Cambia **Tipo de medida** de **Cliente** a **Empresa.**

1. Junto a **Cálculo 1**, selecciona **Editar nombre**.

1. Establece el **Nombre** en **Valor medio de compra en tienda ($)**.

1. Comprueba que el **Nombre del atributo de salida** es **AverageStorePurchaseValue**.

1. Selecciona **Listo.**

1. En el cálculo **Valor medio de compra en tienda ($)**, selecciona **Promedio** en el desplegable **Seleccionar función**.

1. Selecciona **+ Agregar atributo**, expande **Compras : PDV**, y selecciona **TotalPrice**.

1. Seleccione **Agregar**.

1. Selecciona el botón **Ejecutar** para completar tu medida.

    En esta siguiente tarea, crearemos una medida para definir el valor Medio de todas las compras web realizadas en **Contoso Coffee**.

1. Selecciona **Información > Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo > Crear tu propia medida** en la barra de herramientas.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el **Nombre** en **Valor medio de compra web ($)** y selecciona **Listo**.

1. Cambia **Tipo de medida** de **Cliente** a **Empresa**.

1. Junto a **Cálculo 1**, selecciona **Editar nombre**.

1. Establece el **Nombre** en **Valor medio de compra web ($)**.

1. Comprueba que el **Nombre del atributo de salida** es **AverageWebPurchaseValue**.

1. Selecciona **Listo.**

1. En el cálculo **Valor medio de compra web ($)**, elige **Promedio** en el desplegable **Seleccionar función**.

1. Selecciona **+ Agregar atributo**, expande **Compras: comercio electrónico** y selecciona **TotalPrice**.

1. Seleccione **Agregar**.

1. Selecciona el botón **Ejecutar** para completar tu medida.

### Tarea 2: Definir medidas de cliente
Necesitaremos dos medidas de cliente que se puedan usar para calcular un atributo de cliente. Crearemos una medida para determinar el gasto total de los clientes en **Compras online** y otra medida para determinar su gasto total en **Compras en tienda**. Una vez terminados, podemos crear un atributo de cliente para agregar esos dos juntos.

En esta tarea, crearemos una medida para definir el total de todas las compras realizadas en tienda.

1. Selecciona **Información > Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo > Crear tu propia medida** en la barra de herramientas.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el **Nombre** en **Gasto total en tienda** y selecciona **Listo**.

1. En el cálculo **Gasto total en tienda**, selecciona **Suma** en el desplegable **Seleccionar función**.

1. Selecciona **+ Agregar atributo**, expande **Compras: PDV**, selecciona **TotalPrice**, y selecciona **Agregar**.

1. Para configurar el cálculo de la medida, selecciona **Dimensiones (1)**.

1. Selecciona **Editar dimensiones**.

1. Expande **Compras: PDV**, selecciona **LoyaltyId**, y selecciona **Listo**.

1. Seleccione **Aplicar**.

1. Selecciona el botón **Ejecutar** para completar tu medida. Si se produce un error y necesitas elegir la **Ruta de relación**, selecciona **PoS_Purchases > Cliente** y selecciona el botón **Ejecutar** para completarla.

    Después, crearemos una medida para definir el total de todas las compras realizadas en línea.

1. Selecciona **Información > Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo > Crear tu propia medida** en la barra de herramientas.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el **Nombre** en **Gasto total en línea**, selecciona **Listo**.

1. En el cálculo **Gasto total en línea**, elige **Suma** en el desplegable **Seleccionar función**.

1. Selecciona **+ Agregar atributo**, expande **Compras: comercio electrónico**, selecciona **Precio total** y haz clic en **Agregar**.

1. En **Configurar sus cálculos de medidas**, selecciona **Dimensiones (1)**.

1. Seleccione **Editar dimensiones**.

1. Expande **Compras: comercio electrónico**, selecciona **ContactId**, y selecciona **Listo**.

1. Seleccione **Aplicar**.

1. Selecciona el botón **Ejecutar** para completar tu medida.

### Tarea 3: Definir atributos de cliente 
En primer lugar, definiremos los **Puntos de fidelización totales** obtenidos por cada cliente.

1. Si es necesario, selecciona **Información > Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo > Crear tu propia medida** en la barra de herramientas.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el **Nombre** en **Puntos de club totales** y selecciona **Listo**.

1. En el cálculo **Puntos de club totales**, elige **Suma** en el desplegable **Tipo de función**.

1. Selecciona **+ Agregar atributo**, expande **Compras: PDV**, selecciona **RewardPointsAdded** y selecciona **Agregar**.

1. Selecciona el botón **Ejecutar** para completar tu medida.

    Después, definiremos el valor total de todas las compras realizadas de cada cliente.

1. Selecciona **Información > Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo > Crear tu propia medida** en la barra de herramientas.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el **Nombre** en **Duración de gasto ($)** y selecciona **Listo**.

1. En el cálculo **Duración de gasto ($)**, elige **Suma** en el desplegable **Tipo de función**.

1. Selecciona **+ Agregar atributo**.

1. Selecciona la pestaña **Medidas**, expande **TotalInStoreSpend: CustomerInsights**, selecciona **Cálculo 1** y selecciona **Agregar**.

1. Selecciona el **+ (signo más)** para agregar un signo más después del atributo que acabas de agregar. El signo más debe aparecer en la fórmula de cálculo.

1. Selecciona **+ Agregar atributo**.

1. Selecciona la pestaña **Medidas**, expande **TotalOnlineSpend: CustomerInsights**, selecciona **Cálculo 1** y selecciona **Agregar**.

1. Selecciona el botón **Ejecutar** para completar tu medida.

    A continuación, definiremos el valor medio de todas las compras realizadas de cada cliente.

1. Selecciona **Información > Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo > Crear tu propia medida** en la barra de herramientas.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el nombre en **Compra en tienda promedia ($)** y selecciona **Listo**.

1. En el cálculo **Compra en tienda promedia ($)**, elige **Promedio** en el desplegable **Seleccionar función**.

1. Selecciona **+ Agregar atributo**, expande **Compras: PDV**, selecciona **Precio total**, y selecciona **Agregar**.

1. Selecciona el botón **Ejecutar** para completar la medida.

### Tarea 4: Valor medio de compras web
Después, definiremos el valor medio de todas las compras web realizadas de cada cliente.

1. Si es necesario, selecciona **Medidas** en el menú de navegación de la izquierda.

1. Selecciona **+ Nuevo > Crear tu propia medida** en la barra de herramientas.

1. Junto al texto de encabezado **Medida sin título**, selecciona **Editar detalles**.

1. Establece el nombre en **Compra web promedia ($)** y selecciona **Listo**.

1. En el cálculo **Compra web promedia ($)**, elige **Promedio** en el desplegable **Seleccionar función**.

1. Selecciona **+ Agregar atributo**, expande **Compras: comercio electrónico**, selecciona **Precio total** y selecciona **Agregar**.

1. Selecciona el botón **Ejecutar** para completar tu medida.
