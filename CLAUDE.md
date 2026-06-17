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
├── index.html         ← toda la web (estructura + estilos + scripts)
├── logo.jpg           ← logo oficial del laboratorio
├── labo.webp          ← foto del cartel/frente del laboratorio (sección Nosotros)
├── laborat.webp       ← foto de la fachada del edificio (fondo del hero)
├── favicon.png        ← ícono de pestaña del navegador
├── vercel.json        ← headers HTTP de seguridad (CSP, HSTS, X-Frame, etc.)
├── robots.txt         ← control de crawlers + referencia al sitemap
├── sitemap.xml        ← mapa del sitio para Google
├── .gitignore         ← excluye .DS_Store y archivos sensibles
├── CLAUDE.md          ← este archivo
└── PROJECT_CONTEXT.md ← historial de cambios y contexto de conversaciones
```

## Estructura de secciones (en orden)
1. **Header** — fijo, siempre visible con fondo blanco, logo real
2. **Hero** — fondo con `laborat.webp`, título "Brandsen Lab", subtítulo, botones, stats
3. **Ubicación** — dirección, horarios, teléfono, WhatsApp, email, mapa Google Maps
4. **Nosotros** — fundada en 1971 por Norma Cremaschi, foto `labo.webp`, valores (sin misión/visión)
5. **Servicios** — 10 tarjetas: Hematología y Hemostasia, Bioquímica, Perfil Lipídico, Control Metabólico, Estudios Hormonales, Inmunología, Perinatología, Bacteriología y Micología, Análisis de Agua, Estudios Especiales
6. **Indicaciones** — 5 tarjetas para pacientes (ayuno, orina, materia fecal, hormonales, especiales)
7. **Tecnología y Calidad** — 6 tarjetas sobre equipamiento
8. **Preguntas Frecuentes** — 7 acordeones
9. **Contacto** — formulario (⚠️ no envía emails aún) + canales directos
10. **SEO Local** — sección informativa ~400 palabras con H2/H3 para posicionamiento
11. **Footer** — logo, links, datos de contacto

## Datos del laboratorio
- **Dirección:** Saenz Peña 696, Brandsen, Buenos Aires
- **Horarios:** Lunes a Viernes — 8:00 a 10:00 hs extracciones · 10:00 a 12:00 hs consultas y resultados
- **Teléfono:** (2223) 44-2486
- **WhatsApp:** (2223) 67-2253
- **Email:** brandsenlab@gmail.com
- **Google Maps Place ID:** `0x95a2c9d46f21106f:0xe2bbd36fb5c011ee`
- **Coordenadas:** -35.1675794, -58.2385888
- **Fundación:** enero de 1971, por Norma Cremaschi

## Deploy
- **Repositorio GitHub:** https://github.com/lukipetersen/brandsen-lab
- **Hosting:** Vercel (auto-deploy al hacer push a `main`)
- **Dominio:** https://www.brandsenlab.com
- **Flujo de cambios:** editar `index.html` → `git add` → `git commit` → `git push` → Vercel redespliega solo

## SEO
- **Google Search Console:** verificado ✅ — sitemap enviado ✅
- **Schema.org JSON-LD:** tipo `MedicalLab` con dirección, horarios, servicios y fundadora
- **Meta title:** `Laboratorio de Análisis Clínicos en Brandsen | Brandsen Lab`
- **Keyword principal:** `laboratorio análisis clínicos Brandsen`

## Reglas importantes
- ⚠️ **No modificar** datos de contacto, colores ni stack sin confirmación explícita del usuario.
- ⚠️ El formulario de contacto NO envía emails — pendiente integrar Formspree.
- Siempre hacer `git push` al terminar cambios para que Vercel actualice la web online.
- La paleta de colores está definida en `:root` al inicio del `<style>`: vino `#6B1E3C` + malva `#C4A0B0`.
