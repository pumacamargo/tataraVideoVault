# Metadata - Shot Videos

Información técnica detallada de todos los videos generados para el proyecto "Pomeranian tries to be a Police".

---

## ACTO 1 - DESPERTAR

### Shot-01: First Frame - Durmiendo Peacefully

**Estado:** ⏳ Pendiente

**Información Técnica:**
- **Modelo:** `bytedance/v1-lite-image-to-video` (Seedance V1)
- **Resolución:** 720p
- **Duración:** 5 segundos
- **FPS:** 24
- **Aspect Ratio:** 16:9
- **Cámara:** Fixed (sin movimiento)
- **Webhook:** `/webhook/tataraVideo_seedance_genVideo` (Production)

**Imágenes Utilizadas:**
- **Image Start (FASE 1):** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-23-58.jpeg`
- **Image End (FASE 2):** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_03-47-28.jpeg`

**Descripción:** Transición suave de Max durmiendo a despertándose, con movimiento sutil de cabeza

**Prompt Usado:** Vea `05_Prompts.md` > ACTO 1 > Shot-01 > Video

---

### Shot-02: Estiramiento y Bostezar

**Estado:** ⏳ Pendiente

**Descripción:** Adorable white Pomerania puppy wakes up in cozy bed, big stretching motion

**Parámetros:** Estándar (ver sección de Parámetros Globales)

---

### Shot-03: Aseo y Grooming

**Estado:** ⏳ Pendiente

**Descripción:** Small white Pomerania puppy sitting in front of bedroom mirror, grooming itself

**Parámetros:** Estándar (ver sección de Parámetros Globales)

---

### Shot-04: Transición a Cocina

**Estado:** ⏳ Pendiente

**Descripción:** Small white Pomerania puppy transitions from bedroom mirror to kitchen

**Parámetros:** Estándar (ver sección de Parámetros Globales)

---

### Shot-05: Desayuno

**Estado:** ⏳ Pendiente

**Descripción:** Tiny white Pomerania puppy eating from a food bowl in modern minimalist kitchen

**Parámetros:** Estándar (ver sección de Parámetros Globales)

---

### Shot-06: Decisión - Transformación Épica

**Estado:** ⏳ Pendiente

**Descripción:** Small white fluffy Pomerania puppy stands on hind legs, transformed demeanor

**Parámetros:** Estándar (ver sección de Parámetros Globales)

---

## Resumen de Progreso

| Acto | Shot | VIDEO | Estado |
|------|------|-------|--------|
| 1 | 01 | ⏳ Pendiente | En espera |
| 1 | 02-06 | ⏳ Pendiente | En espera |

**Total Completado:** 0/24 videos (0%)

---

## Parámetros Globales de Video

**Estándar para Todos los Videos:**
- **Modelo:** `bytedance/v1-lite-image-to-video`
- **Resolución:** 720p
- **Duración:** 5 segundos
- **FPS:** 24
- **Aspect Ratio:** 16:9
- **Cámara:** Fixed (true)
- **Formato:** MP4
- **Webhook:** `/webhook/tataraVideo_seedance_genVideo` (Production)

**Estructura de Generación:**
1. Requiere FASE 1 (START IMAGE) ✅ Aprobado
2. Requiere FASE 2 (END IMAGE) ✅ Aprobado
3. Video se genera como transición suave entre ambas imágenes

**Convención de Naming:**
- Video se almacena con timestamp automático al uploadear a FTP
- Formato: `YYYY-MM-DD_HH-MM-SS.mp4`

**Referencias para Generación:**
- Los prompts de video están en `05_Prompts.md` con estructura jerárquica por Acto
- Las imágenes source están catalogadas en `images_metadata.md`
- Los parámetros técnicos globales están en `00_Settings-Status.md`
