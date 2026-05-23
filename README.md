# ecomiga — Sitio Web

[![Deploy with Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/USUARIO/ecomiga-site)
[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https://github.com/USUARIO/ecomiga-site)

> Catálogo web de **ecomiga** — yogurt griego y kefir artesanal de La Paz, Bolivia. Hecho por Mirtha Rivera.

![ecomiga · preview del home](./preview.png)

Sitio estático (HTML + CSS + SVG) con 1 home + 9 páginas de sabor, integración con WhatsApp y diseño responsive.

---

## ✨ Características

- 🍓 **9 amiguitos** — un personaje por sabor (7 yogurts + 2 kefirs)
- 📱 **WhatsApp flotante** con mensaje pre-llenado por producto
- 🎨 **Sistema visual completo** — Fraunces + Plus Jakarta Sans, paleta pastel por sabor
- 💯 **100% estático** — sin servidor, sin build, sin dependencias
- 📐 **Responsive** — mobile, tablet, desktop
- ⚡ **Rápido** — SVGs inline, fonts de Google Fonts, sin JS pesado

---

## 📁 Estructura

```
ecomiga-site/
├── index.html              # Home (hero + amiguitos + beneficios + sobre)
├── styles.css              # CSS único compartido por todas las páginas
├── sabores/                # 9 páginas de producto
│   ├── frutilla.html       # Fresi — yogurt griego
│   ├── limon.html          # Limé — yogurt griego
│   ├── arandano.html       # Aru — yogurt griego
│   ├── vainilla.html       # Vani — yogurt griego
│   ├── maracuya.html       # Maru — yogurt griego
│   ├── coco.html           # Coqui — yogurt griego
│   ├── pina.html           # Pini — yogurt griego
│   ├── jamaica.html        # Jamai — kefir
│   └── manzana.html        # Manzi — kefir
├── assets/
│   ├── logo.svg            # Logo ecomiga ("e→C" fusion)
│   └── amiguitos/          # 9 SVGs de personajes
│       ├── fresi-frutilla.svg
│       ├── lime-limon.svg
│       ├── aru-arandano.svg
│       ├── vani-vainilla.svg
│       ├── maru-maracuya.svg
│       ├── coqui-coco.svg
│       ├── pini-pina.svg
│       ├── jamai-jamaica.svg
│       └── manzi-manzana.svg
├── netlify.toml            # Config para Netlify (opcional)
├── vercel.json             # Config para Vercel (opcional)
├── .gitignore
├── LICENSE
└── README.md
```

---

## 🚀 Deploy

### Opción 1 — Netlify (gratis, recomendado)

**Drag & drop (sin git):**
1. Andá a [app.netlify.com/drop](https://app.netlify.com/drop)
2. Arrastrá la carpeta `ecomiga-site/` al cuadro
3. Listo — sale online en `xxx.netlify.app`

**Con GitHub (auto-deploy en cada push):**
1. Subí este repo a GitHub
2. Conectalo en [app.netlify.com](https://app.netlify.com)
3. Build command: vacío · Publish directory: `.`

### Opción 2 — Vercel

```bash
npm i -g vercel
cd ecomiga-site
vercel
```

### Opción 3 — GitHub Pages

1. Settings → Pages
2. Source: `main` branch, root folder `/`
3. Save → disponible en `usuario.github.io/ecomiga-site`

### Opción 4 — Hosting tradicional (FTP)

Subir toda la carpeta al servidor. El `index.html` es la página de inicio.

### Probar local

```bash
# Abrir con doble click
open index.html

# O servir con Python (puerto 8000)
python3 -m http.server 8000

# O con Node.js
npx serve .
```

---

## 🛠️ Modificar el sitio

### Cambiar el número de WhatsApp

Buscar y reemplazar `59172133348` en todos los HTML por el nuevo número (formato internacional sin `+`).

```bash
# En Linux/Mac
find . -name "*.html" -exec sed -i 's/59172133348/NUEVONUMERO/g' {} \;
```

### Cambiar textos

Cada página de sabor tiene su propio HTML — buscar el texto y editarlo directamente.

### Cambiar colores

Todas las variables están al inicio de `styles.css` en `:root`. Por ejemplo:

```css
:root {
  --blue: #0C348E;        /* Azul ecomiga */
  --aqua: #7AC9CB;        /* Aqua signature */
  --frutilla: #F2A1B0;    /* Pastel frutilla */
  /* ... */
}
```

### Agregar un sabor nuevo

1. Crear `sabores/nuevo-sabor.html` (copiar de uno existente y editar)
2. Agregar variables `--nuevo-sabor`, `--nuevo-sabor-soft`, `--nuevo-sabor-accent` en `styles.css`
3. Agregar la card en `index.html` (sección "Los Amiguitos")
4. Agregar el link en el footer

---

## 🎨 Sistema de diseño

| Elemento | Valor |
|---|---|
| **Tipografía display** | Fraunces (Google Fonts) — italic-heavy |
| **Tipografía body** | Plus Jakarta Sans (Google Fonts) |
| **Color primario** | `#0C348E` (azul ecomiga) |
| **Color acento** | `#7AC9CB` (aqua signature) |
| **Detalle** | `#D0A03C` (oro Mirtha) |
| **Animaciones** | CSS keyframes (float, wiggle, hover lift) |
| **Iconografía** | SVG inline, Lucide-style strokes |

---

## 📞 Contacto

**ecomiga** — Yogurt Griego & Kefir Artesanal  
Elaborado por **Mirtha Rivera**  
NIT: 3192684014  
Urb. California, c/ San Francisco #227  
La Paz · Bolivia  
WhatsApp: [+591 721 33 348](https://wa.me/59172133348)

---

## 📄 Licencia

Este código pertenece a Mirtha Rivera / ecomiga. Ver [LICENSE](./LICENSE).

Los SVGs de los amiguitos, el logo y la identidad visual son propiedad de ecomiga.

---

*Hecho con 💙 en La Paz, Bolivia · 2026*
