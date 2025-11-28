# Características del Sistema - Vista del Usuario Final

## 🎯 ¿Qué puede hacer el usuario en el sistema?

Este documento describe todas las funcionalidades que el usuario puede ver y usar en la aplicación, explicadas de manera simple y sin términos técnicos.

---

## 🔐 Inicio de Sesión

### Pantalla de Login
- **Ingresar con usuario y contraseña**: El usuario debe ingresar su nombre de usuario y contraseña para acceder al sistema
- **Tres tipos de usuarios**:
  - **Administrador**: Tiene acceso a todas las funciones del sistema
  - **Vendedor**: Puede realizar ventas y consultar información, pero no puede modificar configuraciones
  - **Transportista**: Tiene acceso a un dashboard móvil para gestionar sus envíos asignados

---

## 📊 Pantalla Principal (Dashboard)

### Resumen General
Al ingresar al sistema, el usuario ve un panel con información importante:

- **Total de Productos**: Cuántos productos hay en el catálogo
- **Productos con Stock Bajo**: Cuántos productos necesitan reposición (menos de 5 unidades)
- **Total de Ventas**: Cantidad de ventas realizadas
- **Ingresos Totales**: Dinero total generado por las ventas

### Accesos Rápidos
Botones para ir rápidamente a:
- Gestionar Productos
- Control de Stock
- Nueva Venta

---

## 📦 Gestión de Productos

### Ver Lista de Productos
El usuario puede ver una tabla con todos los productos que incluye:
- Nombre del producto
- Categoría a la que pertenece
- Marca
- Precio de costo
- Precio de venta
- Stock disponible (con colores: verde si hay suficiente, amarillo si está bajo, rojo si está muy bajo)

### Buscar Productos
- **Barra de búsqueda**: Escribir el nombre del producto para encontrarlo rápidamente
- **Filtro por sucursal**: Ver productos de una sucursal específica o de todas

### Agregar Nuevo Producto (Solo Administradores)
Al crear un producto, se puede ingresar:
- Nombre o descripción del producto
- Proveedor que lo suministra
- Categoría (ej: "Electrónica", "Ropa", etc.)
- Subcategoría
- Marca
- Porcentaje de IVA (21%, 10.5%, etc.)
- Precio de costo
- Precio de venta
- Sucursal donde se guardará inicialmente
- Cantidad inicial de stock

### Editar Producto (Solo Administradores)
- Modificar cualquier información del producto
- Cambiar precios
- Actualizar categoría o marca

### Eliminar Producto (Solo Administradores)
- Eliminar productos que ya no se venden
- El sistema pregunta confirmación antes de eliminar

### Funciones Especiales (Solo Administradores)

#### Remarcar Precios
- **Aumentar precios de todos los productos**: Aplicar un porcentaje de aumento a todo el catálogo
- **Aumentar precios por categoría**: Aumentar solo los productos de una categoría específica
- **Aumentar precio de un producto**: Aumentar el precio de un producto individual

#### Aplicar Descuentos
- **Descuento a todos los productos**: Aplicar un porcentaje de descuento a todo el catálogo
- **Descuento por categoría**: Descuento solo a productos de una categoría
- **Descuento a un producto**: Descuento a un producto específico

#### Mover Productos entre Sucursales
- Seleccionar la sucursal de origen (de dónde se sacan los productos)
- Seleccionar la sucursal destino (a dónde se envían)
- Elegir qué productos mover y en qué cantidad
- Agregar un motivo del traslado (opcional)

---

## 📋 Control de Stock

### Ver Stock por Sucursal
- **Seleccionar sucursal**: Ver el stock de una sucursal específica o de todas las sucursales
- **Tabla de stock**: Muestra:
  - Nombre del producto
  - Categoría
  - Sucursal (si se ven todas)
  - Precio de venta
  - Cantidad disponible (con colores indicativos)
  - Botón para actualizar stock

### Buscar Productos en Stock
- Barra de búsqueda para encontrar productos rápidamente

### Actualizar Stock
Al hacer clic en "Actualizar" de un producto, se puede:
- **Tipo de movimiento**:
  - **Ajuste**: Establecer una cantidad específica (útil para inventarios)
  - **Entrada**: Agregar unidades al stock existente
  - **Salida**: Restar unidades del stock existente
- **Cantidad**: Cuántas unidades se agregan, quitan o se establecen
- **Motivo**: Escribir por qué se hace el movimiento (ej: "Reposición", "Ajuste de inventario", "Devolución")

### Actualizaciones en Tiempo Real
- El stock se actualiza automáticamente cuando alguien más hace cambios
- No es necesario recargar la página para ver los cambios

---

## 💰 Sistema de Ventas

### Ver Historial de Ventas
Tabla que muestra:
- Fecha y hora de cada venta
- Sucursal donde se realizó
- Vendedor que la registró
- Total de la venta

### Seleccionar Sucursal
- Elegir la sucursal donde se realizará la venta
- Ver el contador de ventas de esa sucursal

### Realizar una Nueva Venta

#### Paso 1: Seleccionar Productos
- **Buscar productos**: Barra de búsqueda para encontrar productos rápidamente
- **Filtros**:
  - Filtrar por categoría
  - Filtrar por marca
- **Lista de productos disponibles**: Muestra:
  - Nombre del producto
  - Categoría y marca (con etiquetas de colores)
  - Precio de venta
  - Stock disponible (con advertencia si está bajo)
  - Botón "Agregar" para añadir al carrito

#### Paso 2: Carrito de Compras
- **Ver productos agregados**: Lista de todos los productos en el carrito
- **Modificar cantidades**:
  - Botón "-" para reducir cantidad
  - Botón "+" para aumentar cantidad
  - El sistema no permite agregar más de lo que hay en stock
- **Eliminar productos**: Botón para quitar productos del carrito
- **Ver total**: El total se calcula automáticamente y se muestra en grande

#### Paso 3: Datos del Cliente
Información obligatoria que se debe ingresar:
- **Teléfono**: Número de teléfono del cliente
- **DNI o CUIT**: Al menos uno de los dos es obligatorio
  - Si tiene CUIT: se emitirá Factura A
  - Si solo tiene DNI: se emitirá Factura B
- **Nombre completo**: Nombre y apellido del cliente
- **¿Cómo nos conoció?**: Opciones como:
  - Redes sociales
  - Recomendación
  - Búsqueda en internet
  - Publicidad
  - Pasando por el local
  - Otro

#### Paso 4: Confirmar Venta
- Botón "Confirmar Venta" para finalizar
- El sistema:
  - Registra la venta
  - Actualiza el stock automáticamente
  - Genera un remito y la factura en PDF
  - Envía los archivos por WhatsApp al cliente automáticamente
  - Muestra un mensaje de confirmación

### Características del Carrito
- **Validación de stock**: No permite vender más de lo disponible
- **Cálculo automático**: El total se actualiza en tiempo real
- **Advertencias visuales**: Muestra cuando el stock está bajo
- **Cancelar venta**: Opción para cancelar y vaciar el carrito

---

## 📈 Métricas y Reportes (Solo Administradores)

### Panel de Métricas
Vista con gráficos y estadísticas:

#### Tarjetas de Resumen
- **Total de ventas**: Cantidad de ventas en el período seleccionado
- **Ingresos totales**: Dinero total generado
- **Productos vendidos**: Cantidad de productos vendidos
- **Promedio de venta**: Promedio de dinero por venta

#### Filtros
- **Rango de fechas**: Seleccionar desde qué fecha hasta qué fecha
- **Presets rápidos**:
  - Hoy
  - Esta semana
  - Este mes
  - Últimos 7 días
  - Últimos 30 días
- **Filtro por sucursal**: Ver métricas de una sucursal específica o todas

#### Gráficos
- **Gráfico de ventas por día**: Línea que muestra cómo fueron las ventas día a día
- **Gráfico de ventas por sucursal**: Barras comparando ventas entre sucursales
- **Top 10 productos más vendidos**: Gráfico circular mostrando los productos que más se vendieron

### Actualización en Tiempo Real
- Los gráficos se actualizan automáticamente cuando hay nuevas ventas
- No es necesario recargar la página

---

## 🏢 Gestión de Proveedores (Solo Administradores)

### Ver Lista de Proveedores
Tabla con:
- Nombre del proveedor
- Información de contacto
- Cantidad de productos asociados
- Botones para editar, ver marcas y ver cuentas corrientes

### Agregar Nuevo Proveedor
Información que se puede ingresar:
- Nombre del proveedor
- Contacto (nombre de la persona)
- Teléfono
- Email
- Dirección

### Editar Proveedor
- Modificar cualquier información del proveedor

### Eliminar Proveedor
- Eliminar proveedores que ya no se utilizan

### Gestionar Marcas del Proveedor
- **Ver marcas asociadas**: Lista de todas las marcas que tiene ese proveedor
- **Agregar marca existente**: Asociar una marca que ya existe en el sistema
- **Crear nueva marca**: Crear una nueva marca y asociarla al proveedor
- **Eliminar asociación**: Quitar una marca del proveedor

### Cuentas Corrientes con Proveedores
- **Ver cuentas corrientes**: Lista de todas las cuentas corrientes con ese proveedor
- **Crear nueva cuenta corriente**: 
  - Seleccionar productos recibidos
  - Ingresar cantidad y precio de cada producto
  - Agregar observaciones
- **Ver detalle de cuenta**: 
  - Ver todos los productos recibidos
  - Ver todos los pagos realizados
  - Ver comprobantes subidos
  - Ver saldo pendiente
- **Agregar productos a cuenta existente**: Añadir más productos a una cuenta abierta
- **Registrar pagos**: 
  - Ingresar monto pagado
  - Seleccionar método de pago (transferencia, efectivo, etc.)
  - Agregar observaciones
  - Subir comprobante (PDF, imagen)
- **Subir comprobantes**: Adjuntar archivos de comprobantes de pago
- **Cerrar cuenta**: Marcar una cuenta como cerrada cuando está saldada

---

## 🏪 Gestión de Sucursales (Solo Administradores)

### Ver Lista de Sucursales
Tabla con:
- Nombre de la sucursal
- Dirección
- Teléfono
- Estado (activa o inactiva)
- Botones para editar o eliminar

### Agregar Nueva Sucursal
Información que se puede ingresar:
- Nombre de la sucursal
- Dirección
- Teléfono
- Punto de venta (para facturación electrónica)

### Editar Sucursal
- Modificar información de la sucursal
- Activar o desactivar la sucursal

### Eliminar Sucursal
- Eliminar sucursales que ya no se utilizan

---

## 👥 Gestión de Usuarios (Solo Administradores)

### Ver Lista de Usuarios
Tabla con:
- Nombre de usuario
- Nombre completo
- Email
- Rol (Administrador o Vendedor)
- Estado (activo o inactivo)
- Botones para editar

### Agregar Nuevo Usuario
Información que se puede ingresar:
- Nombre de usuario (para iniciar sesión)
- Nombre completo
- Email
- Contraseña
- Rol (Administrador, Vendedor o Transportista)

### Editar Usuario
- Modificar información del usuario
- Cambiar el rol
- Activar o desactivar el usuario

---

## 📁 Gestión de Categorías (Solo Administradores)

### Ver Lista de Categorías
Tabla con:
- Nombre de la categoría
- Descripción
- Botones para editar o eliminar

### Agregar Nueva Categoría
Información que se puede ingresar:
- Nombre de la categoría
- Descripción (opcional)

### Editar Categoría
- Modificar nombre y descripción

### Eliminar Categoría
- Eliminar categorías que ya no se utilizan

---

## 💳 Chequera (Solo Administradores)

La chequera permite llevar un registro completo de todos los cheques emitidos, con la posibilidad de vincularlos a proveedores y realizar búsquedas avanzadas.

### Ver Lista de Cheques
Tabla que muestra todos los cheques registrados con:
- Número de cheque
- Fecha (mostrada como día/mes/año)
- Detalle de la operación
- Saldo o monto del cheque
- Proveedor asociado (si tiene uno)
- Usuario que creó el cheque
- Botones para editar o eliminar

### Crear un Nuevo Cheque
Al hacer clic en "Nuevo Cheque", se abre un modal con diseño de cheque real donde puedes ingresar:

#### Campos del Cheque
- **Número de Cheque**: El número del cheque (obligatorio)
- **Fecha**: Seleccionar la fecha del cheque usando el calendario (obligatorio)
  - La fecha se muestra como día/mes/año
- **Detalle de la Operación**: Descripción o motivo del cheque (opcional)
  - Ejemplo: "Pago a proveedor por mercadería recibida"
- **Saldo**: Monto del cheque en pesos (obligatorio)
  - Se ingresa como número con decimales
- **Proveedor**: Seleccionar un proveedor de la lista (opcional)
  - Si el cheque está relacionado con un proveedor, puedes vincularlo
  - Si no está relacionado con ningún proveedor, puedes dejarlo vacío

#### Diseño del Modal
- El modal tiene un diseño que simula un cheque real
- Líneas punteadas y bordes que recuerdan a un cheque físico
- Campos con líneas para escribir, como en un cheque real

### Editar un Cheque
- Hacer clic en "Editar" en la fila del cheque
- Se abre el mismo modal con los datos cargados
- Modificar cualquier campo
- Guardar los cambios

### Eliminar un Cheque
- Hacer clic en "Eliminar" en la fila del cheque
- El sistema pregunta confirmación antes de eliminar
- Una vez confirmado, el cheque se elimina permanentemente

### Buscar y Filtrar Cheques
El sistema ofrece múltiples formas de encontrar cheques:

#### Búsqueda General
- **Barra de búsqueda**: Escribir cualquier texto para buscar
- Busca en el número de cheque y en el detalle de la operación
- Los resultados se actualizan mientras escribes

#### Filtros Específicos
- **Por número de cheque**: Filtrar cheques por su número específico
- **Por proveedor**: Ver solo los cheques de un proveedor determinado
  - Seleccionar el proveedor del menú desplegable
  - Ver todos los cheques vinculados a ese proveedor
- **Por fecha desde**: Ver cheques desde una fecha específica
  - Seleccionar la fecha inicial del rango
- **Por fecha hasta**: Ver cheques hasta una fecha específica
  - Seleccionar la fecha final del rango

#### Combinar Filtros
- Puedes usar varios filtros al mismo tiempo
- Por ejemplo: buscar cheques de un proveedor específico entre dos fechas
- Los resultados se actualizan automáticamente al cambiar cualquier filtro

### Información Mostrada
Cada cheque en la lista muestra:
- **Número de cheque**: En negrita para fácil identificación
- **Fecha**: Formato día/mes/año (ej: 15/03/2024)
- **Detalle**: Descripción completa de la operación
- **Saldo**: Monto en verde y con formato de moneda (ej: $50.000,00)
- **Proveedor**: Nombre del proveedor si está vinculado, o "-" si no tiene
- **Creado por**: Nombre del usuario que registró el cheque
- **Fecha de creación**: Fecha y hora en que se registró en el sistema

### Ordenamiento
- Los cheques se muestran ordenados por fecha (más recientes primero)
- Si dos cheques tienen la misma fecha, se ordenan por fecha de creación

### Casos de Uso Comunes

#### Registrar un Cheque Emitido
1. Administrador va a "Chequera"
2. Hace clic en "Nuevo Cheque"
3. Ingresa el número del cheque
4. Selecciona la fecha del cheque
5. Escribe el detalle (ej: "Pago a proveedor ABC por factura 12345")
6. Ingresa el monto del cheque
7. Selecciona el proveedor si corresponde
8. Hace clic en "Crear Cheque"
9. El cheque queda registrado y aparece en la lista

#### Buscar un Cheque Específico
1. Administrador va a "Chequera"
2. Escribe el número del cheque en la barra de búsqueda
3. O selecciona el proveedor en el filtro
4. O selecciona el rango de fechas
5. El sistema muestra solo los cheques que coinciden

#### Ver Cheques de un Proveedor
1. Administrador va a "Chequera"
2. Selecciona el proveedor en el filtro "Proveedor"
3. El sistema muestra todos los cheques vinculados a ese proveedor
4. Puede ver el historial completo de pagos con cheques a ese proveedor

#### Ver Cheques de un Período
1. Administrador va a "Chequera"
2. Selecciona "Fecha desde" y "Fecha hasta"
3. El sistema muestra todos los cheques emitidos en ese período
4. Útil para hacer reportes mensuales o anuales

### Ventajas de la Chequera
- **Registro completo**: Todos los cheques quedan registrados en un solo lugar
- **Búsqueda rápida**: Encontrar cualquier cheque en segundos
- **Vinculación con proveedores**: Saber qué cheques están relacionados con cada proveedor
- **Historial**: Ver el historial completo de cheques emitidos
- **Trazabilidad**: Saber quién y cuándo registró cada cheque
- **Filtros avanzados**: Encontrar información específica fácilmente

### Notas Importantes
- Solo los administradores pueden acceder a la chequera
- Los cheques no se pueden modificar después de ser eliminados
- La fecha del cheque puede ser diferente a la fecha en que se registra en el sistema
- El proveedor es opcional, puedes registrar cheques sin vincularlos a un proveedor
- El sistema registra automáticamente quién creó cada cheque

---

## 🎨 Características Generales de la Interfaz

### Menú Lateral
Panel izquierdo con acceso a todas las secciones:
- Dashboard
- Productos
- Stock
- Ventas
- Métricas (solo administradores)
- Categorías (solo administradores)
- Proveedores (solo administradores)
- Sucursales (solo administradores)
- Usuarios (solo administradores)
- Chequera (solo administradores)
- Envíos (solo administradores)

**Nota**: Los transportistas tienen un dashboard móvil especial y no ven este menú lateral

### Información del Usuario
En la parte inferior del menú:
- Nombre del usuario logueado
- Rol del usuario
- Botón para cerrar sesión

### Barra Superior
- Botón para abrir/cerrar el menú (en móviles)
- Fecha actual mostrada en español

### Notificaciones
- **Mensajes de éxito**: Aparecen cuando una operación se completa correctamente (verde)
- **Mensajes de error**: Aparecen cuando algo sale mal (rojo)
- **Mensajes informativos**: Aparecen para dar información importante (azul)

### Actualizaciones Automáticas
- El sistema se actualiza automáticamente cuando hay cambios
- No es necesario recargar la página manualmente
- Los cambios aparecen en tiempo real para todos los usuarios conectados

### Diseño Responsive
- La aplicación se adapta a diferentes tamaños de pantalla
- Funciona bien en computadoras, tablets y celulares
- El menú se oculta automáticamente en pantallas pequeñas

### Búsqueda y Filtrado
- Búsqueda en tiempo real (mientras se escribe)
- Filtros que se pueden combinar
- Resultados que se actualizan automáticamente

### Colores y Alertas Visuales
- **Verde**: Stock suficiente, operación exitosa
- **Amarillo/Naranja**: Stock bajo, advertencia
- **Rojo**: Stock muy bajo o crítico, error
- **Azul**: Información, categorías
- **Morado**: Marcas

---

## 🔄 Flujos de Trabajo Comunes

### Proceso de Venta Completo
1. Usuario hace clic en "Nueva Venta"
2. Selecciona la sucursal
3. Busca y agrega productos al carrito
4. Modifica cantidades si es necesario
5. Hace clic en "Continuar"
6. Completa los datos del cliente
7. Hace clic en "Confirmar Venta"
8. El sistema registra la venta, actualiza el stock y envía el remito por WhatsApp

### Reposición de Stock
1. Usuario va a "Control de Stock"
2. Selecciona la sucursal
3. Busca el producto que necesita actualizar
4. Hace clic en "Actualizar"
5. Selecciona tipo de movimiento (Entrada)
6. Ingresa la cantidad a agregar
7. Escribe el motivo (ej: "Reposición de proveedor")
8. Confirma y el stock se actualiza automáticamente

### Remarcación de Precios
1. Administrador va a "Productos"
2. Hace clic en "Remarcar Precios"
3. Selecciona si quiere remarcar todos, por categoría o un producto individual
4. Ingresa el porcentaje de aumento
5. Confirma y todos los precios se actualizan automáticamente

### Mover Productos entre Sucursales
1. Administrador va a "Productos"
2. Hace clic en "Mover entre Sucursales"
3. Selecciona sucursal origen y destino
4. Agrega los productos que quiere mover y las cantidades
5. Agrega un motivo (opcional)
6. Confirma y el stock se actualiza en ambas sucursales

### Registrar un Cheque
1. Administrador va a "Chequera"
2. Hace clic en "Nuevo Cheque"
3. Completa el número de cheque, fecha, detalle y saldo
4. Selecciona el proveedor si corresponde
5. Hace clic en "Crear Cheque"
6. El cheque queda registrado en el sistema

---

## 📱 Funcionalidades Adicionales

### Envío Automático de Remitos
- Cuando se registra una venta, el sistema genera automáticamente un remito en PDF
- El remito se envía por WhatsApp al número de teléfono del cliente
- El remito incluye toda la información de la venta

### Facturación Electrónica
- El sistema puede generar facturas electrónicas (Factura A o B)
- Las facturas cumplen con los requisitos de AFIP
- Se generan automáticamente con CAE (Código de Autorización Electrónico)
- La factura se envía por WhatsApp al número de teléfono del cliente

### Notificaciones de Estado de Envíos
- Cuando se crea un envío, el cliente recibe automáticamente un mensaje por WhatsApp informando que su pedido está en depósito
- Cada vez que el transportista actualiza el estado del envío, el cliente recibe una notificación automática:
  - Cuando el pedido sale en camino
  - Cuando el transportista llega al destino
  - Cuando el pedido es entregado exitosamente
- Los mensajes incluyen toda la información relevante: dirección, transportista, estado actual
- El cliente siempre está informado sin necesidad de consultar manualmente

### Historial Completo
- Todas las operaciones quedan registradas
- Se puede ver el historial de ventas, movimientos de stock, etc.
- Cada operación tiene fecha, hora y usuario que la realizó

### Seguridad
- Cada usuario tiene su propia cuenta
- Solo los administradores pueden modificar configuraciones importantes
- Los vendedores pueden realizar ventas pero no modificar productos o precios

---

## 💬 Asistente de WhatsApp

El sistema incluye un asistente inteligente disponible por WhatsApp que permite consultar información de productos y stock sin necesidad de abrir la aplicación web.

### ¿Cómo Funciona?
- Simplemente escribes un mensaje al número de WhatsApp del sistema
- El asistente responde automáticamente con la información que necesitas
- Funciona como una conversación normal de WhatsApp
- Está disponible las 24 horas del día

### Buscar Productos
Puedes buscar productos escribiendo mensajes como:
- **"Buscar producto [nombre]"**: Ejemplo: "Buscar producto notebook"
- **"¿Tienen [producto]?"**: Ejemplo: "¿Tienen notebooks?"
- El asistente te mostrará:
  - Lista de productos que coinciden con tu búsqueda
  - Precio de cada producto
  - Stock disponible (con indicadores visuales: ✅ si hay suficiente, ⚠️ si está bajo, 🔴 si está muy bajo)
  - Marca y categoría de cada producto

### Consultar Stock
Puedes preguntar sobre el stock de productos:
- **"¿Qué stock hay de [producto]?"**: Ejemplo: "¿Qué stock hay de x?"
- **"Stock de [producto] en [sucursal]"**: Ejemplo: "Stock de x en Sucursal Centro"
- El asistente te mostrará:
  - Stock disponible en cada sucursal
  - Stock total si no especificas sucursal
  - Indicadores visuales del nivel de stock

### Buscar Productos con Stock Disponible
- **"¿Qué productos hay con stock?"**: Muestra todos los productos que tienen stock disponible
- **"Productos con stock de [categoría]"**: Ejemplo: "Productos con stock de X"
- **"Productos con stock en [sucursal]"**: Ejemplo: "Productos con stock en Sucursal Centro"

### Información de Sucursales
- **"Listar sucursales"**: Muestra todas las sucursales disponibles
- **"¿Qué sucursales hay?"**: Lista todas las sucursales con su dirección y teléfono

### Información de Categorías y Marcas
- **"Listar categorías"**: Muestra todas las categorías de productos disponibles
- **"Listar marcas"**: Muestra todas las marcas disponibles en el catálogo

### Información Detallada de un Producto
- **"Info del producto [ID]"**: Obtiene información completa de un producto específico
- Muestra:
  - Nombre completo del producto
  - Precio de venta
  - Marca y categoría
  - Stock disponible por sucursal
  - Stock total

### Preguntas en Lenguaje Natural
El asistente entiende preguntas escritas de manera natural, como:
- "¿Cuánto cuesta el X?"
- "¿Hay stock de X?"
- "¿Qué productos tienen en la sucursal del centro?"
- "¿Cuáles son los precios de los productos de X?"
- "¿Qué marcas tienen disponibles?"

### Ventajas del Asistente de WhatsApp
- **Acceso rápido**: No necesitas abrir la aplicación web
- **Disponible siempre**: Funciona las 24 horas
- **Fácil de usar**: Solo escribes como en cualquier chat
- **Información actualizada**: Consulta el stock en tiempo real
- **Respuestas inteligentes**: Entiende lo que preguntas aunque no uses palabras exactas

### ¿Quién Puede Usar el Asistente?
- **Clientes**: Pueden consultar productos y precios antes de ir a la sucursal
- **Vendedores**: Pueden consultar stock rápidamente desde su celular
- **Administradores**: Pueden verificar información desde cualquier lugar

### Notas Importantes
- El asistente solo puede **consultar** información, no puede realizar ventas ni modificar datos
- El asistente responde en tiempo real con la información más actualizada del sistema
- Puedes hacer múltiples preguntas en la misma conversación

---

## 🚚 Gestión de Envíos (Solo Administradores)

El sistema permite gestionar envíos y asignarlos a transportistas para realizar entregas a clientes.

### Ver Lista de Envíos
Tabla que muestra todos los envíos con:
- Transportista asignado
- Número de teléfono del cliente
- Dirección de envío
- Estado actual del envío (con colores indicativos)
- Fecha de asignación
- Botones para editar o eliminar

### Crear un Nuevo Envío
Al hacer clic en "Nuevo Envío", se abre un formulario donde puedes ingresar:

#### Campos del Envío
- **Transportista**: Seleccionar el transportista que realizará la entrega (obligatorio)
  - Solo se muestran usuarios con rol "Transportista"
  - Una vez asignado, no se puede cambiar
- **Número de Teléfono del Cliente**: Teléfono del destinatario (obligatorio)
  - Formato: número completo con código de país
  - Ejemplo: 5491123456789
- **Dirección de Envío**: Dirección completa donde se debe entregar (obligatorio)
  - Se puede escribir en varias líneas
  - Incluir calle, número, ciudad, código postal, etc.
- **Observaciones**: Notas adicionales sobre el envío (opcional)
  - Instrucciones especiales, referencias, etc.

### Editar un Envío
- Hacer clic en "Editar" en la fila del envío
- Se puede modificar:
  - Teléfono del cliente
  - Dirección de envío
  - Observaciones
- **No se puede cambiar el transportista** una vez asignado

### Eliminar un Envío
- Hacer clic en "Eliminar" en la fila del envío
- El sistema pregunta confirmación antes de eliminar
- Una vez eliminado, el envío desaparece del sistema

### Filtrar Envíos
- **Por transportista**: Ver solo los envíos de un transportista específico
- **Por estado**: Filtrar por estado del envío:
  - En Depósito
  - En Camino
  - Llegada a Destino
  - Entregado
- **Combinar filtros**: Usar ambos filtros al mismo tiempo

### Estados de Envío
Los envíos tienen 4 estados posibles:
- **En Depósito** (gris): El envío está en el depósito, esperando ser cargado
- **En Camino** (azul): El transportista cargó el pedido y está en camino
- **Llegada a Destino** (amarillo): El transportista llegó al destino
- **Entregado** (verde): El envío fue entregado exitosamente

### Notificaciones Automáticas por WhatsApp
Cuando se crea o actualiza un envío, el sistema envía automáticamente mensajes informativos por WhatsApp al cliente:

#### Mensaje al Crear el Envío
Cuando el administrador crea un nuevo envío, el cliente recibe inmediatamente un mensaje:
- **Estado**: "Tu pedido está en nuestro depósito, listo para ser despachado"
- Incluye la dirección de entrega
- Informa que pronto comenzará su viaje

#### Mensajes al Actualizar el Estado
Cada vez que el transportista actualiza el estado del envío, el cliente recibe un mensaje automático:

1. **Cuando el pedido sale en camino**:
   - Mensaje: "¡Tu Pedido está en Camino!"
   - Incluye dirección de entrega
   - Muestra el nombre del transportista
   - Informa que llegará pronto

2. **Cuando el transportista llega al destino**:
   - Mensaje: "¡Hemos Llegado a tu Dirección!"
   - Incluye la dirección completa
   - Muestra el nombre del transportista
   - Solicita estar disponible para recibir

3. **Cuando el pedido es entregado**:
   - Mensaje: "¡Pedido Entregado Exitosamente!"
   - Confirma la entrega
   - Incluye información del transportista
   - Agradece al cliente

#### Características de los Mensajes
- **Automáticos**: Se envían sin intervención manual
- **Informativos**: Incluyen toda la información relevante del envío
- **Profesionales**: Mensajes claros y amigables
- **En tiempo real**: El cliente recibe la notificación inmediatamente

#### Ventajas para el Cliente
- **Siempre informado**: Sabe en todo momento dónde está su pedido
- **No necesita consultar**: Recibe las actualizaciones automáticamente
- **Transparencia**: Conoce quién está realizando la entrega
- **Preparación**: Puede estar listo cuando el transportista llegue

---

## 📱 Dashboard de Transportista

Los transportistas tienen acceso a un dashboard móvil especial diseñado para usar desde el celular.

### Acceso al Dashboard
- Los transportistas ingresan con su usuario y contraseña
- Automáticamente son redirigidos a su dashboard móvil
- No ven el menú lateral ni las otras secciones del sistema

### Ver Mis Envíos
El dashboard muestra una lista de todos los envíos asignados al transportista:
- Cada envío se muestra en una tarjeta con:
  - Estado actual (con color indicativo)
  - Teléfono del cliente
  - Dirección de envío
  - Fecha de asignación
  - Botón para ver la hoja de ruta completa

### Filtrar Envíos
- Selector en la parte superior para filtrar por estado
- Ver solo envíos en un estado específico
- Ver todos los envíos

### Actualizar Estado del Envío
Cada envío tiene botones para avanzar en el proceso de entrega:

#### Flujo de Estados
1. **"En Depósito"** → Botón: **"🚚 Pedido Cargado y en Camino"**
   - Se muestra cuando el envío está en depósito
   - Al hacer clic, el estado cambia a "En Camino"

2. **"En Camino"** → Botón: **"📍 Llegada a Destino"**
   - Se muestra cuando el envío está en camino
   - Al hacer clic, el estado cambia a "Llegada a Destino"

3. **"Llegada a Destino"** → Botón: **"✅ Entregado"**
   - Se muestra cuando el transportista llegó al destino
   - Al hacer clic, el estado cambia a "Entregado"

4. **"Entregado"** → Mensaje: **"✓ Envío Completado"**
   - Ya no se pueden hacer más cambios
   - El envío está finalizado

### Hoja de Ruta
Al hacer clic en "Ver Hoja de Ruta" de un envío, se abre un modal con:

#### Información Completa
- **Estado Actual**: Muestra el estado actual con color
- **Teléfono del Cliente**: Número completo para contactar
- **Dirección de Envío**: Dirección completa de entrega
- **Observaciones**: Notas adicionales si las hay

#### Botones de Acción
- Los mismos botones para cambiar el estado
- Aparecen en el orden correcto según el estado actual
- Solo se puede avanzar, no retroceder

#### Historial de Estados
- Muestra todos los cambios de estado que ha tenido el envío
- Incluye:
  - Estado anterior y nuevo
  - Fecha y hora del cambio
  - Usuario que realizó el cambio

### Características del Dashboard Móvil
- **Diseño Responsive**: Optimizado para pantallas de celular
- **Fácil de Usar**: Botones grandes y fáciles de tocar
- **Colores Indicativos**: Cada estado tiene un color diferente
- **Información Clara**: Todo lo necesario está visible de un vistazo
- **Actualización en Tiempo Real**: Los cambios se guardan inmediatamente

### Casos de Uso del Transportista

#### Iniciar una Entrega
1. Transportista abre su dashboard
2. Ve el envío asignado en estado "En Depósito"
3. Hace clic en "🚚 Pedido Cargado y en Camino"
4. El estado se actualiza y el botón desaparece
5. Aparece el siguiente botón "📍 Llegada a Destino"

#### Llegar al Destino
1. Transportista llega a la dirección
2. Hace clic en "📍 Llegada a Destino"
3. El estado se actualiza
4. Aparece el botón final "✅ Entregado"

#### Completar la Entrega
1. Transportista entrega el pedido al cliente
2. Hace clic en "✅ Entregado"
3. El envío queda marcado como completado
4. El cliente recibe automáticamente un mensaje de confirmación por WhatsApp
5. Ya no se pueden hacer más cambios

### Notificaciones Automáticas al Cliente
Cada vez que el transportista actualiza el estado del envío, el sistema envía automáticamente un mensaje por WhatsApp al cliente:

#### Cuando Presiona "Pedido Cargado y en Camino"
- El cliente recibe: "¡Tu Pedido está en Camino!"
- Incluye la dirección de entrega
- Muestra el nombre del transportista
- Informa que el pedido está en ruta

#### Cuando Presiona "Llegada a Destino"
- El cliente recibe: "¡Hemos Llegado a tu Dirección!"
- Incluye la dirección completa
- Muestra el nombre del transportista
- Solicita estar disponible para recibir

#### Cuando Presiona "Entregado"
- El cliente recibe: "¡Pedido Entregado Exitosamente!"
- Confirma la entrega completa
- Incluye información del transportista
- Agradece al cliente

#### Características
- **Automático**: No necesitas hacer nada adicional, el mensaje se envía solo
- **Inmediato**: El cliente recibe la notificación al instante
- **Informativo**: Incluye todos los datos relevantes del envío
- **Profesional**: Mensajes claros y amigables

### Ventajas del Sistema de Envíos
- **Seguimiento en Tiempo Real**: El administrador puede ver el estado de cada envío
- **Trazabilidad Completa**: Se registra quién y cuándo cambió cada estado
- **Fácil de Usar**: El transportista solo necesita tocar botones
- **Información Centralizada**: Todos los datos del envío en un solo lugar
- **Historial Completo**: Se guarda el historial de todos los cambios
- **Comunicación Automática**: Los clientes reciben notificaciones automáticas por WhatsApp
- **Transparencia Total**: El cliente siempre sabe dónde está su pedido
- **Mejor Experiencia**: El cliente no necesita llamar para consultar el estado

### Notas Importantes
- Solo los administradores pueden crear y asignar envíos
- Los transportistas solo pueden ver y actualizar sus propios envíos
- No se puede retroceder el estado de un envío (solo avanzar)
- Una vez que un envío está "Entregado", no se puede modificar
- El sistema registra automáticamente quién y cuándo cambió cada estado
- Los mensajes por WhatsApp se envían automáticamente, no requieren acción adicional
- Si hay un error al enviar el mensaje, el estado del envío se actualiza igualmente

---

## 🛍️ Tienda Web Online

El sistema incluye una tienda web pública donde los clientes pueden ver todos los productos disponibles con sus imágenes, precios y stock, sin necesidad de iniciar sesión.

### Acceso a la Tienda
- La tienda está disponible en una dirección web pública
- **No requiere iniciar sesión**: Cualquiera puede ver los productos
- Diseño moderno y fácil de usar
- Funciona perfectamente en computadoras, tablets y celulares

### Página de Inicio
Al entrar a la tienda, verás:

#### Sección Principal (Hero)
- Mensaje de bienvenida
- Botón para ver todos los productos
- Diseño atractivo con colores llamativos

#### Productos Destacados
- Muestra los primeros productos disponibles
- Cada producto se muestra en una tarjeta con:
  - Imagen del producto
  - Nombre del producto
  - Precio destacado
  - Categoría y marca
  - Indicador de stock disponible
- Botón para ver más productos

#### Características de la Tienda
- **Envío Rápido**: Información sobre entregas rápidas y seguras
- **Pago Seguro**: Múltiples formas de pago disponibles
- **Calidad Garantizada**: Productos de la mejor calidad

### Página de Productos
Lista completa de todos los productos disponibles:

#### Ver Productos
- Grid de productos con imágenes
- Cada tarjeta muestra:
  - Imagen principal del producto
  - Nombre completo
  - Precio de venta
  - Categoría (con color distintivo)
  - Marca
  - Stock disponible
  - Badge "En Stock" si hay unidades disponibles

#### Buscar Productos
- **Barra de búsqueda**: Escribe el nombre del producto que buscas
- Los resultados se actualizan mientras escribes
- Busca en el nombre y descripción de los productos

#### Filtrar Productos
Puedes filtrar los productos por:

1. **Por Categoría**: 
   - Selecciona una categoría del menú desplegable
   - Ver solo productos de esa categoría
   - Ejemplo: "Electrónica", "Ropa", etc.

2. **Por Marca**:
   - Selecciona una marca del menú desplegable
   - Ver solo productos de esa marca
   - Ejemplo: "Samsung", "Nike", etc.

3. **Por Sucursal**:
   - Selecciona una sucursal del menú desplegable
   - Ver solo productos disponibles en esa sucursal
   - Útil para saber qué hay disponible cerca de ti

#### Combinar Filtros
- Puedes usar varios filtros al mismo tiempo
- Por ejemplo: buscar "notebook" de la marca "HP" en la "Sucursal Centro"
- Los resultados se actualizan automáticamente
- Botón para limpiar todos los filtros

#### Información Mostrada
Cada producto en la lista muestra:
- **Imagen**: Foto del producto (si está disponible)
- **Nombre**: Descripción completa del producto
- **Precio**: Precio de venta en formato de moneda
- **Categoría**: Etiqueta con color que indica la categoría
- **Marca**: Nombre de la marca
- **Stock**: Cantidad de unidades disponibles
- **Estado**: Badge verde "En Stock" si hay unidades

### Detalle de Producto
Al hacer clic en un producto, verás su página de detalle:

#### Galería de Imágenes
- **Imagen Principal**: Foto grande del producto
- **Miniaturas**: Si el producto tiene varias imágenes, puedes verlas todas
- Hacer clic en una miniatura para verla en grande
- Las imágenes se muestran en alta calidad

#### Información del Producto
- **Nombre Completo**: Descripción completa del producto
- **Precio**: Precio destacado en grande
- **Categoría y Marca**: Etiquetas con colores distintivos
- **Estado de Stock**: 
  - "✓ En Stock" en verde si hay unidades disponibles
  - "Sin Stock" en rojo si no hay unidades
  - Cantidad total disponible

#### Stock por Sucursal
- Muestra el stock disponible en cada sucursal
- Lista todas las sucursales donde hay stock
- Indica cuántas unidades hay en cada una
- Útil para saber dónde está disponible el producto

#### Descripción
- Información adicional sobre el producto
- Características y detalles

#### Botón de Contacto
- Botón para contactar y realizar la compra
- Al hacer clic, puedes obtener información de contacto
- Próximamente: sistema de compra online

### Características de la Tienda Web

#### Diseño Moderno
- Interfaz limpia y profesional
- Colores atractivos y modernos
- Animaciones suaves al pasar el mouse
- Diseño que inspira confianza

#### Responsive (Adaptable)
- **En Computadora**: Grid de 4 columnas, navegación completa
- **En Tablet**: Grid de 2 columnas, menú adaptado
- **En Celular**: Grid de 1 columna, menú hamburguesa
- Se adapta perfectamente a cualquier tamaño de pantalla

#### Navegación Fácil
- Menú superior siempre visible
- Botón "Volver" en las páginas de detalle
- Enlaces claros y fáciles de encontrar
- Footer con información adicional

#### Imágenes de Productos
- **Imagen Principal**: Cada producto puede tener una imagen principal
- **Imágenes Adicionales**: Los productos pueden tener varias imágenes
- **Galería Interactiva**: Ver todas las imágenes en el detalle del producto
- **Fallback**: Si un producto no tiene imagen, se muestra un placeholder

#### Búsqueda y Filtros
- Búsqueda en tiempo real
- Filtros que se pueden combinar
- Resultados que se actualizan automáticamente
- Fácil de limpiar y empezar de nuevo

### Qué Productos se Muestran
La tienda muestra automáticamente:
- **Solo productos con stock**: No se muestran productos sin unidades disponibles
- **Solo productos activos**: No se muestran productos desactivados
- **Con imágenes**: Si el producto tiene imágenes, se muestran
- **Precios actuales**: Los precios mostrados son los más recientes

### Ventajas de la Tienda Web
- **Accesible 24/7**: Disponible en cualquier momento
- **Sin registro**: No necesitas crear una cuenta para ver productos
- **Información completa**: Precios, stock, imágenes, todo en un solo lugar
- **Fácil de usar**: Interfaz intuitiva que cualquiera puede usar
- **Actualizada**: Los productos y precios se actualizan automáticamente
- **Responsive**: Funciona perfectamente en cualquier dispositivo
- **Profesional**: Da una imagen profesional de tu negocio

### Para Administradores
Los administradores pueden:

#### Agregar Imágenes a Productos
1. Ir a la sección "Productos" en el panel de administración
2. Editar un producto
3. Subir imágenes usando la opción de carga de archivos
4. Seleccionar una imagen principal
5. Agregar imágenes adicionales
6. Las imágenes aparecerán automáticamente en la tienda web

#### Gestionar Productos para la Tienda
- Los productos que agregues al sistema aparecerán automáticamente en la tienda
- Solo se muestran productos con stock disponible
- Los precios se actualizan automáticamente
- Las imágenes se muestran si están disponibles

### Casos de Uso

#### Cliente Busca un Producto
1. Cliente entra a la tienda web
2. Usa la barra de búsqueda o los filtros
3. Ve los productos disponibles con imágenes y precios
4. Hace clic en un producto para ver más detalles
5. Ve el stock disponible y las sucursales
6. Contacta para realizar la compra

#### Cliente Explora por Categoría
1. Cliente entra a la tienda web
2. Selecciona una categoría del filtro
3. Ve todos los productos de esa categoría
4. Puede combinar con filtro de marca o sucursal
5. Encuentra el producto que busca

#### Administrador Publica Productos
1. Administrador agrega productos al sistema
2. Sube imágenes de los productos
3. Los productos aparecen automáticamente en la tienda
4. Los clientes pueden verlos inmediatamente

### Notas Importantes
- La tienda es pública, no requiere autenticación
- Solo muestra productos con stock disponible
- Las imágenes son opcionales pero recomendadas
- Los precios se actualizan automáticamente desde el sistema
- El stock mostrado es en tiempo real
- La tienda se adapta a cualquier dispositivo


**Versión del Documento**: 1.0  
**Fecha**: 2024  
**Sistema**: Gestión de Stock Multi-sucursal

