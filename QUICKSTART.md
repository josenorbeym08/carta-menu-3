# 🚀 Guía Rápida de Inicio

## Pasos para Empezar en 5 Minutos

### 1️⃣ Preparar tu Número de WhatsApp

Abre `flipbook.html` con un editor de texto y busca esta línea (aproximadamente en la línea 850):

```javascript
const phoneNumber = '5491234567890';
```

Reemplaza con tu número de WhatsApp:
- **Incluye el código del país** (ejemplo: 54 para Argentina, 34 para España, 1 para USA)
- **Sin espacios ni símbolos especiales**
- **Ejemplo:** `5491123456789`

### 2️⃣ Subir a GitHub

```bash
# 1. Inicializar repositorio
git init

# 2. Agregar todos los archivos
git add .

# 3. Crear primer commit
git commit -m "Primer commit: flipbook interactivo con carrito"

# 4. Agregar repositorio remoto (reemplaza el URL)
git remote add origin https://github.com/tu-usuario/flipbook-catalogo.git

# 5. Subir a GitHub
git branch -M main
git push -u origin main
```

### 3️⃣ Habilitar GitHub Pages (Opcional)

Para que tu flipbook esté disponible en línea:

1. Ve a tu repositorio en GitHub
2. Abre **Settings** → **Pages**
3. Selecciona **Deploy from a branch**
4. Elige **main** branch y **/root** folder
5. Haz clic en **Save**

Tu sitio estará disponible en:
```
https://tu-usuario.github.io/flipbook-catalogo/
```

## 📝 Personalizar Productos

### Agregar Nueva Categoría

En `flipbook.html`, busca `productCategories` y agrega:

```javascript
productCategories['Mi Nueva Categoría'] = [
    { name: 'Producto 1', price: 10.00, desc: 'Descripción del producto' },
    { name: 'Producto 2', price: 15.00, desc: 'Descripción del producto' }
];
```

### Cambiar Colores

En la sección `<style>`, busca:

```css
/* Gradiente de fondo */
background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);

/* Color primario (azul) */
color: #667eea;

/* Color secundario (púrpura) */
background: #764ba2;

/* Color WhatsApp (verde) */
background: #25d366;
```

### Cambiar Título y Descripción

```html
<h1>📚 Tu Título Aquí</h1>
<p>Tu descripción aquí - Toca/Arrastra para pasar la página</p>
```

## 🎯 Características Principales

✅ **20 productos por categoría** (60 total)
✅ **3 categorías** (Bebidas, Postres, Platos)
✅ **Efecto flip 3D** profesional
✅ **Carrito de compras** completo
✅ **Integración WhatsApp** directa
✅ **Responsivo** en todos los dispositivos
✅ **Deslice táctil** en móvil
✅ **Sin dependencias externas** (HTML5 puro)

## 🧪 Pruebas Locales

### Opción 1: Python
```bash
cd "tu-carpeta/carta menu"
python -m http.server 8000
# Abre: http://localhost:8000/flipbook.html
```

### Opción 2: Node.js
```bash
npm install -g http-server
http-server
# Abre: http://localhost:8080/flipbook.html
```

### Opción 3: Directamente en el navegador
Simplemente abre el archivo `flipbook.html` con doble clic

## 📁 Estructura Final

```
tu-proyecto/
├── flipbook.html          ⭐ Archivo principal
├── README.md              📖 Documentación completa
├── QUICKSTART.md          ⚡ Esta guía
├── package.json           📦 Metadatos del proyecto
├── LICENSE                ⚖️ Licencia MIT
└── .gitignore             🚫 Archivos a ignorar
```

## 🎨 Editar en Línea

Si no quieres usar un editor:

1. Ve a tu repositorio en GitHub
2. Haz clic en `flipbook.html`
3. Haz clic en el ícono de lápiz (✏️) para editar
4. Realiza tus cambios
5. Haz clic en **Commit changes**

## 🐛 Solución de Problemas

### WhatsApp no abre
- ✅ Revisa que incluya el código de país
- ✅ Intenta en un dispositivo con WhatsApp instalado

### Los productos no se ven
- ✅ Abre la consola (F12) para ver errores
- ✅ Verifica la sintaxis del JSON

### Página en blanco
- ✅ Espera a que cargue (JavaScript genera contenido)
- ✅ Recarga la página (Ctrl+F5)

## 💡 Consejos Profesionales

1. **Imágenes**: Agrega URLs de productos en los datos
2. **Categorías**: Puedes agregar más de 3 fácilmente
3. **Colores**: Usa [Color Picker](https://htmlcolorcodes.com/) para elegir
4. **SEO**: Actualiza el `<title>` y `<meta>` en el HTML

## 🚀 Próximos Pasos

- [ ] Agregar fotos de productos
- [ ] Crear más categorías
- [ ] Personalizar colores y fuentes
- [ ] Publicar en GitHub Pages
- [ ] Compartir el link en tu negocio

## 📞 Contacto

¿Preguntas o sugerencias?
- 📧 Email: tu-email@example.com
- 💬 Crea un [Issue](https://github.com/tu-usuario/flipbook-catalogo/issues) en GitHub

---

**¡Listo! Tu flipbook está preparado para usar y personalizar.** 🎉
