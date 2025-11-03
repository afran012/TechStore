# 🛍️ TechStore - Sitio Web para Google Analytics

## 📋 Descripción del Proyecto

Sitio web completo de una tienda de tecnología desarrollado para un proyecto académico de Google Analytics. El sitio simula una tienda online con múltiples páginas y eventos trackeable para análisis de métricas.

## ✨ Características Principales

### 🎨 Diseño y UX
- ✅ Diseño **responsive** (mobile-first)
- ✅ Navegación **SPA** (Single Page Application) sin recargas
- ✅ Animaciones suaves y profesionales
- ✅ Menú hamburguesa para dispositivos móviles
- ✅ Colores corporativos: Azul (#1F4E78), Verde (#00B050), Gris (#F2F2F2)

### 📄 Páginas Incluidas

1. **Inicio**
   - Banner hero atractivo
   - 3 productos destacados
   - 4 beneficios (Envío gratis, Garantía, Pago seguro, Soporte 24/7)

2. **Productos** (Catálogo)
   - 6 productos con precios en COP
   - Filtros por categoría (Todos, Computadores, Accesorios, Audio)
   - Tarjetas de producto interactivas

3. **Nosotros**
   - Historia de la empresa
   - Misión y Visión
   - Valores corporativos
   - Imagen del equipo

4. **Contacto**
   - Formulario funcional con validación
   - Información de contacto
   - Mapa de Google Maps integrado

### 📊 Google Analytics 4

El sitio incluye tracking completo para Google Analytics:

#### Eventos Trackeados:
- ✅ **Vistas de página** - Cada navegación entre secciones
- ✅ **Clics en productos** - Al hacer clic en cualquier producto
- ✅ **Filtros de productos** - Cuando se aplican filtros de categoría
- ✅ **Envío de formulario** - Al enviar el formulario de contacto
- ✅ **Clics en redes sociales** - Al hacer clic en iconos sociales
- ✅ **Botones CTA** - Botón "Ver Productos" del hero
- ✅ **Tiempo en sitio** - Duración total de la visita

#### Métricas Capturadas:
- Número de visitas (contador local)
- Páginas visitadas
- Productos más clicados
- Categorías más filtradas
- Formularios completados
- Engagement en redes sociales

## 🚀 Cómo Usar

### Paso 1: Abrir el Sitio
1. Abre el archivo `index.html` en tu navegador web
2. El sitio funciona **100% offline** (excepto Google Analytics y Google Fonts)

### Paso 2: Configurar Google Analytics

Para activar el tracking real de Google Analytics:

1. **Crea una cuenta de Google Analytics 4:**
   - Ve a [analytics.google.com](https://analytics.google.com)
   - Crea una nueva propiedad
   - Obtén tu **ID de medición** (formato: `G-XXXXXXXXXX`)

2. **Reemplaza el ID en el código:**
   - Abre `index.html` en un editor de texto
   - Busca la línea 25 (aprox.): `<!-- IMPORTANTE: Reemplaza 'G-XXXXXXXXXX' con tu ID real de Google Analytics -->`
   - En la línea 28, reemplaza `G-XXXXXXXXXX` con tu ID real:
   
   ```javascript
   gtag('config', 'TU-ID-AQUI', {
       'page_title': 'TechStore Colombia',
       'page_location': window.location.href
   });
   ```

3. **También reemplaza en la línea 26:**
   ```html
   <script async src="https://www.googletagmanager.com/gtag/js?id=TU-ID-AQUI"></script>
   ```

### Paso 3: Probar el Sitio

1. **Navega por las secciones:**
   - Usa el menú superior para moverte entre páginas
   - Observa las transiciones suaves

2. **Prueba los productos:**
   - Haz clic en productos destacados (Inicio)
   - Ve a la página de Productos
   - Prueba los filtros de categoría

3. **Completa el formulario:**
   - Ve a la página de Contacto
   - Llena el formulario con datos válidos
   - Envía el formulario

4. **Verifica el contador de visitas:**
   - Mira el footer (abajo)
   - El contador aumenta con cada carga de página
   - Se guarda en el almacenamiento local del navegador

## 📊 Ver Métricas en Google Analytics

Una vez configurado tu ID de Google Analytics:

1. **Espera 24-48 horas** para datos completos
2. Ve a tu panel de Google Analytics
3. Revisa:
   - **Informes > Interacción > Eventos**: Ver todos los eventos personalizados
   - **Informes > Interacción > Páginas**: Ver navegación entre secciones
   - **Informes > Usuarios**: Ver visitantes únicos

### Eventos que verás en Analytics:

| Nombre del Evento | Descripción | Categoría |
|-------------------|-------------|-----------|
| `page_view` | Vista de página | Navegación |
| `select_item` | Clic en producto | Products |
| `filter_products` | Aplicar filtro | Products |
| `form_submit` | Envío de formulario | Contact |
| `social_click` | Clic en red social | Social Media |
| `click` | Clic en CTA | CTA |
| `time_on_site` | Tiempo total en sitio | Engagement |

## 🎯 Productos Incluidos

| Producto | Precio | Categoría |
|----------|--------|-----------|
| Laptop HP Pavilion | $45.000 COP | Computadores |
| Mouse Inalámbrico | $25.000 COP | Accesorios |
| Monitor Samsung 24" | $120.000 COP | Computadores |
| Teclado Mecánico | $35.000 COP | Accesorios |
| Impresora HP | $85.000 COP | Computadores |
| Audífonos Sony | $55.000 COP | Audio |

## 🔧 Tecnologías Utilizadas

- **HTML5**: Estructura semántica
- **CSS3**: Estilos modernos, Flexbox, Grid, Animaciones
- **JavaScript (Vanilla)**: Interactividad, SPA, Validaciones
- **Google Analytics 4**: Tracking de métricas
- **Google Fonts**: Tipografías Poppins y Roboto
- **LocalStorage**: Contador de visitas
- **Placehold.co**: Imágenes placeholder (con fallback a dummyimage.com)

## 📱 Compatibilidad

✅ Chrome, Firefox, Safari, Edge (últimas versiones)  
✅ Dispositivos móviles (iOS, Android)  
✅ Tablets  
✅ Escritorio  

## 🐛 Solución de Problemas

### Las imágenes no se cargan
- **Solución**: Asegúrate de tener conexión a internet
- Las imágenes usan servicios de placeholder online
- Si persiste, revisa la consola del navegador (F12)

### Google Analytics no registra eventos
- **Verifica**: ¿Reemplazaste el ID `G-XXXXXXXXXX`?
- **Espera**: Los datos pueden tardar 24-48 horas en aparecer
- **Prueba**: Usa el modo "DebugView" en Google Analytics (tiempo real)

### El menú móvil no funciona
- **Solución**: Asegúrate de que JavaScript esté habilitado
- Prueba en modo incógnito para descartar extensiones

### El contador de visitas no aumenta
- **Solución**: El navegador debe permitir localStorage
- Revisa la configuración de privacidad del navegador

## 📝 Notas para el Proyecto Académico

### Datos para tu informe:

1. **Estructura del sitio**: SPA con 4 secciones principales
2. **Eventos implementados**: 7+ tipos de eventos diferentes
3. **Validaciones**: Formulario con validación de email y campos requeridos
4. **Persistencia**: Contador de visitas usando localStorage
5. **Responsive**: 100% adaptable a todos los dispositivos
6. **SEO**: Meta tags, Open Graph, Schema.org implementados

### Sugerencias para tu presentación:

1. **Demostrar navegación**: Muestra cómo funciona el SPA
2. **Mostrar eventos**: Abre la consola de Analytics en tiempo real
3. **Probar responsive**: Usa las herramientas de desarrollador (F12)
4. **Explicar el tracking**: Describe cada evento y su utilidad
5. **Analizar métricas**: Presenta datos reales después de algunas visitas

## 📄 Estructura de Archivos

```
ACtividad2/
├── index.html          # Archivo principal (todo incluido)
└── README.md           # Este archivo (instrucciones)
```

## 🎓 Características Académicas Cumplidas

- ✅ Sitio completo y funcional
- ✅ Google Analytics 4 configurado
- ✅ Múltiples eventos trackeable
- ✅ Diseño profesional y responsive
- ✅ Código limpio y comentado
- ✅ Sin dependencias complejas
- ✅ Documentación completa

## 💡 Tips para Mejorar las Métricas

1. **Comparte el enlace**: Pide a compañeros que visiten el sitio
2. **Navega tú mismo**: Haz varias visitas desde diferentes dispositivos
3. **Prueba todas las funciones**: Clica productos, aplica filtros, envía el formulario
4. **Deja el sitio abierto**: Para aumentar el tiempo promedio en sitio
5. **Usa diferentes navegadores**: Para simular usuarios únicos

## 📧 Información de Contacto (Ficticia)

- **Email**: contacto@techstore.com.co
- **Teléfono**: +57 300 123 4567
- **Dirección**: Calle 10 #43-25, Medellín, Antioquia, Colombia

---

## ✅ Checklist para Entregar el Proyecto

- [ ] Archivo `index.html` funcional
- [ ] Google Analytics ID configurado
- [ ] Sitio probado en navegador
- [ ] Screenshots de métricas en Analytics
- [ ] Documento explicando los eventos
- [ ] Informe académico completo

---

**Desarrollado para**: Proyecto Académico de Google Analytics  
**Fecha**: Noviembre 2025  
**Versión**: 1.0  

¡Buena suerte con tu proyecto! 🚀📊
