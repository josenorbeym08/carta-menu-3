# 📤 Guía Completa para Subir a GitHub

## Requisitos Previos

1. **Git instalado**: Descárgalo desde [git-scm.com](https://git-scm.com/)
2. **Cuenta GitHub**: Crea una en [github.com](https://github.com)
3. **Editor de texto**: VSCode, Notepad++, etc.

## Paso 1: Configurar Git (Primera Vez)

```bash
# Configura tu nombre
git config --global user.name "Tu Nombre"

# Configura tu email (el mismo de GitHub)
git config --global user.email "tu-email@example.com"

# Verifica la configuración
git config --global --list
```

## Paso 2: Crear Repositorio en GitHub

1. Ve a [github.com/new](https://github.com/new)
2. **Repository name**: `flipbook-catalogo`
3. **Description**: "Catálogo digital interactivo con carrito y WhatsApp"
4. Selecciona **Public** (para que sea visible)
5. Haz clic en **Create repository**
6. Copia el URL (ejemplo: `https://github.com/tu-usuario/flipbook-catalogo.git`)

## Paso 3: Subir Desde la Carpeta Local

Abre PowerShell o CMD en tu carpeta del proyecto:

```powershell
# 1. Navega a la carpeta (reemplaza con tu ruta)
cd "C:\Users\josen\Documents\cursor-python_acad\carta menu"

# 2. Inicializa el repositorio local
git init

# 3. Agrega todos los archivos
git add .

# 4. Crea el primer commit
git commit -m "Inicial: Flipbook interactivo con 20 productos por categoría, carrito y WhatsApp"

# 5. Renombra la rama a main
git branch -M main

# 6. Agrega el repositorio remoto (reemplaza con tu URL)
git remote add origin https://github.com/tu-usuario/flipbook-catalogo.git

# 7. Sube los cambios
git push -u origin main
```

## Paso 4: Verificar en GitHub

1. Ve a tu repositorio en GitHub
2. Deberías ver todos tus archivos subidos
3. Verifica que `flipbook.html` esté presente

## Futuros Cambios (Después del Primer Push)

Para hacer cambios y subirlos:

```powershell
# 1. Navega a la carpeta
cd "C:\Users\josen\Documents\cursor-python_acad\carta menu"

# 2. Ver cambios
git status

# 3. Agregar cambios
git add .

# 4. Crear commit
git commit -m "Descripción de los cambios"

# 5. Subir
git push
```

## Habilitar GitHub Pages

Para que tu flipbook sea accesible en línea sin servidor:

1. Ve a tu repo → **Settings**
2. Busca **Pages** en el menú izquierdo
3. Bajo "Build and deployment":
   - **Source**: Deploy from a branch
   - **Branch**: main
   - **Folder**: / (root)
4. Haz clic en **Save**

Tu sitio estará en: `https://tu-usuario.github.io/flipbook-catalogo/`

### Esperar Despliegue

- La primera vez tarda 1-5 minutos
- Verás un checkmark verde cuando esté listo
- Recarga la página para ver el progreso

## Agregar Dominio Personalizado (Opcional)

Si tienes tu propio dominio:

1. En GitHub Pages settings, ingresa tu dominio bajo "Custom domain"
2. En tu proveedor DNS, agrega:
   ```
   CNAME: tu-usuario.github.io
   ```
3. Espera 24-48 horas para que se propague

## Estructura Final en GitHub

```
tu-usuario/flipbook-catalogo/
├── flipbook.html              ⭐ Tu flipbook
├── index.html                 (antiguo, mantener para referencia)
├── main.py                    (puedes eliminar)
├── README.md                  📖 Documentación
├── QUICKSTART.md              ⚡ Inicio rápido
├── CONFIG.md                  ⚙️ Configuración
├── GITHUB.md                  (este archivo)
├── LICENSE                    ⚖️ Licencia MIT
├── package.json               📦 Metadata
├── .gitignore                 🚫 Archivos ignorados
└── .github/
    └── workflows/
        └── deploy.yml         🤖 Deploy automático
```

## Errores Comunes

### "fatal: not a git repository"
```bash
# Solución: Navega a la carpeta correcta
cd "tu-ruta-correcta"
git init
```

### "Permission denied (publickey)"
```bash
# Solución: Configura SSH
# Ve a: GitHub Settings → Developer settings → Personal access tokens
# Copia el token y usa:
git remote set-url origin https://tu-token@github.com/usuario/repo.git
```

### "remote origin already exists"
```bash
# Solución: Elimina y re-agrega
git remote remove origin
git remote add origin https://github.com/usuario/repo.git
```

### Los cambios no aparecen en GitHub Pages
```bash
# Solución: Verifica que esté en la rama main
git status  # Debe decir "On branch main"

# Si está en otra rama:
git checkout main
git push origin main
```

## Colaboración (Compartir con Equipo)

### Agregar Colaboradores

1. **Settings** → **Collaborators**
2. Haz clic en **Add people**
3. Busca al usuario y haz clic en **Select**

### Clonar Repositorio (Para Otros)

```bash
git clone https://github.com/tu-usuario/flipbook-catalogo.git
cd flipbook-catalogo
```

## Buenas Prácticas

✅ **DO:**
- Hacer commits frecuentes y descriptivos
- Usar ramas para features importantes
- Escribir mensajes claros

❌ **DON'T:**
- Subir datos sensibles (passwords, tokens)
- Hacer commits gigantes sin descripción
- Olvidar hacer push

## Mensajes de Commit Recomendados

```bash
# Agregar productos
git commit -m "Agregar 20 nuevos productos a categoría Bebidas"

# Cambiar colores
git commit -m "Personalizar colores del tema a azul/verde"

# Corregir bug
git commit -m "Corregir error del carrito en móvil"

# Actualizar documentación
git commit -m "Actualizar README con instrucciones de instalación"
```

## URLs Útiles

- 🏠 Tu repositorio: `https://github.com/tu-usuario/flipbook-catalogo`
- 🌐 Tu sitio: `https://tu-usuario.github.io/flipbook-catalogo/flipbook.html`
- 📚 Docs de Git: `https://git-scm.com/doc`
- 🐙 GitHub Help: `https://docs.github.com`

## Próximos Pasos

1. ✅ Configura Git
2. ✅ Crea el repositorio
3. ✅ Sube los archivos
4. ✅ Habilita GitHub Pages
5. ✅ Personaliza tu flipbook
6. ✅ Comparte el link

---

¿Necesitas ayuda? Abre un [Issue](https://github.com) o consulta la documentación oficial.

**¡Tu flipbook estará en línea en minutos!** 🚀
