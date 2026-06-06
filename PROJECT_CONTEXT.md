# PROJECT_CONTEXT — Brandsen Lab

> Este archivo se actualiza al final de cada sesión de trabajo.  
> Antes de empezar una sesión nueva, leer este archivo para retomar contexto.

---

## Última actualización
**Fecha:** 5 Junio 2026  
**Estado del proyecto:** Online en Vercel ✅ — Security hardening aplicado

---

## Historial de sesiones

### Sesión 1 — Creación inicial
- Se creó el sitio institucional completo desde cero en un único `index.html`
- Paleta basada en el logo: vino `#6B1E3C` + malva `#C4A0B0`
- 11 secciones completas con animaciones, FAQ acordeón, formulario validado, WhatsApp flotante
- SEO básico con meta tags y Open Graph

### Sesión 2 — Ajustes y personalización
- **Estadísticas del hero:** se eliminó "+50 Tipos de estudios", quedaron solo "+50 Años de experiencia" y "100% Compromiso profesional"
- **Logo real:** se reemplazó el logo de texto/CSS por la imagen real `logo.jpg` en header y footer
- **Años de experiencia:** cambiado de +20 a +50 en todos los lugares del sitio
- **Título del hero:** cambiado de "Comprometidos con la precisión y la salud" a "Brandsen Lab"
- **Fotos reales:** 
  - `laborat.webp` (fachada del edificio) → fondo del hero
  - `labo.webp` (cartel con logo en la pared) → foto en sección Nosotros
  - Se eliminó la foto lateral del hero (era de Unsplash)
- **Header:** siempre visible con fondo blanco (ya no es transparente al inicio)
- **Orden de secciones:** Ubicación movida al segundo lugar (después del hero), antes de Nosotros
- **Google Maps:** vinculado con el Place ID real del laboratorio (`0x95a2c9d46f21106f:0xe2bbd36fb5c011ee`), botón "Cómo llegar" apunta a la ficha real del negocio
- **Favicon:** creado `favicon.png` desde `logo.jpg`, aparece en la pestaña del navegador

### Sesión 4 — Security Hardening & Performance (2026-06-05)

**Infraestructura:**
- `vercel.json` creado con 7 headers HTTP de seguridad:
  - `Content-Security-Policy` — whitelist estricta de fuentes permitidas (CSP)
  - `X-Frame-Options: DENY` — protección anti-clickjacking
  - `X-Content-Type-Options: nosniff` — protección anti-MIME sniffing
  - `Referrer-Policy: strict-origin-when-cross-origin`
  - `Strict-Transport-Security` — HSTS max-age 1 año + includeSubDomains + preload
  - `Permissions-Policy` — bloquea cámara, micrófono, geolocalización, pagos
  - `X-DNS-Prefetch-Control: off`
- `.gitignore` creado — previene subir .DS_Store y archivos sensibles
- `robots.txt` creado — controla crawlers y apunta al sitemap
- `sitemap.xml` creado — mejora SEO e indexación

**Código frontend (index.html):**
- CSS muerto eliminado — regla `.hero-side` con URL de Unsplash (dependencia externa innecesaria, código de sesión anterior)
- `<link rel="preload">` para `laborat.webp` — LCP image priorizada → mejor Core Web Vitals
- Dimensiones explícitas agregadas a todas las imágenes → elimina Layout Shift (CLS):
  - `logo.jpg` en header: `width="52" height="52"`
  - `logo.jpg` en footer: `width="64" height="64"`
  - `labo.webp` en Nosotros: `width="1360" height="764"`
- `decoding="async"` en imágenes no críticas
- Copyright año dinámico — ya no está hardcodeado a 2024
- Meta tags OG completados: `og:url` y `og:image` faltaban

**Vulnerabilidades identificadas que NO aplican a este sitio:**
- Sin backend → sin SQL injection, sin autenticación, sin gestión de sesiones
- Sin credenciales en código
- HTTPS gestionado por Vercel

**NOTA CRÍTICA — Formulario de contacto:**
El formulario valida client-side pero NO envía ningún email. Los pacientes creen que enviaron una consulta pero no llega nada. Para resolverlo: integrar Formspree (https://formspree.io) — gratuito, sin backend.

### Sesión 3 — Deploy
- Repositorio creado en GitHub: https://github.com/lukipetersen/brandsen-lab
- Conectado a Vercel para auto-deploy al hacer push a `main`
- Favicon subido y pusheado
- Creados `CLAUDE.md` y `PROJECT_CONTEXT.md`

---

## Pendiente / Por hacer
- [ ] **Formulario** — integrar Formspree para que las consultas lleguen realmente al email
- [ ] **SRI** — agregar hash `integrity` a Font Awesome en cdnjs (obtener hash en https://cdnjs.com/libraries/font-awesome/6.5.0)
- [ ] **Dominio propio** — conectar dominio a Vercel (actualizar `og:url`, `sitemap.xml` y `robots.txt` con el dominio real)
- [ ] **Fotos del equipo** — reemplazar íconos de placeholder con fotos reales del personal
- [ ] **RRSS** — agregar links reales de Instagram y Facebook (hoy van a `#`)
- [ ] **Privacidad Google Maps** — evaluar agregar banner de consentimiento antes de cargar el iframe (cumplimiento GDPR/LPDP)
- [ ] **Font Awesome** — considerar cargar solo los íconos usados (reduce ~180KB de CSS) o migrar a SVG inline

---

## Cómo retomar trabajo
1. Leer `CLAUDE.md` para entender la estructura del proyecto
2. Leer este archivo para saber qué se hizo y qué falta
3. Abrir `/Users/lucaspetersen/Desktop/brandsen-lab/index.html`
4. Al terminar cambios: `git add -A && git commit -m "descripción" && git push`
