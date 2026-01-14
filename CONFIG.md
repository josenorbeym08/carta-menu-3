# Configuración del Flipbook

## Variables Principales

```javascript
// Número de WhatsApp (reemplaza con tu número)
const phoneNumber = '5491234567890';  // Formato: código país + número

// Colores del tema
const colors = {
    primary: '#667eea',      // Azul principal
    secondary: '#764ba2',    // Púrpura
    accent: '#25d366',       // Verde WhatsApp
    light: '#f8f9fa',        // Gris claro
    dark: '#333'             // Gris oscuro
};
```

## Estructura de Productos

Cada producto debe tener:

```javascript
{
    name: 'Nombre del Producto',           // Título visible
    price: 0.00,                           // Precio en decimal
    desc: 'Descripción breve del producto' // Máximo 60 caracteres
}
```

## Ejemplos de Categorías

### Restaurante/Comida
```javascript
'Platos Principales': [ ... ]
'Bebidas': [ ... ]
'Postres': [ ... ]
'Promociones': [ ... ]
```

### Tienda/E-commerce
```javascript
'Hombres': [ ... ]
'Mujeres': [ ... ]
'Niños': [ ... ]
'Accesorios': [ ... ]
```

### Consultorio/Servicios
```javascript
'Consultas Médicas': [ ... ]
'Tratamientos': [ ... ]
'Análisis': [ ... ]
'Paquetes': [ ... ]
```

## Paletas de Colores Recomendadas

### Moderna (Actual)
```css
primary: #667eea
secondary: #764ba2
accent: #25d366
```

### Cálida
```css
primary: #f97316
secondary: #ea580c
accent: #25d366
```

### Fría
```css
primary: #0891b2
secondary: #0369a1
accent: #25d366
```

### Lujo
```css
primary: #7c3aed
secondary: #1e3a8a
accent: #25d366
```

## Redes Sociales Alternativas

Además de WhatsApp, puedes agregar:

```javascript
// Telegram
const telegramUrl = `https://t.me/${phoneNumber}?text=${mensaje}`;

// Email
const emailUrl = `mailto:tu-email@example.com?subject=Pedido&body=${mensaje}`;

// Llamada
const callUrl = `tel:${phoneNumber}`;
```

## Mejoras Futuras

- [ ] Agregar imágenes a los productos
- [ ] Sistema de descuentos/promociones
- [ ] Calificaciones de productos
- [ ] Historial de compras
- [ ] Modo oscuro
- [ ] Soporte multiidioma
- [ ] Búsqueda de productos
- [ ] Filtros avanzados

---

Para más información, lee [README.md](README.md) y [QUICKSTART.md](QUICKSTART.md)
