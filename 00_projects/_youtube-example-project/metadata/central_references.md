# Central References - Pomeranian tries to be a Police

**MASTER REFERENCE FILE** - Single source of truth for all URLs used in this project.

Every URL is defined ONCE here. All other files use reference tags `[TAG-NAME]` that point to this source.

---

## CHARACTER REFERENCES

### [POMERANIAN-PAJAMAS-REF]
- **URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-26.png`
- **Description:** Max the Pomeranian wearing pajamas
- **Local File:** `/media/_youtube-example-project/art/characters/pomerania-pajamas.jpg`
- **Used in:** All Act 1 shots (01-06) - Bedroom and kitchen scenes
- **Associated Colors:**
  - Soft Pink: `#ffb6c1` (Pajamas)
  - White: `#ffffff` (Fur, ears with bows)

### [POMERANIAN-POLICE-REF]
- **URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-31.jpeg`
- **Description:** Max the Pomeranian wearing police uniform
- **Local File:** `/media/_youtube-example-project/art/characters/pomerania-police.jpg`
- **Used in:** All Act 2-4 shots (07-24) - Police station and action scenes
- **Associated Colors:**
  - Dark Blue: `#0a1428` (Police uniform)
  - Gold: `#d4af37` (Badge)

---

## LOCATION REFERENCES

### [BEDROOM-REF]
- **URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-18-50.jpeg`
- **Description:** Cozy bedroom setting
- **Local File:** `/media/_youtube-example-project/art/locations/dormitorio.jpeg`
- **Used in:** Shots 01-04, 06 (Act 1 start and end)
- **Associated Colors:**
  - Warm Beige: `#f5e6d3` (Warm backgrounds)
  - White: `#ffffff` (Bedding)

### [KITCHEN-REF]
- **URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-17-35.jpeg`
- **Description:** Modern minimalist kitchen setting
- **Local File:** `/media/_youtube-example-project/art/locations/cocina.jpeg`
- **Used in:** Shots 04-05 (Act 1 transition)
- **Associated Colors:**
  - White: `#ffffff` (Modern appliances)
  - Professional Gray: `#808080` (Kitchen elements)

### [POLICE-STATION-EXTERIOR-REF]
- **URL:** `https://lemonsushi.com/uploads/tataraVideo/files/[pending]`
- **Description:** Large imposing police station building exterior
- **Local File:** `/media/_youtube-example-project/art/locations/estacion-exterior.jpeg`
- **Used in:** Shots in Act 2-3 (exterior approach)
- **Associated Colors:**
  - Dark Blue: `#0a1428` (Building, institution)
  - White: `#ffffff` (Architectural details)

### [POLICE-STATION-INTERIOR-REF]
- **URL:** `https://lemonsushi.com/uploads/tataraVideo/files/[pending]`
- **Description:** Professional police station interior with desks and institutional elements
- **Local File:** `/media/_youtube-example-project/art/locations/estacion-interior.jpeg`
- **Used in:** Shots in Act 3 (interior action)
- **Associated Colors:**
  - Dark Blue: `#0a1428` (Institutional elements)
  - Professional Gray: `#808080` (Walls, desks)
  - White: `#ffffff` (Fluorescent lights)

---

## ACT 1 - AWAKENING IMAGE REFERENCES

### SHOT-01: First Frame - Sleeping Peacefully

#### [SHOT-01-PHASE1-URL]
- **Definition:** First image of Shot-01 (Max sleeping peacefully in bed)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-11_15-23-58.jpeg`
- **Generation Timestamp:** `2026-01-11_15-23-58`
- **Status:** ✅ Approved, Version 1.0
- **Character Reference Used:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference Used:** [BEDROOM-REF]
- **Model:** `google/nano-banana-edit`
- **Generation Time:** 16 seconds
- **Used In:**
  - images_metadata.md (source)
  - prompts_metadata.md (reference)
  - 05_Prompts.md (display)
  - 08_ShotImages.md (display)
  - 09_ShotVideos.md (video source)

#### [SHOT-01-PHASE2-URL]
- **Definition:** Second image of Shot-01 (Max waking up)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_03-47-28.jpeg`
- **Generation Timestamp:** `2026-01-12_03-47-28`
- **Status:** ✅ Approved, Version 1.0
- **Character Reference Used:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference Used:** [BEDROOM-REF]
- **References for Generation:** [SHOT-01-PHASE1-URL], [BEDROOM-REF], [POMERANIAN-PAJAMAS-REF]
- **Model:** `google/nano-banana-edit`
- **Generation Time:** ~15 seconds
- **Used In:**
  - images_metadata.md (source)
  - prompts_metadata.md (reference)
  - 05_Prompts.md (display)
  - 08_ShotImages.md (display)
  - 09_ShotVideos.md (video source)

### SHOT-02: Stretching and Yawning

#### [SHOT-02-PHASE1-URL]
- **Definition:** First image of Shot-02 (Max awakened in bed, completely awake)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_13-45-12.jpeg`
- **Generation Timestamp:** `2026-01-12_13-45-12`
- **Status:** ✅ Approved, Version 1.0
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [BEDROOM-REF]
- **Model:** `google/nano-banana-edit`
- **Generation Time:** 24 seconds

#### [SHOT-02-PHASE2-URL]
- **Definition:** Second image of Shot-02 (Max stretching and yawning)
- **Status:** ⏳ Pending Generation
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [BEDROOM-REF]

### SHOT-03: Grooming and Cleaning

#### [SHOT-03-PHASE1-URL]
- **Definition:** First image of Shot-03 (Max getting out of bed)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_14-00-19.jpeg`
- **Generation Timestamp:** `2026-01-12_14-00-19`
- **Status:** ✅ Approved, Version 1.0
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [BEDROOM-REF]
- **Model:** `google/nano-banana-edit`
- **Generation Time:** 18 seconds

#### [SHOT-03-PHASE2-URL]
- **Definition:** Second image of Shot-03 (Max in front of mirror grooming himself)
- **Status:** ⏳ Pending Generation
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [BEDROOM-REF]

### SHOT-04: Transition to Kitchen

#### [SHOT-04-PHASE1-URL]
- **Definition:** First image of Shot-04 (Max in front of mirror finishing grooming)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_14-00-19.jpeg`
- **Generation Timestamp:** `2026-01-12_14-00-19`
- **Status:** ✅ Approved, Version 1.0
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [BEDROOM-REF]
- **Model:** `google/nano-banana-edit`
- **Generation Time:** 19 seconds

#### [SHOT-04-PHASE2-URL]
- **Definition:** Second image of Shot-04 (Max in kitchen sitting on chair)
- **Status:** ⏳ Pending Generation
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [KITCHEN-REF]

### SHOT-05: Breakfast

#### [SHOT-05-PHASE1-URL]
- **Definition:** First image of Shot-05 (Max in kitchen before eating)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_14-00-19.jpeg`
- **Generation Timestamp:** `2026-01-12_14-00-19`
- **Status:** ✅ Approved, Version 1.0
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [KITCHEN-REF]
- **Model:** `google/nano-banana-edit`
- **Generation Time:** 19 seconds

#### [SHOT-05-PHASE2-URL]
- **Definition:** Second image of Shot-05 (Max eating from bowl)
- **Status:** ⏳ Pending Generation
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [KITCHEN-REF]

### SHOT-06: Decision - Epic Transformation

#### [SHOT-06-PHASE1-URL]
- **Definition:** First image of Shot-06 (Max finishing eating)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_14-00-19.jpeg`
- **Generation Timestamp:** `2026-01-12_14-00-19`
- **Status:** ✅ Approved, Version 1.0
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [KITCHEN-REF]
- **Model:** `google/nano-banana-edit`
- **Generation Time:** 17 seconds

#### [SHOT-06-PHASE2-URL]
- **Definition:** Second image of Shot-06 (Max standing determined - epic transformation)
- **Status:** ⏳ Pending Generation
- **Character Reference:** [POMERANIAN-PAJAMAS-REF]
- **Location Reference:** [KITCHEN-REF]

---

## VIDEO REFERENCES

### [SHOT-01-VIDEO-URL]
- **Definition:** Video transition for Shot-01 (sleeping to waking)
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/2026-01-12_09-32-21.mp4`
- **Generation Timestamp:** `2026-01-12_09-32-21`
- **Status:** ✅ Completed, Version 1.0
- **Model:** `bytedance/v1-lite-image-to-video` (Seedance V1)
- **Resolution:** 480p
- **Duration:** 5 seconds
- **Generation Time:** 55 seconds
- **Phase 1 Reference:** [SHOT-01-PHASE1-URL]
- **Phase 2 Reference:** [SHOT-01-PHASE2-URL]
- **Used In:**
  - videos_metadata.md (source)
  - 09_ShotVideos.md (display)

---

## COLOR PALETTE CODES

### Main Colors
- **[DARK-BLUE]** = `#0a1428` (Police uniform, institutional buildings)
- **[SOFT-PINK]** = `#ffb6c1` (Pajamas, adorable elements)
- **[GOLD]** = `#d4af37` (Police badge, authority details)
- **[WHITE]** = `#ffffff` (Max's fur, clean details)

### Secondary Colors
- **[WARM-BEIGE]** = `#f5e6d3` (Warm backgrounds, bedroom)
- **[PROFESSIONAL-GRAY]** = `#808080` (Station, interior scenes)
- **[SOFT-GREEN]** = `#a8d5ba` (Nature, street, exteriors)

---

## REFERENCE USAGE GUIDE

### How to Use These Tags

**In prompts (05_Prompts.md):**
```markdown
Using [BEDROOM-REF] and [POMERANIAN-PAJAMAS-REF] as visual guides:
Create an ultra-high quality cinematic image of Max sleeping...
```

**In metadata (images_metadata.md):**
```markdown
- Character Reference Used: [POMERANIAN-PAJAMAS-REF]
- Location Reference Used: [BEDROOM-REF]
```

**In review files (08_ShotImages.md):**
```markdown
### Shot-01 PHASE 1: Max sleeping
- Status: ✅ Approved
- Image: [SHOT-01-PHASE1-URL]
```

### Claude's Resolution Process

When Claude sees a tag like `[BEDROOM-REF]`:
1. Finds it in this file
2. Extracts the URL
3. Sends the actual URL to n8n webhooks
4. Records the reference used in metadata

---

## Update Procedure

When regenerating or updating:

### Step 1: Generate new image
```
Claude generates new image with feedback
```

### Step 2: Update this file ONLY
```markdown
#### [SHOT-01-PHASE1-URL]
- **FTP URL:** `https://lemonsushi.com/uploads/tataraVideo/files/[NEW-TIMESTAMP].jpeg`
- **Status:** ✅ Approved, Version 2.0
- Previous version: Version 1.0 (in version history)
```

### Step 3: All references automatically updated
```
All files using [SHOT-01-PHASE1-URL] now point to the new URL
No manual updates needed in other files ✅
```

---

## Files That Depend on This

| File | Reads From | Purpose |
|------|-----------|---------|
| `05_Prompts.md` | central_references.md | Uses tags in generation prompts |
| `metadata/images_metadata.md` | central_references.md | Source records, uses same tags |
| `metadata/videos_metadata.md` | central_references.md | Source records for videos |
| `08_ShotImages.md` | central_references.md | Review file, displays with tags |
| `09_ShotVideos.md` | central_references.md | Review file, displays with tags |
| `metadata/prompts_metadata.md` | central_references.md | Records actual URLs expanded |

---

## Version History

When a reference is regenerated, old version is preserved:

```markdown
#### [SHOT-01-PHASE1-URL]

**Version 2.0 (Current)**
- URL: https://lemonsushi.com/uploads/tataraVideo/files/[NEW].jpeg

**Version 1.0 (Previous)**
- URL: https://lemonsushi.com/uploads/tataraVideo/files/[OLD].jpeg
- Status: Replaced due to feedback
```

