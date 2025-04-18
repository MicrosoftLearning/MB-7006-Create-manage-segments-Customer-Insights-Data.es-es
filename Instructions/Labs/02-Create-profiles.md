---
lab:
  title: 'Laboratorio 2: Creación de perfiles de cliente unificados'
---

# Laboratorio 2: Creación de perfiles de cliente unificados
Estos son los objetivos del laboratorio:
- Combina tus orígenes de datos sin procesar en un perfil de cliente
- Selecciona una clave principal 
- Crea reglas de coincidencia
- Define índices y actividades de búsqueda y filtrado

Tu objetivo es descubrir cuántos perfiles de clientes únicos tiene **Contoso Retail** en los diferentes orígenes de datos.

## Ejercicio 1: Unificación los datos
### Tarea 1: Asignar contactos a tipos de datos comunes
1. Inicia sesión en **Customer Insights - Data**.

1. En el menú de navegación de la izquierda, expande **Datos**, selecciona **Unificar**. Seleccione **Comenzar**.

1. Elige **Seleccionar tablas y columnas**.

1. Selecciona las tablas que representan el perfil del cliente: **Contactos (eCommerce)** y **Clientes (Fidelización)**. Selecciona **Aplicar**.

1. Ahora se mostrarán las asignaciones de la tabla de origen en comparación con los tipos de modelos estándar. Puedes revisar los tipos en la tabla.

1. Debes elegir una **«Clave principal»** para cada entidad que hayas introducido. La clave principal debe ser una referencia única. En **Contactos de comercio electrónico**, selecciona **ContactId** como la clave principal.

1. Los datos de **Contactos de comercio electrónico** contienen una columna denominada **Suscriptor de correo electrónico** que se asignará a un tipo incorrecto, **Identity.Service.Email**, debido al nombre. Abre el desplegable de esta columna y selecciona la opción vacía (nada/en blanco). Si no lo hacemos, el comportamiento predeterminado del sistema combinará este campo con el campo **Correo electrónico**, cosa que no queremos que suceda.

1. Selecciona **Clientes de fidelización** en **Tablas** y establece **LoyaltyId** como clave principal.

1. Selecciona **Guardar columnas de origen** en la esquina superior izquierda.

1. Selecciona **Siguiente** y **Siguiente** de nuevo para omitir la comprobación duplicada y pasar al paso **Reglas de coincidencia**.

### Tarea 2: Especificar el orden de coincidencia
En la siguiente fase, deberás seleccionar el orden en el que combinar los perfiles. Podrás combinar atributos para garantizar que los perfiles unificados estén completos y la prioridad de los orígenes que se usarán para esos atributos.

1. Debes seleccionar el origen del perfil más completo o preciso como **Origen principal (primero)**. Comprueba que **Contactos: comercio electrónico** es el origen principal (primero).

1. Comprueba que **Clientes: fidelización** es el segundo origen de la lista. 

1. Comprueba que **Incluir todos los registros** está marcado en ambos orígenes de datos.

### Tarea 3: Crear una regla de coincidencia
1. Hay un indicador de advertencia en la línea **Clientes: fidelización**. Seleccione **+ Add rule** (+ Agregar regla).

1. Agrega la primera condición con **FullName**:
    - En la tabla **Contactos: comercio electrónico**, selecciona el campo **FullName**.
    - En la tabla **Clientes: fidelización**, selecciona el campo **FullName**.
    - Deje en blanco el desplegable **Normalizar**.
    - Establece el **Nivel de precisión** en **Básico**.
    - Establece el **Valor de precisión** en **Exacto** mediante el control deslizante.
    - Escribe el nombre **FullName, Email** para el **Nombre de la regla**.

1. Selecciona **+ Agregar** y elige **Agregar condición** para agregar una segunda condición para la dirección de correo electrónico.
    - En la tabla **Contactos: comercio electrónico**, selecciona el campo **Correo electrónico**.
    - En la tabla **Clientes: fidelización**, selecciona el campo **Correo electrónico**.
    - Deje en blanco el desplegable **Normalizar**.
    - Establece el **Nivel de precisión** en **Básico**.
    - Establece el **Valor de precisión** en **Exacto**.

1. Selecciona **Listo.**

1. Seleccione **Siguiente**.

1. En la pantalla **Vista de datos unificada**, no vamos a realizar ningún cambio. Selecciona **Siguiente** para pasar a la pantalla de revisión.

1. En la pantalla **Revisar**, selecciona **Crear perfiles de cliente**. Customer Insights ahora hará coincidir los datos de clientes de tus orígenes de información de clientes con el fin de identificar cuántos perfiles de clientes únicos tendrías según tus reglas. Puedes tardar algún tiempo en crear los perfiles.

Felicidades. Has unificado con éxito datos de varios orígenes de **Customer Insights** para crear un **Perfil unificado del cliente** que se puede usar para obtener información sobre toda tu base de clientes.

## Ejercicio 2: Configuración de índices y actividades de búsqueda y filtrado
En este ejercicio, configuraremos los criterios de **búsqueda y filtro** para que los usuarios de Customer Insights puedan buscar perfiles unificados del cliente. Después, configuraremos las actividades.

### Tarea 1: Configurar las columnas de búsqueda y el índice de filtro 
1. En **Customer Insights**, selecciona **Clientes** en el menú de navegación de la izquierda.

1. Selecciona **Índice de buscar y filtrar.** Algunos campos ya se agregan de forma predeterminada. Selecciona **+Agregar** en la barra de herramientas.

1. Selecciona **CustomerId, FirstName, LastName, FullName, DateOfBirth, EMail, PostCode, ContactId (eCommerce_Contacts), y LoyaltyId** (si no están seleccionados ya). Anula la selección de cualquier otro campo que esté activado. Selecciona **Aplicar**.

1. Seleccione **Guardar**.

1. Selecciona **Ejecutar**.

1. En **Customer Insights**, selecciona **Clientes** en el menú de navegación de la izquierda. Debería aparecer un conjunto de tarjetas de cliente, que representan los **perfiles unificados**. Puedes expandir las tarjetas para obtener más información sobre el cliente u ordenar las tarjetas por varios campos. Para probarlo, selecciona **Expandir tarjetas** y **Ordenar por** en la barra de herramientas.

1. Puedes usar **Buscar clientes** para buscar atributos de texto relacionados con los perfiles unificados del cliente. (por ejemplo, La búsqueda de "1" buscará en todos los atributos de texto y devolverá coincidencias y coincidencias parciales).

### Tarea 2: Crear actividades
1. En **Customer Insights**, expande **Datos > Actividades** en el menú de navegación izquierdo y selecciona **+ Configurar actividades**.

1. Haz clic en **Seleccionar tablas**.

1. Selecciona las tablas **Compras: comercio electrónico** y **Compras: PDV** y selecciona **Agregar**.

1. En **Compras: comercio electrónico**, configura lo siguiente:
    - Establece el **Tipo de actividad** en **SalesOrder**.
    - Establece la **clave principal** en **PurchaseId**.

1. En **Compras: PDV**, configura lo siguiente:
    - Establece el **Tipo de actividad** en **SalesOrder.**
    - Establece la **clave principal** en **PurchaseId.**

1. Seleccione **Siguiente**.
   
1. Configura **Comercio electrónico: compras** de la siguiente manera:
    - Escribe **OnlinePurchase** en **Nombre de actividad**.
    - Rellena los campos siguientes (deja los campos que no se mencionan en blanco):
        - **Timestamp**: PurchasedOn
        - **Actividad del evento**: Visualización del tipo de actividad
        - **Detalles adicionales**: asunto
        - **¿Mostrar esta actividad en la escala de tiempo del perfil de cliente?** Sí
        - **Icono**: selecciona la cesta de compras.
        - **¿Establecer tipos de campo de asignación en los atributos de tu actividad?** Sí, y configurar lo siguiente:
            - **Id. de pedido de ventas**: PurchaseID
            - **Fecha de pedido**: PurchasedOn
            - **Importe de ventas**: TotalPrice

1. Configura **PDV: compras** de la siguiente manera:
    - Escribe **PoSPurchase** para **Nombre de actividad**.
    - Rellena los campos siguientes (deja los campos que no se mencionan en blanco):
        - **Timestamp**: PurchasedOn
        - **Actividad del evento**: Visualización del tipo de actividad
        - **Detalles adicionales**: asunto
        - **¿Mostrar esta actividad en la escala de tiempo del perfil de cliente?** Sí
        - **Icono**: selecciona la cesta de compras.
        - **¿Establecer tipos de campo de asignación en los atributos de tu actividad?** Sí, y configurar lo siguiente:
            - **Id. de pedido de ventas**: PurchaseID
            - **Fecha de pedido**: PurchasedOn
            - **Importe de ventas**: TotalPrice

1. Seleccione **Siguiente**.

1. En la pantalla **Configurar relaciones de actividad**, con **Comercio electrónico: compras** seleccionado, selecciona **+ Agregar relación**.

1. En el panel **Agregar ruta de relación**, establece los siguientes valores:
    - **Clave externa**: ContactId
    - **En nombre de la tabla**: contactos: comercio electrónico
    - **Nombre de relación**: eCommPurchasesToContacts
    - Seleccione **Aplicar**.

1. Selecciona **PDV: compras.** Seleccione **+ Agregar relación**.

1. En el panel **Agregar ruta de relación**, establece los siguientes valores:
    - **Clave externa**: LoyaltyId
    - **En nombre de la tabla**: clientes: fidelización
    - **Nombre de la relación**: PoSPurchasesToLoyalty
    - Seleccione **Aplicar**.

1. Seleccione **Siguiente**.

1. Selecciona **Crear actividades.**

1. Espera mientras las **actividades** se actualizan y unifican.



