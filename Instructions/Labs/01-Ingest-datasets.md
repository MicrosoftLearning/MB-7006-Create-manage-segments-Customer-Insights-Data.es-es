---
lab:
  title: 'Laboratorio 1: Ingesta de conjuntos de datos'
---

# Laboratorio 1: Ingesta de conjuntos de datos
Estos son los objetivos del laboratorio:
- Incorporación de varios conjuntos de datos mediante PowerQuery
- Transformación de conjuntos de datos y cambio de tipos de columna
- Supervisión del estado de importación

Para crear segmentos, tenemos que importar primero los datos que usaremos en nuestros segmentos. En este laboratorio, importaremos algunos conjuntos de datos como requisito previo para unificar los datos y crear los segmentos.

## Ejercicio 1: Ingesta de orígenes de datos
Para este proyecto guiado, deberás importar varios orígenes de datos. Estos orígenes de datos se usarán para crear los perfiles de cliente unificados.

### Tarea 1: Ingesta de datos del cliente de una plataforma de comercio electrónico
1. En **Customer Insights - Data**, amplía la opción **Datos** situada en el menú de navegación izquierdo y selecciona **Orígenes de datos**.

1. Selecciona **+ Agregar un origen de datos**. Mira los métodos disponibles de ingesta de datos. Para este laboratorio, elige **Microsoft Power Query**, denomina el origen **eCommerce** y selecciona **Siguiente**.

1. Se mostrará una vista de los **orígenes de datos de Power Query** que **Customer Insights** puede ingerir. Toma nota de los tipos de conectores disponibles. Selecciona el conector **Texto o CSV**.

1. Escribe `https://aka.ms/CI-ILT/Contacts` en la **ruta de acceso o dirección URL del archivo** y selecciona **Siguiente**. Los datos pueden tardar unos instantes en cargarse.

1. Ahora deberías ver los datos del origen en formato de tabla. Selecciona **Transformar datos** para configurar los tipos de datos y los formatos de los datos que ingieres.

1. Verás que el encabezado de la columna ha aparecido en la primera fila de los datos. Para corregirlo, selecciona **Transformar > Usar la primera fila como encabezados** en la pestaña **Inicio** o selecciona la pestaña **Transformar** y, después, **Usar la primera fila como encabezados**.

1. Dado que hemos ingerido datos de un **origen de Texto o CSV**, todas las columnas han adoptado de forma predeterminada un **tipo de datos** de "Texto". Para ingerir y modelar correctamente los datos, podemos establecer el tipo de datos de las columnas sin texto.

1. Para cambiar el tipo de datos, selecciona el icono **ABC** del encabezado de columna. Actualiza el tipo de datos para estas columnas:
    - **DateOfBirth**: fecha
    - **CreatedOn:** fecha
    - **Income:** moneda

1. Comprueba que el campo **Nombre** del panel **Configuración de consulta** está establecido en **Contactos**. Selecciona **Siguiente**.

1. Selecciona **Actualizar manualmente** y después **Guardar**.

Enhorabuena. Has creado correctamente el primer origen de datos con un conjunto de datos. Continuaremos con la importación del siguiente conjunto de datos en la próxima tarea.

### Tarea 2: Ingesta de datos del cliente del esquema de fidelización
1. En **Customer Insights**, amplía la opción **Datos** situada en el menú de la izquierda y selecciona **Orígenes de datos**.

1. Selecciona **+Agregar un origen de datos** y elige **Microsoft Power Query** como método de importación. Denomina el origen **Loyalty** y luego selecciona **Siguiente.**

1. Selecciona el conector **Texto o CSV**.

1. Escribe `https://aka.ms/CI-ILT/LoyaltySchemeCustomers` en **Ruta de acceso o dirección URL del archivo**, selecciona **Siguiente** y, después, selecciona **Transformar datos**.

1. Como antes, selecciona **Transformar** y, después, **Usar la primera fila como encabezados.**

1. Actualiza el tipo de datos para estas columnas:
    - **DateOfBirth**: fecha
    - **RewardsPoints**: número entero
    - **CreatedOn:** fecha

1. Cambia el nombre de esta consulta a **Customers** en el panel **Configuración de consulta** y selecciona **Siguiente**.

1. Selecciona **Actualizar manualmente** y después **Guardar**.

### Tarea 3: Ingesta de datos del cliente de las compras de punto de venta
1. En **Customer Insights**, amplía la opción **Datos** situada en el menú de navegación izquierdo y selecciona **Orígenes de datos**.

1. Selecciona **+ Agregar un origen de datos**, elige **Microsoft Power Query** y denomina el origen **PoS** y, después, selecciona **Siguiente.**

1. Selecciona el conector **Texto o CSV**.

1. Escribe `https://aka.ms/CI-ILT/POSPurchases` en la **Ruta de acceso o dirección URL del archivo**. Selecciona **Siguiente** y, después, selecciona **Transformar datos.**

1. Como antes, selecciona **Transformar** y, después, **Usar la primera fila como encabezados.**

1. Actualiza el tipo de datos para estas columnas:
    - **PurchasedOn**: fecha
    - **TotalPrice**: moneda
    - **RewardPointsAdded:** número entero

1. En el campo **Nombre** del panel **Configuración de consulta**, cambia el nombre de la consulta a **Purchases**.

1. Selecciona **Siguiente**.

1. Elige **Actualizar manualmente** y selecciona **Guardar**.

### Tarea 4: Ingesta de datos de compras en línea
1. En esta tarea, ingeriremos los datos de las **compras en línea**, que representan las compras realizadas a través del sitio web de **Contoso Coffee**.

1. En **Customer Insights**, amplía la opción **Datos** situada en el menú de la izquierda y selecciona **Orígenes de datos**. (Asegúrate de que el estado del origen de datos de **eCommerce** indica **Correcto**).

1. Selecciona el conjunto de datos de **eCommerce** que creaste en la primera tarea y selecciona **Editar**. (Si los datos todavía se están actualizando, deberás esperar a que finalice el proceso antes de editarlos).

1. Selecciona **Siguiente**. 

1. Debería aparecer la vista de **Power Query** de los datos de **eCommerce Contacts** que ingeriste en la Tarea 1. En la pestaña **Inicio**, selecciona **Obtener datos.**

1. Se mostrará una vista de los conectores de orígenes de datos que **Customer Insights** puede ingerir. Selecciona **Texto o CSV**.

1. Escribe `https://aka.ms/CI-ILT/OnlinePurchases` en la **Ruta de acceso o dirección URL del archivo** y selecciona **Siguiente**. Selecciona **Crear**.

1. Como antes, selecciona **Transformar** y **Usar la primera fila como encabezados.**

1. Actualiza los tipos de datos de las columnas siguientes:
    - **PurchasedOn**: fecha
    - **TotalPrice**: moneda

1. Denomina esta consulta **Purchases** y selecciona **Guardar.**

**Importante:** tendrás que esperar a que el estado de todos los orígenes de datos esté en **Correcto** antes de poder pasar al ejercicio siguiente.
