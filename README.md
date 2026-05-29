# Guía de Despliegue - Norteñita en Vercel

## 📋 Contenido del Proyecto

Tu proyecto incluye:
- **index.html** - Página principal completa con todas las secciones
- **vercel.json** - Configuración para Vercel

## 🚀 Pasos para Desplegar en Vercel

### Opción 1: Despliegue rápido (Recomendado)

1. **Crea una carpeta para tu proyecto**
   ```bash
   mkdir nortenita-web
   cd nortenita-web
   ```

2. **Coloca los archivos**
   - Copia `index.html` en la carpeta
   - Copia `vercel.json` en la carpeta

3. **Sube a GitHub** (necesario para Vercel)
   ```bash
   git init
   git add .
   git commit -m "Inicial: Página Norteñita"
   ```

4. **Crea un repositorio en GitHub**
   - Ve a https://github.com/new
   - Crea un repositorio llamado `nortenita-web`
   - Sube tu código:
   ```bash
   git remote add origin https://github.com/tu-usuario/nortenita-web.git
   git branch -M main
   git push -u origin main
   ```

5. **Despliega en Vercel**
   - Ve a https://vercel.com
   - Inicia sesión (o crea cuenta)
   - Click en "New Project"
   - Importa tu repositorio de GitHub
   - Vercel detectará automáticamente la configuración
   - Click en "Deploy"

### Opción 2: Sin Git (Más fácil)

1. **Directamente en Vercel**
   - Ve a https://vercel.com/new
   - Selecciona "Deploy with GitHub" (o conecta tu cuenta)
   - Arrastra y suelta los archivos
   - Vercel desplegará automáticamente

## ⚙️ Personalización Necesaria

Antes de desplegar, edita `index.html` y actualiza:

### 1. Teléfono y Email
Busca en el archivo y reemplaza:
```html
<p>+54 (381) XXX-XXXX</p>
```
Con tu número real:
```html
<p>+54 (381) 123-4567</p>
```

Y el email:
```html
<p>info@norenita.com</p>
```

### 2. Redes Sociales
Busca la sección de footer y reemplaza los enlaces `#`:
```html
<a href="https://facebook.com/nortenita" title="Facebook">
<a href="https://instagram.com/nortenita" title="Instagram">
<a href="https://wa.me/543811234567" title="WhatsApp">
```

### 3. Dominio Personalizado (Opcional)
Una vez desplegado en Vercel:
1. Ve a los "Settings" de tu proyecto
2. "Domains"
3. Agrega tu dominio (ej: www.nortenita.com)
4. Configura los DNS records según las instrucciones

## 🎨 Cambios de Colores (Opcional)

Si quieres cambiar los colores de la marca, busca en `index.html`:

```css
:root {
    --primary-color: #8B4513;      /* Marrón principal */
    --secondary-color: #D2B48C;    /* Tostado claro */
    --accent-color: #DC143C;       /* Rojo crimson */
    --dark-color: #2C1810;         /* Marrón oscuro */
    --light-color: #F5F5DC;        /* Crema */
}
```

Puedes cambiar estos códigos hexadecimales a cualquier color que prefieras.

## 📱 Características Incluidas

✅ **Responsive Design** - Se ve bien en móviles, tablets y desktop
✅ **Navbar Sticky** - Navegación siempre visible
✅ **Hero Section** - Presentación atractiva
✅ **4 Productos** - Dulce de batata, membrillo, tomate, azúcar
✅ **Galería Visual** - Showcase de productos
✅ **Formulario de Contacto** - Para que clientes te escriban
✅ **Redes Sociales** - Enlaces a tus perfiles
✅ **SEO Básico** - Meta tags y estructura HTML5

## 🔧 Agregar Formulario Funcional

Para que el formulario de contacto envíe emails, puedes:

### Opción A: Formspree (Gratuito)
1. Ve a https://formspree.io
2. Crea una cuenta
3. Crea un nuevo formulario
4. Copia el ID
5. Reemplaza el `<form>` en index.html:
```html
<form action="https://formspree.io/f/TU_ID_AQUI" method="POST">
```

### Opción B: EmailJS
1. Ve a https://www.emailjs.com
2. Sigue el tutorial para integración
3. Agrega el script en el HTML

## 📊 Agregar Imágenes Reales

Para mejorar la página, puedes:

1. **Reemplazar iconos con imágenes**
   ```html
   <img src="https://url-de-imagen.jpg" alt="Producto">
   ```

2. **Usar un CDN de imágenes** (como Cloudinary o imgur)

3. **Comprimir imágenes** para mejor performance

## 📈 Próximos Pasos Recomendados

- [ ] Agregar imágenes reales de productos
- [ ] Integrar formulario de contacto funcional
- [ ] Agregar Google Analytics
- [ ] Comprar dominio propio
- [ ] Agregar más páginas (About, Blog, etc)
- [ ] Implementar tienda online (si deseas vender)

## 🆘 Solución de Problemas

**Problema:** El sitio no carga
- Verifica que los archivos estén en la raíz del repositorio

**Problema:** Los estilos no se aplican
- Limpia caché del navegador (Ctrl+Shift+R)
- Verifica el archivo index.html está íntegro

**Problema:** El formulario no envía
- Implementa Formspree u otro servicio de emails
- Verifica los permisos de CORS

## 📞 Soporte

Para más información sobre Vercel:
- Documentación: https://vercel.com/docs
- GitHub: https://github.com/vercel

¡Tu página Norteñita está lista para desplegarse! 🚀
