# PROJECT_CONTEXT — Brandsen Lab

> Este archivo se actualiza al final de cada sesión de trabajo.  
> Antes de empezar una sesión nueva, leer este archivo para retomar contexto.

---

## Última actualización
**Fecha:** 17 Junio 2026  
**Estado del proyecto:** Online en www.brandsenlab.com ✅ — SEO local implementado

---

## Historial de sesiones

### Sesión 1 — Creación inicial
- Sitio institucional completo desde cero en un único `index.html`
- Paleta basada en el logo: vino `#6B1E3C` + malva `#C4A0B0`
- 11 secciones completas con animaciones, FAQ acordeón, formulario validado, WhatsApp flotante
- SEO básico con meta tags y Open Graph

### Sesión 2 — Ajustes y personalización
- Estadísticas del hero: "+50 Años de experiencia" y "100% Compromiso profesional"
- Logo real `logo.jpg` en header y footer
- Fotos reales: `laborat.webp` (hero), `labo.webp` (Nosotros)
- Header fijo con fondo blanco
- Ubicación movida al segundo lugar (después del hero)
- Google Maps vinculado con Place ID real

### Sesión 3 — Deploy
- Repositorio GitHub: https://github.com/lukipetersen/brandsen-lab
- Conectado a Vercel para auto-deploy al push a `main`
- Creados `CLAUDE.md` y `PROJECT_CONTEXT.md`

### Sesión 4 — Security Hardening & Performance (2026-06-05)
- `vercel.json`: 7 headers HTTP de seguridad (CSP, HSTS, X-Frame-Options, X-Content-Type-Options, Referrer-Policy, Permissions-Policy, X-DNS-Prefetch-Control)
- `.gitignore`, `robots.txt`, `sitemap.xml` creados
- CSS muerto eliminado (referencia Unsplash), preload LCP, dimensiones en imágenes, copyright dinámico

### Sesión 5 — Contenido real + Dominio + SEO (2026-06-17)

**Contenido actualizado en index.html:**
- Dirección: Saenz Peña 696 (era 682)
- Horario: 8–10 hs extracciones · 10–12 hs consultas y resultados
- Nosotros: "Fundado en enero de 1971 por Norma Cremaschi" + eliminados recuadros Misión/Visión
- Servicios reordenados (10 tarjetas):
  1. Hematología y Hemostasia (hemograma, metabolismo del hierro)
  2. Bioquímica
  3. Perfil Lipídico
  4. Control Metabólico
  5. Estudios Hormonales
  6. Inmunología (factor reumatoideo)
  7. Perinatología (estreptococo B, screening neonatal)
  8. Bacteriología y Micología (urocultivos, hisopados, hongos)
  9. Análisis de Agua (bacteriológico y fisicoquímico)
  10. Estudios Especiales
- Cartel "ante cualquier duda consultarnos" agregado en Servicios
- Indicaciones actualizadas: ayuno 8–10 hs, medicación post-extracción, orina 24hs completa, materia fecal 3–5 muestras, hormonales con cortisol y TSH, progesterona día 21–23
- Sección Equipo: eliminada
- FAQ: ayuno actualizado a 8–10 hs, retiro de resultados sin "comprobante"

**Dominio y Google:**
- Dominio `www.brandsenlab.com` conectado via GoDaddy → Vercel
- Google Search Console verificado ✅
- Sitemap enviado a Google ✅ — indexación en progreso

**SEO implementado:**
- Meta title: `Laboratorio de Análisis Clínicos en Brandsen | Brandsen Lab`
- Meta description: con keywords locales, horario y dirección
- Meta keywords: 10 términos geo-específicos de Brandsen
- JSON-LD Schema.org tipo `MedicalLab`: dirección, horarios, fundadora, fecha, servicios
- Sección SEO local ~400 palabras visible (H2 + 4×H3) antes del footer
- og:title y og:description actualizados

---

## Pendiente / Por hacer

- [ ] **Formulario** — integrar Formspree para que las consultas lleguen al email. Pasos: registrarse en formspree.io → crear form → darme el ID → yo hago el cambio en el código
- [ ] **RRSS** — agregar links reales de Instagram y Facebook (hoy van a `#`)
- [ ] **SRI** — agregar hash `integrity` a Font Awesome en cdnjs (obtener en https://cdnjs.com/libraries/font-awesome/6.5.0)
- [ ] **Privacidad Google Maps** — evaluar banner de consentimiento (Ley 25.326 Argentina)
- [ ] **Font Awesome** — cargar solo los íconos usados (~180KB de ahorro)

---

## Cómo retomar trabajo
1. Leer `CLAUDE.md` para entender estructura y datos actuales
2. Leer este archivo para saber qué se hizo y qué falta
3. El archivo principal es `/Users/lucaspetersen/Desktop/brandsen-lab/index.html`
4. Al terminar: `git add -A && git commit -m "descripción" && git push`
