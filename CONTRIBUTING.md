# 🤝 Guía de Contribución - CSS Loaders Vibe Coding

¡Gracias por tu interés en contribuir a CSS Loaders! Este documento te guiará a través del proceso de contribución.

---

## 📋 Tabla de Contenidos

- [Código de Conducta](#código-de-conducta)
- [Cómo Puedo Contribuir](#cómo-puedo-contribuir)
- [Proceso de Desarrollo](#proceso-de-desarrollo)
- [Estándares de Código](#estándares-de-código)
- [Guía de Estilo](#guía-de-estilo)
- [Proceso de Pull Request](#proceso-de-pull-request)

---

## 📜 Código de Conducta

Este proyecto sigue el Código de Conducta de Vibe Coding. Al participar, se espera que mantengas este código.

### Nuestros Compromisos

- Ser respetuoso con diferentes puntos de vista
- Aceptar críticas constructivas
- Enfocarse en lo mejor para la comunidad
- Mostrar empatía hacia otros miembros

---

## 💡 Cómo Puedo Contribuir

### Reportar Bugs

Antes de crear un reporte de bug, revisa la lista de issues para evitar duplicados.

**Template para reportar bugs:**

```markdown
**Descripción del Bug:**
Descripción clara y concisa del problema.

**Pasos para Reproducir:**
1. Ve a '...'
2. Haz clic en '...'
3. Desplázate hasta '...'
4. Observa el error

**Comportamiento Esperado:**
Qué debería suceder.

**Comportamiento Actual:**
Qué está sucediendo.

**Screenshots:**
Si aplica, agrega screenshots.

**Entorno:**
- Navegador: [ej. Chrome 120]
- OS: [ej. Windows 11]
- Versión del Proyecto: [ej. 1.0.0]

**Contexto Adicional:**
Cualquier información adicional relevante.
```

### Sugerir Mejoras

¿Tienes ideas para mejorar el proyecto? ¡Nos encantaría escucharlas!

**Template para sugerencias:**

```markdown
**Tipo de Mejora:**
[Nueva funcionalidad / Optimización / Diseño / Documentación]

**Descripción:**
Descripción clara de la mejora sugerida.

**Problema que Resuelve:**
¿Qué problema o necesidad aborda esta mejora?

**Solución Propuesta:**
Describe cómo visualizas la implementación.

**Alternativas Consideradas:**
Otras soluciones que hayas considerado.

**Ejemplos:**
Código, mockups o referencias visuales.
```

### Agregar Nuevos Loaders

¿Creaste un loader increíble? ¡Compártelo!

**Requisitos para nuevos loaders:**

- ✅ CSS puro (sin JavaScript)
- ✅ Performance de 60 FPS
- ✅ Tamaño base de 40x40px
- ✅ Compatible con tema oscuro/claro
- ✅ Accesible (soporte para screen readers)
- ✅ Responsive
- ✅ Documentado con comentarios
- ✅ Nombre descriptivo y único

---

## 🛠️ Proceso de Desarrollo

### 1. Fork y Clone

```bash
# Fork el repositorio en GitHub
# Luego clona tu fork
git clone https://github.com/tu-usuario/css-loaders.git
cd css-loaders
```

### 2. Crear una Rama

```bash
# Para nuevas funcionalidades
git checkout -b feature/nombre-descriptivo

# Para corrección de bugs
git checkout -b fix/nombre-del-bug

# Para documentación
git checkout -b docs/que-documentas
```

### 3. Hacer Cambios

- Mantén los commits pequeños y enfocados
- Escribe mensajes de commit descriptivos
- Prueba tus cambios en múltiples navegadores

### 4. Probar Localmente

```bash
# Abre index.html en tu navegador
# O usa un servidor local
python -m http.server 8000
# Visita http://localhost:8000
```

### 5. Commit y Push

```bash
git add .
git commit -m "feat: agrega nuevo loader orbital mejorado"
git push origin feature/nombre-descriptivo
```

---

## 📐 Estándares de Código

### Estructura CSS

```css
/* ✅ BUENO: Estructura clara y organizada */
.loader-nombre {
  /* Posicionamiento */
  position: relative;
  
  /* Dimensiones */
  width: 40px;
  height: 40px;
  
  /* Animación */
  animation: nombreAnimacion 2s ease-in-out infinite;
}

.loader-nombre::before {
  content: "";
  position: absolute;
  /* ... más propiedades ... */
}

@keyframes nombreAnimacion {
  0% { transform: rotate(0deg); }
  100% { transform: rotate(360deg); }
}
```

### Nomenclatura

```css
/* ✅ BUENO: Nombres descriptivos en kebab-case */
.loader-spinning-circle { }
.loader-bouncing-dots { }

/* ❌ MALO: Nombres genéricos o poco descriptivos */
.loader1 { }
.ld { }
```

### Performance

```css
/* ✅ BUENO: Usa transform y opacity */
.loader {
  transform: translateX(10px);
  opacity: 0.8;
}

/* ❌ MALO: Evita left, top, width, height en animaciones */
.loader {
  left: 10px;
  width: 50px;
}
```

### Comentarios

```css
/* ✅ BUENO: Comentarios descriptivos */
.loader-orbital {
  /* Crea efecto de perspectiva 3D */
  perspective: 500px;
  
  /* Sistema orbital con 3 elementos rotando */
  animation: orbit 4s linear infinite;
}

/* ❌ MALO: Comentarios obvios o innecesarios */
.loader {
  width: 40px; /* ancho */
}
```

---

## 🎨 Guía de Estilo

### HTML

```html
<!-- ✅ BUENO: Semántico y accesible -->
<div class="loader loader-spinning-circle" 
     role="status" 
     aria-label="Cargando contenido">
  <span class="visually-hidden">Cargando...</span>
</div>

<!-- ❌ MALO: Sin accesibilidad -->
<div class="loader-1"></div>
```

### CSS

**Propiedades Permitidas:**
- `transform` ✅
- `opacity` ✅
- `filter` ✅
- `background` ✅
- `border` ✅
- `box-shadow` ✅

**Propiedades a Evitar en Animaciones:**
- `width/height` ❌
- `left/top/right/bottom` ❌
- `margin/padding` ❌

### Colores

```css
/* ✅ BUENO: Usa variables CSS */
:root {
  --loader-color: #ffffff;
  --loader-bg: transparent;
}

.loader {
  background: var(--loader-color);
}

/* ❌ MALO: Colores hardcoded */
.loader {
  background: #fff;
}
```

---

## 🔄 Proceso de Pull Request

### Checklist Pre-PR

Antes de enviar tu PR, verifica:

- [ ] El código sigue los estándares del proyecto
- [ ] Los commits tienen mensajes descriptivos
- [ ] Se agregó documentación si es necesario
- [ ] El loader funciona en Chrome, Firefox, Safari
- [ ] Performance es de 60 FPS
- [ ] Es responsive (móvil a desktop)
- [ ] Incluye soporte para accesibilidad
- [ ] Soporta `prefers-reduced-motion`
- [ ] El CSS está comentado apropiadamente

### Template de Pull Request

```markdown
## Descripción
Descripción clara de los cambios realizados.

## Tipo de Cambio
- [ ] Bug fix (cambio que corrige un issue)
- [ ] Nueva funcionalidad (cambio que agrega funcionalidad)
- [ ] Breaking change (fix o feature que causa cambios en funcionalidad existente)
- [ ] Documentación

## Loader Agregado (si aplica)
**Nombre:** Spinning Galaxy
**Descripción:** Loader con efecto de galaxia rotando
**Caso de uso ideal:** Aplicaciones astronómicas o científicas

## Cómo se ha Probado
- [ ] Chrome 120+
- [ ] Firefox 115+
- [ ] Safari 16+
- [ ] Edge 120+
- [ ] Móvil (iOS/Android)

## Screenshots
[Agrega screenshots o GIFs del loader en acción]

## Checklist
- [ ] Mi código sigue el estilo del proyecto
- [ ] He realizado self-review del código
- [ ] He comentado el código, especialmente en áreas complejas
- [ ] He actualizado la documentación
- [ ] Mis cambios no generan nuevos warnings
- [ ] He probado que funciona en diferentes navegadores
- [ ] Performance es óptima (60 FPS)
```

### Proceso de Review

1. **Envío:** Crea tu PR usando el template
2. **Revisión Automática:** Los checks automáticos deben pasar
3. **Code Review:** Un maintainer revisará el código
4. **Feedback:** Implementa cambios solicitados
5. **Aprobación:** PR aprobado por al menos 1 maintainer
6. **Merge:** El PR será merged a la rama main

---

## 🏆 Reconocimiento

Los contribuidores serán:
- Listados en el README.md
- Mencionados en las release notes
- Agregados a la página de contribuidores
- Invitados al canal privado de Discord

---

## 📞 Preguntas

¿Tienes preguntas sobre cómo contribuir?

- Abre un [Discussion](https://github.com/vibecoding/css-loaders/discussions)
- Únete a nuestro [Discord](https://discord.gg/vibecoding)
- Contacta a los maintainers

---

## 📚 Recursos Útiles

- [Guía de CSS Performance](https://web.dev/animations-guide/)
- [Accesibilidad Web](https://www.w3.org/WAI/WCAG21/quickref/)
- [Convenciones de Commits](https://www.conventionalcommits.org/)

---

<div align="center">

**¡Gracias por contribuir a CSS Loaders! 🎉**

Tu trabajo ayuda a miles de developers a crear mejores experiencias.

</div>
