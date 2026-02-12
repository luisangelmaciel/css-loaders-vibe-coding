# ⚡ CSS Loaders Profesionales - Vibe Coding

<div align="center">

![CSS Loaders Banner](https://img.shields.io/badge/CSS-Loaders-000000?style=for-the-badge&logo=css3&logoColor=white)
![Version](https://img.shields.io/badge/version-1.0.0-brightgreen?style=for-the-badge)
![License](https://img.shields.io/badge/license-MIT-blue?style=for-the-badge)
![No Dependencies](https://img.shields.io/badge/dependencies-0-success?style=for-the-badge)

**Colección curada de 9 loaders ultra-ligeros con CSS puro**

[Demo en Vivo](https://vibecoding.dev/css-loaders) • [Documentación](#documentación) • [Contribuir](#contribuir)

</div>

---

## 📋 Tabla de Contenidos

- [Características](#-características)
- [Demo Interactiva](#-demo-interactiva)
- [Instalación](#-instalación)
- [Uso Rápido](#-uso-rápido)
- [Galería de Loaders](#-galería-de-loaders)
- [Personalización](#-personalización)
- [Performance](#-performance)
- [Accesibilidad](#-accesibilidad)
- [Navegadores Soportados](#-navegadores-soportados)
- [Contribuir](#-contribuir)
- [Licencia](#-licencia)

---

## ✨ Características

- ✅ **0 Dependencias JavaScript** - CSS puro, sin librerías externas
- ✅ **Ultra-ligero** - Menos de 2KB por loader
- ✅ **100% Responsive** - Funciona en cualquier dispositivo
- ✅ **Performance Superior** - Optimizado con GPU acceleration
- ✅ **Accesible** - Compatible con lectores de pantalla
- ✅ **Personalizable** - Fácil de adaptar a tu marca
- ✅ **Moderno** - Utiliza las últimas características de CSS
- ✅ **Copy & Paste** - Listo para usar en segundos
- ✅ **SEO Friendly** - Metadatos optimizados incluidos

---

## 🎯 Demo Interactiva

Visita nuestra [página de demostración](https://vibecoding.dev/css-loaders) para ver todos los loaders en acción y copiar el código directamente.

**Características de la demo:**
- Vista previa en tiempo real de cada loader
- Selector interactivo con hover effects
- Código completo HTML + CSS para cada loader
- Botones de copiar y descargar
- Guía de implementación paso a paso

---

## 🚀 Instalación

### Opción 1: Descarga Directa

Clona el repositorio:

```bash
git clone https://github.com/vibecoding/css-loaders.git
cd css-loaders
```

### Opción 2: CDN

Incluye el CSS en tu HTML:

```html
<link rel="stylesheet" href="https://cdn.vibecoding.dev/loaders.css">
```

### Opción 3: NPM (próximamente)

```bash
npm install @vibecoding/css-loaders
```

---

## 💡 Uso Rápido

### Método 1: HTML + CSS Inline

```html
<!-- HTML -->
<div class="loader loader-1"></div>

<!-- CSS -->
<style>
  .loader {
    width: 40px;
    height: 40px;
    position: relative;
  }
  /* Agrega el CSS específico del loader que elijas */
</style>
```

### Método 2: Clases CSS Externas

1. Incluye el archivo CSS en tu proyecto
2. Agrega el div con la clase correspondiente

```html
<link rel="stylesheet" href="path/to/loaders.css">
<div class="loader loader-spinning-circle"></div>
```

### Método 3: Framework Integration

**React:**
```jsx
const Loader = () => (
  <div className="loader loader-1" role="status">
    <span className="visually-hidden">Cargando...</span>
  </div>
);
```

**Vue:**
```vue
<template>
  <div class="loader loader-1" role="status">
    <span class="visually-hidden">Cargando...</span>
  </div>
</template>
```

---

## 🎨 Galería de Loaders

### 1. Spinning Circle
Loader circular con animación de rotación suave.
- **Uso ideal:** Operaciones de carga general
- **Performance:** Excelente
- **Personalización:** Alta

### 2. 3D Flaps
Efecto 3D con perspectiva y transformaciones.
- **Uso ideal:** Aplicaciones modernas, dashboards
- **Performance:** Muy buena
- **Personalización:** Media

### 3. Map Pin
Animación de pin de mapa con rebote.
- **Uso ideal:** Aplicaciones de geolocalización
- **Performance:** Excelente
- **Personalización:** Alta

### 4. Rotating Dots
Dos puntos que rotan alrededor de un eje.
- **Uso ideal:** Sincronización, procesos duales
- **Performance:** Excelente
- **Personalización:** Alta

### 5. Bouncing Dots
Puntos que rebotan verticalmente.
- **Uso ideal:** Carga de mensajes, chat
- **Performance:** Excelente
- **Personalización:** Alta

### 6. Pac-Man
Clásico Pac-Man comiendo puntos.
- **Uso ideal:** Aplicaciones divertidas, gaming
- **Performance:** Muy buena
- **Personalización:** Media

### 7. Progress Bar
Barra de progreso con animación de relleno.
- **Uso ideal:** Cargas con porcentaje conocido
- **Performance:** Excelente
- **Personalización:** Alta

### 8. Ripple Drop
Efecto de gota con ondas expansivas.
- **Uso ideal:** Actualizaciones, refresh
- **Performance:** Muy buena
- **Personalización:** Media

### 9. Orbital
Sistema orbital con múltiples elementos.
- **Uso ideal:** Procesos complejos, análisis
- **Performance:** Muy buena
- **Personalización:** Media

---

## 🎨 Personalización

### Cambiar Colores

Simplemente reemplaza `#ffffff` en el CSS:

```css
/* Original */
background: #ffffff;

/* Tu color de marca */
background: #ff6b6b;
```

### Ajustar Tamaño

Modifica las propiedades `width` y `height`:

```css
.loader {
  width: 60px;   /* Tamaño deseado */
  height: 60px;  /* Tamaño deseado */
  position: relative;
}
```

### Velocidad de Animación

Cambia `animation-duration`:

```css
/* Más rápido */
animation-duration: 1s;

/* Más lento */
animation-duration: 4s;
```

### Tema Oscuro/Claro

```css
/* Tema oscuro */
.loader::before { background: #ffffff; }

/* Tema claro */
.loader::before { background: #000000; }
```

---

## ⚡ Performance

### Optimizaciones Aplicadas

- ✅ **GPU Acceleration**: Uso de `transform` y `opacity`
- ✅ **Will-change**: Pre-optimización de propiedades animadas
- ✅ **Render Layers**: Aislamiento de capas de renderizado
- ✅ **CSS Containment**: Mejora de painting performance

### Benchmarks

| Loader | FPS Promedio | CPU Usage | Repaints/seg |
|--------|--------------|-----------|--------------|
| Spinning Circle | 60 | 2-3% | 0 |
| 3D Flaps | 60 | 3-4% | 0 |
| Map Pin | 60 | 2-3% | 0 |
| Rotating Dots | 60 | 2-3% | 0 |
| Bouncing Dots | 60 | 2-3% | 0 |

### Mejores Prácticas

```css
/* ✅ BUENO - Usa transform */
.loader {
  transform: translateX(10px);
}

/* ❌ MALO - Evita left/top */
.loader {
  left: 10px;
}
```

---

## ♿ Accesibilidad

### Implementación Recomendada

```html
<div class="loader loader-1" role="status" aria-label="Cargando contenido">
  <span class="visually-hidden">Cargando...</span>
</div>
```

### CSS para Texto Invisible

```css
.visually-hidden {
  position: absolute;
  width: 1px;
  height: 1px;
  padding: 0;
  margin: -1px;
  overflow: hidden;
  clip: rect(0, 0, 0, 0);
  white-space: nowrap;
  border-width: 0;
}
```

### Soporte para `prefers-reduced-motion`

```css
@media (prefers-reduced-motion: reduce) {
  .loader,
  .loader::before,
  .loader::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
  }
}
```

---

## 🌐 Navegadores Soportados

| Navegador | Versión Mínima |
|-----------|----------------|
| Chrome | 90+ |
| Firefox | 88+ |
| Safari | 14+ |
| Edge | 90+ |
| Opera | 76+ |
| Samsung Internet | 14+ |

**Nota:** Para navegadores más antiguos, se mostrarán versiones simplificadas sin animaciones 3D complejas.

---

## 📁 Estructura del Proyecto

```
css-loaders-vibe-coding/
├── index.html              # Página de demostración completa
├── README.md               # Este archivo
├── LICENSE                 # Licencia MIT
├── CONTRIBUTING.md         # Guía de contribución
├── css/
│   ├── loaders.css        # Todos los loaders (minificado)
│   └── individual/        # Loaders individuales
│       ├── loader-1.css
│       ├── loader-2.css
│       └── ...
├── js/
│   └── demo.js            # JavaScript para la demo
├── docs/
│   ├── customization.md   # Guía de personalización
│   ├── performance.md     # Métricas de performance
│   └── accessibility.md   # Guía de accesibilidad
└── examples/
    ├── react/             # Ejemplos para React
    ├── vue/               # Ejemplos para Vue
    └── vanilla/           # Ejemplos vanilla JS
```

---

## 🤝 Contribuir

¡Las contribuciones son bienvenidas! Por favor lee nuestro [CONTRIBUTING.md](CONTRIBUTING.md) para detalles sobre nuestro código de conducta y el proceso para enviar pull requests.

### Cómo Contribuir

1. Fork el proyecto
2. Crea tu rama de feature (`git checkout -b feature/NuevoLoader`)
3. Commit tus cambios (`git commit -m 'Agrega nuevo loader increíble'`)
4. Push a la rama (`git push origin feature/NuevoLoader`)
5. Abre un Pull Request

### Reportar Bugs

Abre un [issue](https://github.com/vibecoding/css-loaders/issues) con:
- Descripción clara del problema
- Pasos para reproducir
- Navegador y versión
- Screenshots si es posible

---

## 📊 Roadmap

- [ ] Agregar 10 loaders adicionales
- [ ] Paquete NPM
- [ ] Generador de loaders personalizado
- [ ] Soporte para Tailwind CSS
- [ ] Plugin para Figma
- [ ] Variantes de color predefinidas
- [ ] Animaciones con Intersection Observer
- [ ] Documentación en inglés

---

## 🙏 Agradecimientos

- Inspirado por la comunidad de Vibe Coding
- Diseños basados en las mejores prácticas de UX
- Optimizaciones de performance gracias a feedback de la comunidad

---

## 📄 Licencia

Este proyecto está bajo la Licencia MIT - ver el archivo [LICENSE](LICENSE) para más detalles.

---

## 📞 Contacto

- Website: [vibecoding.dev](https://vibecoding.dev)
- GitHub: [@vibecoding](https://github.com/vibecoding)
- Twitter: [@vibecoding](https://twitter.com/vibecoding)
- Discord: [Únete a la comunidad](https://discord.gg/vibecoding)

---

<div align="center">

**⭐ Si este proyecto te fue útil, considera darle una estrella en GitHub ⭐**

Hecho con ❤️ por la comunidad Vibe Coding

</div>
