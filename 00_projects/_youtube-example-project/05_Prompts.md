# 🎬 Prompts para Generación de Contenido

**Proyecto:** Pomeranian tries to be a Police
**Duración:** 2 minutos (24 shots × 5 segundos)
**Resolución:** 720p
**Formato:** JPEG

---

## 📋 Referencias de Dirección de Arte

### Imágenes base para usar como referencias:

| Shot | Referencia Principal | URL |
|------|-----------------|------|
| 01-06 | Pomerania Pajamas | `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-26.png` |
| 01-02 | Dormitorio | `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-18-50.jpeg` |
| 03 | Dormitorio | `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-18-50.jpeg` |
| 04-05 | Cocina | `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-35.jpeg` |
| 06 | Pomerania Police | `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-31.jpeg` |

---

## 🔄 Workflow de Generación

**IMPORTANTE:** Se genera en 2 FASES por cada shot

### FASE 1️⃣: Generar START IMAGE
1. Enviar prompt a Nano Banana EDIT con imágenes de dirección de arte como referencias
2. Esperar respuesta
3. **REVISAR Y APROBAR** la imagen antes de continuar
4. Guardar URL de la imagen aprobada

### FASE 2️⃣: Generar END IMAGE (usando START IMAGE como referencia)
1. Enviar prompt a Nano Banana EDIT con:
   - La START IMAGE como `image_urls` (REFERENCIA)
   - Instrucción clara en el prompt de qué cambiar
2. Esperar respuesta
3. REVISAR Y APROBAR
4. Guardar URL
5. Una vez ambas imágenes aprobadas → Generar VIDEO con Seedance

---

## 🎭 ACTO 1 - DESPERTAR (6 Shots - 30 segundos)

**Tone:** Tierno, esperanzador, adorable
**Mood:** Transición de sueño a despertar con determinación creciente

---

## Shot-01: First Frame - Durmiendo Peacefully

### FASE 1️⃣ - START IMAGE: Max durmiendo en la cama

**Referencias a enviar:**
- Dormitorio: `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-18-50.jpeg`
- Pomerania Pajamas: `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-26.png`

**Prompt:**
```
Using the bedroom reference and the pomerania character reference as visual guides:
Create an ultra-high quality cinematic image of a small fluffy white Pomerania puppy sleeping peacefully in a cozy bed.
The puppy wears soft pink pajamas (use character reference for consistency).
The bedroom matches the reference location with warm tones, beige walls, white pillows.
Close-up of the face showing adorable serene expression, eyes closed, pink tongue slightly out.
Warm golden lighting with shallow depth of field and bokeh highlights on fur.
Professional 3D render style, Pixar quality, 1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-18-50.jpeg",
      "https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-26.png"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

**Endpoint:** `https://n8n.lemonsushi.com/webhook-test/tataraVideo_nanoBanana_genImage`

✅ **REVISAR Y APROBAR la imagen. Guardar URL como [SHOT-01-START-URL]**

---

### FASE 2️⃣ - END IMAGE: Max con ojos entreabiertos despertándose

**Referencia a enviar:**
- START IMAGE aprobada: `[SHOT-01-START-URL]`

**Prompt:**
```
Using the approved sleeping image as reference:
Modify to show the same white Pomerania puppy beginning to wake up.
Keep the same bedroom setting and character consistency.
The puppy's eyes are now slightly open, transitioning from sleep to consciousness.
Soft transition state, same warm golden lighting.
Maintain the pink pajamas and all other visual elements from the reference.
Subtle changes only - minor adjustment to show waking process.
Professional 3D render, 1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-01-START-URL]"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-01-END-URL]**

---

### Video para Shot-01 (después de ambas imágenes aprobadas)

**Prompt Seedance:**
```
Soft cinematic transition. Small fluffy white Pomerania puppy wakes up slowly. Eyes open from closed to fully alert expression. Subtle head movement lifting from pillow. Warm golden bedroom lighting. Close-up focus on face and eyes. Soft, gentle, adorable. No camera movement. Gentle and tender mood.
```

**JSON a enviar:**
```json
{
  "model": "bytedance/v1-lite-image-to-video",
  "input": {
    "prompt": "[Prompt Seedance arriba]",
    "image_url": "[SHOT-01-START-URL]",
    "end_image_url": "[SHOT-01-END-URL]",
    "resolution": "720p",
    "duration": "5",
    "camera_fixed": true
  }
}
```

---

## Shot-02: Estiramiento y Bostezar

### FASE 1️⃣ - START IMAGE: Max despertado en la cama

**Referencias a enviar:**
- Shot-01-END (aprobada): `[SHOT-01-END-URL]`
- Dormitorio: `https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg`
- Pomerania Pajamas: `https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg`

**Prompt:**
```
Using the previous shot (puppy beginning to wake up) for continuity and the character references:
Show the same small white fluffy Pomerania puppy now fully awake in the same cozy bed.
Eyes are open wide with an alert, energized expression.
The puppy is just beginning to stretch slightly.
Same bedroom environment with warm golden lighting.
Close-up of upper body on soft pillows, showing the pink pajamas clearly.
Same character consistency and professional cinematography.
1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-01-END-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg",
      "https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-02-START-URL]**

---

### FASE 2️⃣ - END IMAGE: Max estirándose y bostezando

**Referencia a enviar:**
- START IMAGE aprobada: `[SHOT-02-START-URL]`

**Prompt:**
```
Using the awake puppy image as reference:
Modify to show the same Pomerania puppy with a big stretching motion.
Front paws are extending forward in a stretch.
Wide open mouth yawning, showing both cuteness and determination.
Big eyes expressing the yawn sensation.
Same warm bedroom lighting with same background.
Still in the same bed but with dynamic stretching pose.
Maintain character consistency and pink pajamas visibility.
Professional 3D render, 1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-02-START-URL]"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-02-END-URL]**

---

### Video para Shot-02

**Prompt Seedance:**
```
Adorable white Pomerania puppy wakes up in cozy bed. Big stretching motion, front paws extending forward. Wide mouth yawn showing determination and cuteness. Camera slowly zooms in slightly on the face. Warm bedroom lighting with bokeh highlights on fur. Cinematic close-up. Fluffy white fur with soft shadows. Tender and heartwarming mood.
```

**JSON a enviar:**
```json
{
  "model": "bytedance/v1-lite-image-to-video",
  "input": {
    "prompt": "[Prompt Seedance arriba]",
    "image_url": "[SHOT-02-START-URL]",
    "end_image_url": "[SHOT-02-END-URL]",
    "resolution": "720p",
    "duration": "5",
    "camera_fixed": false
  }
}
```

---

## Shot-03: Aseo y Grooming

### FASE 1️⃣ - START IMAGE: Max saliendo de la cama

**Referencias a enviar:**
- Shot-02-END (aprobada): `[SHOT-02-END-URL]`
- Dormitorio: `https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg`
- Pomerania Pajamas: `https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg`

**Prompt:**
```
Using the previous shot for continuity and references:
Show the same small white Pomerania puppy getting out of bed, standing up.
Stretched and energized after waking up.
Bedroom interior visible with warm tones.
Soft natural light from window illuminating the puppy.
Professional cinematography.
Cute determined expression on the puppy's face.
Still wearing the pink pajamas.
Transition state between bed and next activity.
1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-02-END-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg",
      "https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-03-START-URL]**

---

### FASE 2️⃣ - END IMAGE: Max frente al espejo acicalándose

**Referencia a enviar:**
- START IMAGE aprobada: `[SHOT-03-START-URL]`
- Dormitorio: `https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg`

**Prompt:**
```
Using the standing puppy image as reference:
Show the same Pomerania puppy now sitting in front of a bedroom mirror, grooming itself.
Paw brushing through fluffy white fur, licking paw.
Focused and determined expression with big eyes showing concentration.
Soft natural light from window illuminating the beautiful fluffy fur.
Professional grooming pose.
The puppy is grooming itself with care and attention.
Same bedroom interior as reference.
Maintain character consistency.
Professional 3D render, 1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-03-START-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-03-END-URL]**

---

### Video para Shot-03

**Prompt Seedance:**
```
Small white Pomerania puppy sitting in front of bedroom mirror, grooming itself. Paw brushing through fluffy white fur, licking paw, determined expression with big eyes. Soft natural light from window illuminating the fur. Medium shot framing. Camera slight pan to the right. Transition from relaxed to focused mood. Professional cinematography.
```

**JSON a enviar:**
```json
{
  "model": "bytedance/v1-lite-image-to-video",
  "input": {
    "prompt": "[Prompt Seedance arriba]",
    "image_url": "[SHOT-03-START-URL]",
    "end_image_url": "[SHOT-03-END-URL]",
    "resolution": "720p",
    "duration": "5",
    "camera_fixed": false
  }
}
```

---

## Shot-04: Transición a Cocina

### FASE 1️⃣ - START IMAGE: Max frente al espejo terminando grooming

**Referencia a enviar:**
- Shot-03-END (aprobada): `[SHOT-03-END-URL]`
- Dormitorio: `https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg`

**Prompt:**
```
Using the grooming image as reference:
Show the same white Pomerania puppy in front of the bedroom mirror, finished grooming.
Alert and energized after grooming.
Bright eyes with confident expression.
Bedroom interior with warm lighting.
Professional cinematography.
Expression shows growing determination and readiness.
The puppy appears energized and prepared for the day.
1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-03-END-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/dormitorio.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-04-START-URL]**

---

### FASE 2️⃣ - END IMAGE: Max en la cocina sentado en silla

**Referencia a enviar:**
- START IMAGE aprobada: `[SHOT-04-START-URL]`
- Cocina: `https://lemonsushi.com/uploads/tataraVideo/files/cocina.jpeg`
- Pomerania Pajamas: `https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg`

**Prompt:**
```
Using the energized puppy from previous shot for character consistency:
Show the same tiny white Pomerania puppy now in a modern minimalist kitchen.
The puppy is sitting on a small chair at dining table scale.
Food bowl visible on the table.
Excited and eager expression.
Natural light flooding from kitchen window.
Professional interior photography style.
The scene transitions from bedroom to kitchen.
Same character consistency with pink pajamas still visible.
Professional 3D render, 1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-04-START-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/cocina.jpeg",
      "https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-04-END-URL]**

---

### Video para Shot-04

**Prompt Seedance:**
```
Small white Pomerania puppy transitions from bedroom mirror to kitchen. Quick dynamic movement. Scene shifts from bedroom to modern minimalist kitchen. Dog appears more energized and focused. Natural light transitions from bedroom golden to bright kitchen sunlight. Mood escalates from grooming routine to breakfast preparation.
```

**JSON a enviar:**
```json
{
  "model": "bytedance/v1-lite-image-to-video",
  "input": {
    "prompt": "[Prompt Seedance arriba]",
    "image_url": "[SHOT-04-START-URL]",
    "end_image_url": "[SHOT-04-END-URL]",
    "resolution": "720p",
    "duration": "5",
    "camera_fixed": false
  }
}
```

---

## Shot-05: Desayuno

### FASE 1️⃣ - START IMAGE: Max en cocina antes de comer

**Referencia a enviar:**
- Shot-04-END (aprobada): `[SHOT-04-END-URL]`
- Cocina: `https://lemonsushi.com/uploads/tataraVideo/files/cocina.jpeg`
- Pomerania Pajamas: `https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg`

**Prompt:**
```
Using the puppy in kitchen as reference:
Show the same tiny white Pomerania puppy in modern minimalist kitchen.
Sitting on small chair at dining table scale.
Empty food bowl in front ready for breakfast.
Alert and hungry expression.
Big eyes showing anticipation.
Natural light from window.
Professional food photography lighting.
Cinematic quality.
Same character consistency.
1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-04-END-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/cocina.jpeg",
      "https://lemonsushi.com/uploads/tataraVideo/files/pomerania-pajamas.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-05-START-URL]**

---

### FASE 2️⃣ - END IMAGE: Max comiendo del tazón

**Referencia a enviar:**
- START IMAGE aprobada: `[SHOT-05-START-URL]`

**Prompt:**
```
Using the hungry puppy image as reference:
Modify to show the same Pomerania puppy eating from a full food bowl.
Head down in the bowl eating enthusiastically.
Satisfied and energized expression visible.
Same natural kitchen lighting from window.
Same chair and table scale.
Dynamic eating pose.
Professional food photography style.
Maintain character consistency throughout.
Professional 3D render, 1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-05-START-URL]"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-05-END-URL]**

---

### Video para Shot-05

**Prompt Seedance:**
```
Tiny white Pomerania puppy eating from a food bowl in modern minimalist kitchen. Dog sitting on small chair at dining table scale. Dynamic quick energetic movement. Cutaway shots: mouth in bowl, head up with satisfied expression, determination growing. Natural light flooding from window. Quick pans montage style. Mood transitions from cozy to energetic. Professional food photography style.
```

**JSON a enviar:**
```json
{
  "model": "bytedance/v1-lite-image-to-video",
  "input": {
    "prompt": "[Prompt Seedance arriba]",
    "image_url": "[SHOT-05-START-URL]",
    "end_image_url": "[SHOT-05-END-URL]",
    "resolution": "720p",
    "duration": "5",
    "camera_fixed": false
  }
}
```

---

## Shot-06: Decisión - Transformación Épica

### FASE 1️⃣ - START IMAGE: Max terminando de comer

**Referencia a enviar:**
- Shot-05-END (aprobada): `[SHOT-05-END-URL]`
- Cocina: `https://lemonsushi.com/uploads/tataraVideo/files/cocina.jpeg`

**Prompt:**
```
Using the eating puppy as reference:
Show the same small white fluffy Pomerania puppy finishing meal in kitchen.
Head up from food bowl.
Energized, satisfied expression.
Eyes bright and focused.
Natural kitchen lighting from window.
Professional cinematography.
Mood shows transition from breakfast routine to growing determination.
Same character consistency.
1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-05-END-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/cocina.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-06-START-URL]**

---

### FASE 2️⃣ - END IMAGE: Max de pie determinado (transformación épica)

**Referencia a enviar:**
- START IMAGE aprobada: `[SHOT-06-START-URL]`
- Pomerania Police: `https://lemonsushi.com/uploads/tataraVideo/files/pomerania-police.jpeg`

**Prompt:**
```
Using the energized puppy image and the police character reference for inspiration:
Show the same white fluffy Pomerania puppy now standing on hind legs.
Transformed demeanor - energized and determined expression.
Eyes bright and focused.
Cinematic lighting, dramatic but still adorable.
Powerful stance showing readiness for action.
Ready and epic moment.
Background subtle transition from kitchen.
Same character consistency but with grown confidence.
Professional cinematography, Disney/Pixar quality.
1920x1080, no watermark.
```

**JSON a enviar:**
```json
{
  "model": "google/nano-banana-edit",
  "input": {
    "prompt": "[Prompt completo arriba]",
    "image_urls": [
      "[SHOT-06-START-URL]",
      "https://lemonsushi.com/uploads/tataraVideo/files/pomerania-police.jpeg"
    ],
    "output_format": "jpeg",
    "image_size": "16:9"
  }
}
```

✅ **REVISAR Y APROBAR. Guardar URL como [SHOT-06-END-URL]**

---

### Video para Shot-06

**Prompt Seedance:**
```
Small white fluffy Pomerania puppy stands on hind legs, transformed demeanor. Energized and determined expression. Eyes bright and focused. Cinematic lighting, dramatic but still adorable. Camera pull back slowly from close-up. Mood shifts from breakfast routine to epic determination. Rise in tension, hopeful and determined energy. Professional cinematography, Disney/Pixar quality.
```

**JSON a enviar:**
```json
{
  "model": "bytedance/v1-lite-image-to-video",
  "input": {
    "prompt": "[Prompt Seedance arriba]",
    "image_url": "[SHOT-06-START-URL]",
    "end_image_url": "[SHOT-06-END-URL]",
    "resolution": "720p",
    "duration": "5",
    "camera_fixed": false
  }
}
```

---

## 📊 Resumen - ACTO 1

| Shot | Tipo | Duración | Imágenes | Estado |
|------|------|----------|----------|--------|
| 01 | Video | 5s | 2 | ⏳ En generación |
| 02 | Video | 5s | 2 | ⏳ En generación |
| 03 | Video | 5s | 2 | ⏳ En generación |
| 04 | Video | 5s | 2 | ⏳ En generación |
| 05 | Video | 5s | 2 | ⏳ En generación |
| 06 | Video | 5s | 2 | ⏳ En generación |

**Total Imágenes:** 12 (6 inicio + 6 fin)
**Total Videos:** 6
**Duración Total:** 30 segundos
**Costo Estimado (720p):** 112.5 créditos

---

## ✅ Estado

**Fecha:** 2026-01-11
**Status:** ✅ Prompts listos para generación
**Próximo Paso:** Empezar con Shot-01 FASE 1 (generar START IMAGE)
