# Carrito SV - Carrito de Supermercado

Aplicación web progresiva (PWA) para gestionar compras de supermercado en Venezuela.

## Características

- **Módulo de Facturación**: Agrega productos y controla tu total antes de pagar
- **Buscador en tiempo real**: Escribe y filtra productos instantáneamente
- **Gestión de inventario**: Agrega, edita y elimina productos
- **Escáner de códigos de barras**: Escanea productos y busca información en línea
- **Precio en USD y BS**: Totas en dólares y bolívares con tasa de cambio automática
- **100% Offline**: Funciona sin internet una vez cargada (usa localStorage)

## Cómo usarla

1. Abre la URL de la app en tu navegador móvil
2. Ve a la pestaña **Inventario** para agregar productos
3. En **Facturación** usa el buscador para agregar productos a tu carrito
4. Ajusta cantidades con los botones + y -
5. Mira el total en USD y BS al final

## Desplegar en GitHub Pages

1. Sube todos los archivos a un repositorio
2. Ve a **Settings** → **Pages**
3. En "Source" selecciona **Deploy from a branch**
4. En "Branch" selecciona **main** y guarda
5. Tu app estará disponible en `tu-usuario.github.io/repositorio`

## Tecnologías

- HTML5, CSS3, JavaScript (Vanilla)
- Service Worker para PWA
- API de Open Food Facts para información de productos
- localStorage para persistencia de datos

## Licencia

MIT