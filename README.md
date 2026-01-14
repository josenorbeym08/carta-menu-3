# 📚 Flipbook Catálogo Digital Interactivo

Un flipbook HTML5 profesional con efecto de revista interactiva para catálogos de productos, menús digitales y más. Incluye carrito de compras integrado y envío directo por WhatsApp.

## ✨ Características Principales

### 🎨 Diseño y Experiencia
- **Efecto de flip 3D**: Animación profesional tipo revista como AnyFlip
- **Completamente Responsivo**: Funciona perfecto en desktop, tablet y móvil
- **Touch-friendly**: Desliza en móvil para pasar páginas
- **Gradiente Moderno**: Diseño visual atractivo y profesional

### 🛒 Carrito de Compras
- **Agregar/Quitar Productos**: Control de cantidad en cada artículo
- **Edición en Carrito**: Modifica cantidades directamente en el carrito modal
- **Cálculo Automático**: Total actualizado en tiempo real
- **Carrito Flotante**: Badge visual con contador de artículos

### 📱 Funcionalidades de Móvil
- **Gesture Control**: Desliza izquierda/derecha para cambiar páginas
- **Botones Táctiles**: Interfaz optimizada para pantallas táctiles
- **Layouts Adaptativos**: Se ajusta automáticamente a cualquier tamaño de pantalla

### 💬 Integración WhatsApp
- **Envío Directo**: Botón flotante para WhatsApp
- **Mensaje Formateado**: Detalles completos del pedido con emojis
- **Carrito a WhatsApp**: Envía todo tu carrito en un mensaje

## 🚀 Inicio Rápido

### Instalación

1. **Clona el repositorio**
```bash
git clone https://github.com/tu-usuario/flipbook-catalogo.git
cd flipbook-catalogo
```

2. **Abre en tu navegador**
```bash
# Simplemente abre el archivo en tu navegador
# O usa un servidor local:
python -m http.server 8000
# Luego accede a: http://localhost:8000/flipbook.html
```

### Configuración Inicial

1. Abre `flipbook.html` en un editor de texto
2. Busca la línea:
```javascript
const phoneNumber = '5491234567890';
```
3. Reemplaza con tu número de WhatsApp (formato: código país + número sin espacios)

## 📝 Estructura del Proyecto

```
.
├── flipbook.html          # Archivo principal del flipbook
├── README.md              # Este archivo
├── LICENSE                # Licencia del proyecto
└── assets/                # (Opcional) Para agregar imágenes
    ├── images/
    └── favicon.ico
```

## 🎯 Cómo Usar

### Para Usuarios
1. **Hojear el Catálogo**: Usa los botones "Anterior/Siguiente" o desliza en móvil
2. **Seleccionar Cantidad**: Usa +/− para ajustar la cantidad de cada producto
3. **Agregar al Carrito**: Haz clic en el botón "Agregar"
4. **Ver Carrito**: Haz clic en el badge 🛒 en la esquina
5. **Editar Pedido**: Modifica cantidades o elimina productos en el modal del carrito
6. **Enviar Pedido**: Haz clic en "Enviar a WhatsApp"

### Para Desarrolladores

#### Agregar Productos

Edita el objeto `productCategories` en el JavaScript:

```javascript
const productCategories = {
    'Tu Categoría': [
        { name: 'Producto 1', price: 10.00, desc: 'Descripción' },
        { name: 'Producto 2', price: 15.00, desc: 'Descripción' }
    ]
};
```

#### Personalizar Colores

Busca estas líneas en el CSS:
```css
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
color: #667eea;
background: #25d366; /* Color WhatsApp */
```

#### Cambiar Número de WhatsApp

```javascript
const phoneNumber = 'TUNUMERODEWHATSAPP';
```

## 🛠️ Personalización Avanzada

### Modificar Temas de Color

```css
/* Color primario */
--primary: #667eea;

/* Color secundario */
--secondary: #764ba2;

/* Color de acento (WhatsApp) */
--accent: #25d366;
```

### Agregar Más Categorías

```javascript
productCategories['Nueva Categoría'] = [
    { name: 'Producto', price: 0.00, desc: 'Descripción' }
];
```

### Modificar Animaciones

```css
transition: opacity 0.8s cubic-bezier(0.6, 0, 0.4, 1);
/* Ajusta la duración (0.8s) y la curva de animación */
```

## 📊 Características Técnicas

- **HTML5 Semántico**: Estructura limpia y accesible
- **CSS3 Avanzado**: Transforms 3D, Gradientes, Flexbox, Grid
- **JavaScript Vanilla**: Sin dependencias externas
- **Responsive Design**: Mobile-first approach
- **Touch Events**: Soporte completo para dispositivos táctiles
- **LocalStorage Ready**: Preparado para guardar carrito

## 🌐 Compatibilidad

| Navegador | Desktop | Móvil |
|-----------|---------|-------|
| Chrome    | ✅      | ✅    |
| Firefox   | ✅      | ✅    |
| Safari    | ✅      | ✅    |
| Edge      | ✅      | ✅    |
| Opera     | ✅      | ✅    |

## 📱 Responsive Breakpoints

- **Desktop**: > 1024px - 2 columnas de productos
- **Tablet**: 768px - 1024px - 1 columna de productos
- **Móvil**: < 768px - Stack vertical, botones optimizados

## 🎨 Customización Visual

### Cambiar Logo/Título
Busca en el HTML:
```html
<h1>📚 Catálogo Digital</h1>
```

### Cambiar Descripción
```html
<p>Hojea como una revista - Toca/Arrastra para pasar la página</p>
```

### Agregar Favicon
```html
<link rel="icon" type="image/x-icon" href="assets/favicon.ico">
```

## 🔐 Seguridad

- No almacena datos sensibles en el cliente
- WhatsApp API se usa solo para mensajería
- Sin tracking ni cookies no consentidas
- GDPR compliant

## 📈 Optimización SEO

```html
<title>Catálogo Digital - Flipbook Interactivo</title>
<meta name="description" content="Catálogo digital interactivo con carrito de compras">
<meta name="keywords" content="catálogo, flipbook, tienda online">
```

## 🐛 Solución de Problemas

### El flipbook no se ve
- Asegúrate de que el archivo está correctamente nombrado: `flipbook.html`
- Abre la consola del navegador (F12) para ver errores

### WhatsApp no abre
- Verifica que tu número incluya el código de país (ejemplo: +5491234567890)
- Elimina el signo + en la constante: `5491234567890`

### Los productos no aparecen
- Revisa que el objeto `productCategories` esté correctamente formateado
- Asegúrate de que los precios sean números válidos

### Móvil no responde al deslice
- Verifica que el navegador permita eventos touch
- En algunos navegadores, quizás debas actualizar la página

## 🤝 Contribuciones

¡Las contribuciones son bienvenidas! Por favor:

1. Fork el proyecto
2. Crea una rama para tu feature (`git checkout -b feature/AmazingFeature`)
3. Commit tus cambios (`git commit -m 'Add some AmazingFeature'`)
4. Push a la rama (`git push origin feature/AmazingFeature`)
5. Abre un Pull Request

## 📄 Licencia

Este proyecto está bajo la licencia MIT. Ver [LICENSE](LICENSE) para más detalles.

## 📧 Contacto

- **Email**: tu-email@example.com
- **GitHub**: [@tu-usuario](https://github.com/tu-usuario)
- **WhatsApp**: Mensaje desde el flipbook

## 🙏 Agradecimientos

- Inspirado en plataformas como AnyFlip y Issuu
- Iconos de emojis nativos
- Comunidad de desarrollo web

## 📚 Recursos Útiles

- [MDN Web Docs](https://developer.mozilla.org/)
- [CSS Tricks](https://css-tricks.com/)
- [JavaScript.info](https://javascript.info/)
- [WhatsApp Business API](https://www.whatsapp.com/business/)

## 🔮 Futuras Mejoras

- [ ] Agregar soporte para imágenes de productos
- [ ] Implementar búsqueda de productos
- [ ] Agregar filtros por categoría
- [ ] Sistema de favoritos
- [ ] LocalStorage para guardar carrito
- [ ] Modo oscuro
- [ ] Soporte multiidioma
- [ ] Analytics integrado

---

**¡Gracias por usar Flipbook Catálogo Digital!** 

Si te gusta, no olvides dar una ⭐ en GitHub.
