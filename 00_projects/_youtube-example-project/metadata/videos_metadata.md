# Metadata - Shot Videos

Detailed technical information for all videos generated for the "Pomeranian tries to be a Police" project.

**Reference System:** This file uses tags like `[SHOT-01-PHASE1-URL]` and `[SHOT-01-VIDEO-URL]` that are defined in `metadata/central_references.md`. See that file for URL definitions and cross-references.

---

## ACT 1 - AWAKENING

### Shot-01: First Frame - Sleeping Peacefully

**Version Status: ⏳ Pending Generation**

**Images Required:**
- **Image Start (PHASE 1):** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-23-58.jpeg` ✅ Approved
- **Image End (PHASE 2):** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_03-47-28.jpeg` ✅ Approved

**Video Parameters:**
- **Model:** `bytedance/v1-lite-image-to-video` (Seedance V1)
- **Resolution:** 720p
- **Duration:** 5 seconds
- **FPS:** 24
- **Aspect Ratio:** 16:9
- **Camera:** Fixed (no movement)
- **Webhook:** `/webhook/tataraVideo_seedance_genVideo` (Production)

**Description:** Smooth transition from Max sleeping to waking up, with subtle head movement

**Prompt Used:** See `05_Prompts.md` > ACT 1 > Shot-01 > Video

**Notes:** Ready to generate when approved. Both images are approved and ready for video generation

---

### Shot-02: Stretching and Yawning

**Status:** ⏳ Pending

**Description:** Adorable white Pomeranian puppy wakes up in cozy bed, big stretching motion

**Parameters:** Standard (see Global Parameters section)

---

### Shot-03: Grooming and Cleaning

**Status:** ⏳ Pending

**Description:** Small white Pomeranian puppy sitting in front of bedroom mirror, grooming itself

**Parameters:** Standard (see Global Parameters section)

---

### Shot-04: Transition to Kitchen

**Status:** ⏳ Pending

**Description:** Small white Pomeranian puppy transitions from bedroom mirror to kitchen

**Parameters:** Standard (see Global Parameters section)

---

### Shot-05: Breakfast

**Status:** ⏳ Pending

**Description:** Tiny white Pomeranian puppy eating from a food bowl in modern minimalist kitchen

**Parameters:** Standard (see Global Parameters section)

---

### Shot-06: Decision - Epic Transformation

**Status:** ⏳ Pending

**Description:** Small white fluffy Pomeranian puppy stands on hind legs, transformed demeanor

**Parameters:** Standard (see Global Parameters section)

---

## Progress Summary

| Act | Shot | VIDEO | Status |
|------|------|-------|--------|
| 1 | 01 | ⏳ Pending | Waiting |
| 1 | 02-06 | ⏳ Pending | Waiting |

**Total Completed:** 0/24 videos (0%)

---

## Global Video Parameters

**Standard for All Videos:**
- **Model:** `bytedance/v1-lite-image-to-video`
- **Resolution:** 720p
- **Duration:** 5 seconds
- **FPS:** 24
- **Aspect Ratio:** 16:9
- **Camera:** Fixed (true)
- **Format:** MP4
- **Webhook:** `/webhook/tataraVideo_seedance_genVideo` (Production)

**Generation Structure:**
1. Requires PHASE 1 (START IMAGE) ✅ Approved
2. Requires PHASE 2 (END IMAGE) ✅ Approved
3. Video is generated as smooth transition between both images

**Naming Convention:**
- Video is stored with automatic timestamp when uploading to FTP
- Format: `YYYY-MM-DD_HH-MM-SS.mp4`

**References for Generation:**
- Video prompts are in `05_Prompts.md` with hierarchical structure by Act
- Source images are cataloged in `images_metadata.md`
- Global technical parameters are in `00_Settings-Status.md`
