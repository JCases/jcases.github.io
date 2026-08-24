# CV — Javier Cases Sempere

Página estática (HTML + CSS, sin frameworks JS) con el CV en formato web,
lista para imprimir/exportar a PDF en **una sola página A4**.

## Estructura

```
cv-web-project/
├── index.html          ← el CV (ábrelo directamente en el navegador)
├── assets/
│   ├── avatar.jpg       ← tu foto
│   └── tailwind.css     ← CSS de Tailwind ya compilado (no requiere red ni JS)
├── src/
│   └── input.css        ← fuente de estilos (Tailwind + CSS personalizado)
├── tailwind.config.js   ← configuración de colores/tipografías de Tailwind
└── package.json
```

## Ver el CV

Abre `index.html` con doble clic o arrastrándolo a cualquier navegador
(Chrome, Firefox, Edge, Safari). No necesita servidor ni conexión a internet
para funcionar (aunque si tienes conexión cargará las fuentes Google Fonts
Merriweather + Inter; si no, usa una alternativa muy similar del sistema).

## Exportar a PDF

Con la página abierta en el navegador: **Cmd/Ctrl + P** → "Guardar como PDF".
Los estilos de impresión ya están ajustados para que todo el contenido quepa
exactamente en **1 página A4**, sin sombras ni fondo gris de pantalla.

## Editar el contenido

Todo el texto está directamente en `index.html` (nombre, experiencia,
educación, skills, idiomas...). Edítalo con cualquier editor de texto.

## Editar estilos / recompilar Tailwind

Si cambias clases de Tailwind en `index.html` o `src/input.css`, necesitas
recompilar `assets/tailwind.css`:

```sh
npm install
npm run build
```

## Diseño

- **Layout**: sidebar azul marino (foto, contacto, educación, competencias,
  idiomas) + columna principal blanca (perfil, experiencia) — inspirado en
  el tema `jsonresume-theme-sidebar`.
- **Competencias técnicas**: agrupadas por categoría en negrita con lista en
  texto corrido — mismo patrón que `jsonresume-theme-executive-slate`.
- **Tipografía**: Merriweather (serif) para títulos + Inter (sans-serif)
  para el cuerpo del texto — combinación clásica y muy legible para CVs,
  con buen contraste jerárquico entre encabezados y contenido.
