# PROJECT_CONTEXT — Brandsen Lab

> Este archivo se actualiza al final de cada sesión de trabajo.  
> Antes de empezar una sesión nueva, leer este archivo para retomar contexto.

---

## Última actualización
**Fecha:** Junio 2026  
**Estado del proyecto:** Online en Vercel ✅

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

### Sesión 3 — Deploy
- Repositorio creado en GitHub: https://github.com/lukipetersen/brandsen-lab
- Conectado a Vercel para auto-deploy al hacer push a `main`
- Favicon subido y pusheado
- Creados `CLAUDE.md` y `PROJECT_CONTEXT.md`

---

## Pendiente / Por hacer
- [ ] Conectar dominio propio a Vercel
- [ ] Agregar fotos reales del equipo profesional (actualmente tienen avatares de placeholder)
- [ ] Completar redes sociales (links de Instagram/Facebook reales)

---

## Cómo retomar trabajo
1. Leer `CLAUDE.md` para entender la estructura del proyecto
2. Leer este archivo para saber qué se hizo y qué falta
3. Abrir `/Users/lucaspetersen/Desktop/brandsen-lab/index.html`
4. Al terminar cambios: `git add -A && git commit -m "descripción" && git push`
