# 🎨 Guía Visual - Personalización de Norteñita Web

## 📐 Estructura de la Página

Tu página web tiene 6 secciones principales:

```
┌─────────────────────────────────────┐
│     NAVBAR (Navegación fija)        │
│  Norteñita | Productos | Galería   │
└─────────────────────────────────────┘
│                                     │
│       HERO SECTION (Portada)        │
│  Bienvenido a Norteñita             │
│  [Botón: Conoce nuestros productos]│
│                                     │
├─────────────────────────────────────┤
│                                     │
│     PRODUCTOS (4 tarjetas)          │
│  ┌──────────┐ ┌──────────┐         │
│  │ Batata   │ │Membrillo │         │
│  └──────────┘ └──────────┘         │
│  ┌──────────┐ ┌──────────┐         │
│  │ Tomate   │ │ Azúcar   │         │
│  └──────────┘ └──────────┘         │
│                                     │
├─────────────────────────────────────┤
│                                     │
│      GALERÍA (6 elementos)          │
│  Visual showcase de productos       │
│                                     │
├─────────────────────────────────────┤
│                                     │
│    CONTACTO (Formulario + Info)     │
│  Teléfono | Email | Formulario      │
│                                     │
├─────────────────────────────────────┤
│          FOOTER (Pie de página)     │
│  Copyright | Redes Sociales         │
└─────────────────────────────────────┘
```

## 🎯 Secciones Detalladas

### 1️⃣ NAVBAR (Navegación)
**Ubicación:** Arriba de la página (fija al scroll)
**Componentes:**
- Logo de Norteñita (icono + texto)
- Enlaces de navegación (Productos, Galería, Contacto)
- Fondo marrón (#8B4513)

**Para personalizar:**
- Cambiar color: busca `--primary-color: #8B4513;`
- Cambiar logo: edita el icono `<i class="fas fa-jar"></i>`
- Agregar más enlaces: añade en `<li><a href="#">`

---

### 2️⃣ HERO SECTION (Portada)
**Ubicación:** Primera sección visible
**Componentes:**
- Titulo grande: "Bienvenido a Norteñita"
- Subtitulo descriptivo
- Botón de acción rojo

**Para personalizar:**
```html
<h1>Tu título aquí</h1>
<p>Tu descripción aquí</p>
```

---

### 3️⃣ PRODUCTOS (4 Tarjetas)
**Ubicación:** Segunda sección (fondo crema)
**Componentes por tarjeta:**
- Icono (Font Awesome)
- Nombre del producto
- Descripción corta

**Productos actuales:**
1. 🍬 Dulce de Batata
2. 🍎 Dulce de Membrillo
3. 🍅 Tomate Triturado
4. 🟨 Azúcar

**Para agregar/editar productos:**
```html
<div class="producto-card">
    <div class="producto-icon">
        <i class="fas fa-icono"></i>
    </div>
    <h3>Nombre del Producto</h3>
    <p>Descripción del producto</p>
</div>
```

**Iconos Font Awesome disponibles:**
- `fa-candy-cane` (caramelo)
- `fa-apple-alt` (manzana/fruta)
- `fa-tomato` (tomate)
- `fa-cube` (caja)
- `fa-jar` (frasco)
- `fa-heart` (corazón)

---

### 4️⃣ GALERÍA
**Ubicación:** Tercera sección (fondo blanco)
**Componentes:**
- 6 elementos visuales con iconos
- Efecto hover (se agrandan)

**Para personalizar:**
```html
<div class="galeria-item">
    <i class="fas fa-icono"></i>
</div>
```

O reemplazar con imágenes:
```html
<div class="galeria-item">
    <img src="tu-imagen.jpg" alt="Descripción">
</div>
```

---

### 5️⃣ CONTACTO
**Ubicación:** Cuarta sección (fondo marrón oscuro)
**Componentes:**
- Información de contacto (Dirección, Teléfono, Email)
- Formulario de contacto (Nombre, Email, Mensaje)

**Para actualizar contacto:**
```html
<p>+54 (381) TU-NUMERO</p>
<p>tu-email@nortenita.com</p>
<p>Tu dirección aquí</p>
```

**Para habilitar el formulario:**
1. Ve a https://formspree.io
2. Crea un formulario
3. Obtén el ID
4. Reemplaza en el HTML:
```html
<form action="https://formspree.io/f/TU_ID" method="POST">
```

---

### 6️⃣ FOOTER
**Ubicación:** Pie de página
**Componentes:**
- Copyright
- Descripción
- Enlaces a redes sociales

**Para actualizar redes sociales:**
```html
<a href="https://facebook.com/nortenita">
    <i class="fab fa-facebook"></i>
</a>
<a href="https://instagram.com/nortenita">
    <i class="fab fa-instagram"></i>
</a>
<a href="https://wa.me/5438XXXXXXXXX">
    <i class="fab fa-whatsapp"></i>
</a>
```

---

## 🎨 Paleta de Colores Actual

| Elemento | Color | Código |
|----------|-------|--------|
| Principal | Marrón | #8B4513 |
| Secundario | Tostado | #D2B48C |
| Acento | Rojo | #DC143C |
| Oscuro | Marrón Oscuro | #2C1810 |
| Claro | Crema | #F5F5DC |

**Para cambiar toda la paleta:** Busca `:root {` en el CSS y edita los códigos.

---

## 📱 Diseño Responsivo

La página se adapta automáticamente a:
- 📱 Móviles (320px - 768px)
- 📱 Tablets (768px - 1024px)
- 💻 Desktop (1024px+)

**Breakpoint principal:** 768px
```css
@media (max-width: 768px) {
    /* Estilos para móviles */
}
```

---

## 🔤 Textos Actualizables

**En el HTML busca y reemplaza:**

```html
<!-- Título principal -->
<h1>Bienvenido a Norteñita</h1>

<!-- Subtítulo -->
<p>Productos alimenticios premium elaborados con tradición y calidad</p>

<!-- Nombre de productos y descripciones -->
<h3>Dulce de Batata</h3>
<p>Elaborado con batata fresca...</p>

<!-- Información de contacto -->
<p>+54 (381) XXX-XXXX</p>
<p>info@nortenita.com</p>

<!-- Footer -->
<p>&copy; 2024 Norteñita. Todos los derechos reservados.</p>
```

---

## ⚡ Optimizaciones Recomendadas

### Velocidad
- [ ] Optimizar imágenes (comprimir a máximo 100KB)
- [ ] Usar WebP en lugar de JPG
- [ ] Implementar lazy loading para imágenes

### SEO
- [ ] Agregar palabras clave en meta tags
- [ ] Crear sitemap.xml
- [ ] Agregar robots.txt
- [ ] Implementar Open Graph (para redes sociales)

### Seguridad
- [ ] Usar HTTPS (Vercel lo hace automáticamente)
- [ ] Agregar CSP headers
- [ ] Validar formularios en cliente y servidor

---

## 🚀 Mejoras Futuras

1. **E-commerce**
   - Agregar carrito de compras
   - Integrar pasarela de pagos

2. **Blog**
   - Sección de recetas con tus productos
   - Historias de la empresa

3. **Newsletter**
   - Formulario de suscripción
   - Email marketing

4. **Admin Panel**
   - Gestionar productos
   - Ver contactos

5. **App Móvil**
   - Versión nativa iOS/Android

---

## 🎓 Recursos Útiles

- **Font Awesome Icons:** https://fontawesome.com/icons
- **Color Picker:** https://htmlcolorcodes.com
- **Optimizar Imágenes:** https://tinypng.com
- **Validar HTML:** https://validator.w3.org
- **CSS Referencia:** https://developer.mozilla.org/es/docs/Web/CSS

---

## 💡 Tips Finales

1. **Mantén el móvil en mente** - 80% de visitantes usan móvil
2. **Textos claros y concisos** - Máximo 2 líneas por sección
3. **Imágenes de calidad** - Son la cara de tu marca
4. **CTA claros** - Botones obvios para que hagan clic
5. **Velocidad** - Comprime todo lo posible

¡Tu página está lista para el éxito! 🎉
