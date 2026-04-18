# Especificación - Carrito de Supermercado

## 1. Project Overview
- **Nombre**: Carrito SV (Carrito de Supermercado Venezuela)
- **Tipo**: WebApp móvil progresiva (PWA)
- **Propósito**: Aplicación para móviles que permite llevar un registro de productos de supermercado, calculando el total en dólares y bolivares antes de pagar
- **Usuario objetivo**: Consumidores venezolanos

## 2. UI/UX Specification

### Layout Structure
- **Diseño**: Mobile-first, orientado a pantalla vertical
- **Navegación**: Tabsinferior con 2 módulos (Facturación, Inventario)
- **Header**: Título de la sección actual con botón de tasa de cambio

### Visual Design
- **Paleta de colores**:
  - Primario: #2563eb (azul)
  - Secundario: #10b981 (verde esmeralda)
  - Fondo: #f8fafc
  - Cards: #ffffff
  - Texto: #1e293b
  - Acento: #f59e0b (naranja)
- **Tipografía**: 
  - Font family: system-ui, -apple-system, sans-serif
  - Títulos: 20px bold
  - Cuerpo: 16px
  - Detalles: 14px
- **Spacing**: 8px base (múltiplos de 8)
- **Border radius**: 12px para cards, 8px para botones

### Componentes
- **Tabs de navegación**: 2 botones inferiores (Facturación, Inventario)
- **Buscador**: Input con sugerencias en tiempo real
- **Lista de productos**: Cards con nombre, cantidad, precio unitario, total
- **Modal de cantidad**: Para ajustar cantidad de productos
- **Botones de acción**: Plus/minus para cantidad, delete

## 3. Funcionalidad Specification

### Módulo Facturación (Principal)
- Buscador en tiempo real que filtra productos del inventario
- Al escribir, muestra coincidencias progresivas
- Click en producto lo agrega a la factura
- Cada producto muestra: nombre, cantidad (+/-), precio unitario, precio total
- Total en dólares y convertir a Bs. con tasa actual
- Botón para limpiar factura
- Botón para ver tasa de cambio

### Módulo Inventario
- Formulario para agregar producto:
  - Nombre del producto
  - Precio en dólares
  - Código de barras (opcional)
- Escáner de código de barras:
  - Usa cámara del dispositivo
  - Al detectar código, busca info del producto en línea
- Edición de productos existentes
- Eliminación de productos
- Persistencia en localStorage

### Tasa de Cambio
- Obtener tasa actual del BCV (Banco Central de Venezuela)
- Alternativa: API de tasa de cambio
- Mostrar tasa en header
- Actualizar automáticamente cada hora

## 4. Acceptance Criteria
- [ ] La app se ve correctamente en móvil (viewport vertical)
- [ ] El buscador filtra productos mientras el usuario escribe
- [ ] Los productos agregados muestran cantidad editable
- [ ] El total se calcula correctamente en USD y BS
- [ ] El inventario permite agregar/editar/eliminar productos
- [ ] El escáner de códigos de barras funciona
- [ ] Los datos persisten al recargar la página
- [ ] La tasa de cambio se obtiene de internet