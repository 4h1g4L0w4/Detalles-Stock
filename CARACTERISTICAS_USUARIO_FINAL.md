# Características del Sistema - Vista del Usuario Final

## 🎯 ¿Qué puede hacer el usuario en el sistema?

Este documento describe todas las funcionalidades que el usuario puede ver y usar en la aplicación, explicadas de manera simple y sin términos técnicos.

---

## 🔐 Inicio de Sesión

### Pantalla de Login
- **Ingresar con usuario y contraseña**: El usuario debe ingresar su nombre de usuario y contraseña para acceder al sistema
- **Dos tipos de usuarios**:
  - **Administrador**: Tiene acceso a todas las funciones del sistema
  - **Vendedor**: Puede realizar ventas y consultar información, pero no puede modificar configuraciones

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
- Rol (Administrador o Vendedor)

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


**Versión del Documento**: 1.0  
**Fecha**: 2024  
**Sistema**: Gestión de Stock Multi-sucursal

