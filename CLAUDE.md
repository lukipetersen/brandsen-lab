# Brandsen Lab — Sitio Institucional

## Descripción
Página web institucional e informativa del laboratorio de análisis clínicos **Brandsen Lab**.  
**No tiene** sistema de turnos, login de pacientes ni funciones administrativas.  
Su objetivo es exclusivamente informativo: mostrar servicios, ubicación, horarios, equipo y contacto.

## Stack técnico
- **HTML / CSS / JavaScript** puro — todo en un único archivo `index.html`
- Sin frameworks, sin bundlers, sin dependencias locales
- Fuentes: Google Fonts (Playfair Display + Inter) vía CDN
- Íconos: Font Awesome 6.5 vía CDN

## Archivos del proyecto
```
brandsen-lab/
├── index.html       ← toda la web (estructura + estilos + scripts)
├── logo.jpg         ← logo oficial del laboratorio
├── labo.webp        ← foto del cartel/frente del laboratorio (sección Nosotros)
├── laborat.webp     ← foto de la fachada del edificio (fondo del hero)
├── favicon.png      ← ícono de pestaña del navegador (generado desde logo.jpg)
├── CLAUDE.md        ← este archivo
└── PROJECT_CONTEXT.md ← historial de cambios y contexto de conversaciones
```

## Estructura de secciones (en orden)
1. **Header** — fijo, siempre visible con fondo blanco, logo real
2. **Hero** — fondo con `laborat.webp`, título "Brandsen Lab", subtítulo, botones, stats
3. **Ubicación** — dirección, horarios, teléfono, WhatsApp, email, mapa Google Maps
4. **Nosotros** — historia, misión, visión, valores, foto `labo.webp`
5. **Servicios** — 12 tarjetas con iconos
6. **Indicaciones** — 5 tarjetas para pacientes (ayuno, orina, etc.)
7. **Tecnología y Calidad** — 6 tarjetas sobre equipamiento
8. **Equipo** — 4 perfiles profesionales
9. **Preguntas Frecuentes** — 7 acordeones
10. **Contacto** — formulario validado + canales directos
11. **Footer** — logo, links, datos de contacto

## Datos del laboratorio
- **Dirección:** Saenz Peña 696, Brandsen, Buenos Aires
- **Horarios:** Lunes a Viernes, 8:00–10:00 hs extracciones · 10:00–12:00 hs consultas y resultados
- **Teléfono:** (2223) 44-2486
- **WhatsApp:** (2223) 67-2253
- **Email:** brandsenlab@gmail.com
- **Google Maps Place ID:** `0x95a2c9d46f21106f:0xe2bbd36fb5c011ee`
- **Coordenadas:** -35.1675794, -58.2385888

## Deploy
- **Repositorio GitHub:** https://github.com/lukipetersen/brandsen-lab
- **Hosting:** Vercel (auto-deploy al hacer push a `main`)
- **Flujo de cambios:** editar `index.html` → `git add` → `git commit` → `git push` → Vercel redespliega solo

## Reglas importantes
- ⚠️ **No modificar** la estructura de secciones, datos de contacto, colores ni stack sin confirmación explícita del usuario.
- Siempre hacer `git push` al terminar cambios para que Vercel actualice la web online.
- La paleta de colores está definida en `:root` al inicio del `<style>`: vino `#6B1E3C` + malva `#C4A0B0`.
