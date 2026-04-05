# F96 — Instrucciones de configuración
<!-- Review business name throughout all files -->

## Estructura de archivos

```
f96/
├── index.html          ← Sitio principal (Nosotros + Equipo + Actividades + Tarifas)
├── landing.html        ← Página de funnel (no aparece en el menú)
├── assets/
│   ├── gym.jpg         ← ⚠️ AÑADIR: foto del espacio (la imagen que compartiste)
│   └── miguel.jpg      ← ⚠️ AÑADIR: foto de Miguel (opcional, hay placeholder)
└── README.md           ← Este archivo
```

---

## ⚠️ PASOS NECESARIOS ANTES DE PUBLICAR

### 1. Añadir las imágenes
Guarda la foto del gimnasio como `assets/gym.jpg`.
Si tienes foto de Miguel, guárdala como `assets/miguel.jpg` y en `index.html` 
reemplaza el bloque `trainer-photo-placeholder` por:
```html
<img src="assets/miguel.jpg" alt="Miguel Oliver Ramírez — Head Coach F96" />
```

---

### 2. Configurar Calendly + Google Calendar

**Paso a paso:**

1. Ve a https://calendly.com y crea una cuenta gratuita con el email del negocio.

2. Una vez dentro, ve a **"Event Types"** → **"+ New Event Type"**
   - Nombre: "Primera clase F96" (o el que prefieras)
   - Duración: la que corresponda a tu sesión (ej. 60 min)
   - Disponibilidad: configura los días y horas en que se pueden reservar clases

3. Conecta Google Calendar:
   - Ve a **"Integrations"** en el menú lateral
   - Busca **Google Calendar** y haz clic en **"Connect"**
   - Autoriza el acceso con tu cuenta de Google
   - Calendly leerá tu calendario para no solapar citas y escribirá las reservas nuevas

4. Copia tu URL de evento. Tendrá este formato:
   ```
   https://calendly.com/TU_USUARIO/primera-clase
   ```

5. Abre `landing.html` y busca la línea:
   ```
   data-url="https://calendly.com/TU_USUARIO/primera-clase?..."
   ```
   Reemplaza `TU_USUARIO/primera-clase` con tu URL real.

---

### 3. Cookies — ¿necesito hacer algo más?

El banner de cookies **ya está integrado** en el código y funciona sin plugins externos.
Guarda la preferencia del usuario en su navegador.

**Sin embargo, para cumplir con la RGPD (ley europea de cookies) necesitarás:**

- Crear una página de **Política de Cookies** explicando qué cookies usas
  (si solo usas Calendly y no tienes analytics, es bastante sencillo)
- Si añades Google Analytics u otras cookies de seguimiento en el futuro,
  deberás actualizar el banner para bloquearlas hasta que el usuario acepte
- La solución actual es suficiente para un sitio sencillo sin analytics

**Opción avanzada (gratuita):** puedes usar Cookiebot (https://www.cookiebot.com)
que escanea tu web y genera la política automáticamente. Su plan gratuito 
cubre hasta 1 dominio con menos de 100 subpáginas.

---

### 4. Datos pendientes de revisar en el código

Busca estos comentarios en los archivos HTML para completarlos:

| Comentario | Qué hacer |
|---|---|
| `<!-- Review business name -->` | Confirmar que "F96" es el nombre definitivo |
| `[Revisar precio]` | Añadir precios reales en la sección de tarifas |
| `[Revisar y completar]` | Completar máster y experiencia de Miguel |
| `info@f96.es` | Cambiar por el email real del negocio |
| `[Teléfono por confirmar]` | Añadir teléfono de contacto |
| `[Dirección por confirmar]` | Añadir dirección física |

---

### 5. Cómo publicar el sitio (hosting estático)

Opciones recomendadas para un sitio estático como este:

- **Netlify** (https://netlify.com) — gratis, arrastra la carpeta y listo
- **Vercel** (https://vercel.com) — gratis, muy rápido
- **GitHub Pages** — gratis si el repo es público

Para cualquiera de ellas: sube la carpeta `f96/` completa con las imágenes dentro.

---

### 6. Dominio personalizado (f96.es o similar)

Una vez publicado en Netlify/Vercel, puedes conectar un dominio propio.
El proceso es: comprar dominio → apuntar DNS a Netlify/Vercel → configurar en el panel.
Cada plataforma tiene una guía paso a paso para esto.
