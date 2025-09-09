# Kypria Dual‑Purpose Banner — Layer Architecture

> Defines the canonical stacking order and responsibilities of each layer group in the master 1500 × 640 px dual‑purpose banner file (GitHub Org Social Preview + Twitter/X Header). Use with:  
> - `dual-purpose-banner-template.md` (spec)  
> - `dual-purpose-banner-safe-zone-overlay.md` (overlay guide)

---

## 1. Layer Stack (Top → Bottom)

```
LAYER 1: LABELS (GUIDE ONLY)
LAYER 2: SHARED SAFE ZONE RECTANGLE (GUIDE)
LAYER 3: GITHUB SAFE WIDTH RECTANGLE (GUIDE)
LAYER 4: TWITTER/X SAFE HEIGHT RECTANGLE (GUIDE)
LAYER 5: FULL CANVAS OUTLINE (GUIDE)
LAYER 6: BACKGROUND TEXTURE (ART)
```

Remove (or hide) Layers 1–5 before exporting final production artwork.

---

## 2. Detailed Layer Definitions

### LAYER 1: LABELS
- Contents: Text tags for each guide
  - “Full Canvas — 1500×640”
  - “GitHub Safe Width — 1120 px”
  - “Twitter/X Safe Height — 400 px”
  - “Shared Safe Zone — 1120×400 px”
- Font: Arial, 18 pt, white (#FFFFFF) with 1–2 px black (#000000) stroke
- Placement: Just outside corresponding rectangle edges
- Group name suggestion: `GUIDE/LABELS`
- Export: Hidden

### LAYER 2: SHARED SAFE ZONE RECTANGLE
- Size: 1120 × 400 px
- Position: Centered horizontally & vertically
- Stroke: 3 px Gold (#FFD700), no fill
- Purpose: Absolute boundary for semantic content (crest, title, invocation, motto)
- Group name: `GUIDE/SAFE_SHARED`
- Export: Hidden

### LAYER 3: GITHUB SAFE WIDTH RECTANGLE
- Size: 1120 × 640 px
- Position: X:190, Y:0
- Stroke: 2 px Light Blue (#4DA3FF), no fill
- Purpose: Lateral cropping reference for GitHub preview scaling
- Group name: `GUIDE/SAFE_GITHUB_WIDTH`
- Export: Hidden

### LAYER 4: TWITTER/X SAFE HEIGHT RECTANGLE
- Size: 1500 × 400 px
- Position: X:0, Y:120
- Stroke: 2 px Light Green (#4DFF88), no fill
- Purpose: Vertical cropping reference for Twitter/X
- Group name: `GUIDE/SAFE_TWITTER_HEIGHT`
- Export: Hidden

### LAYER 5: FULL CANVAS OUTLINE
- Size: 1500 × 640 px (artboard boundary)
- Stroke: 2 px Light Grey (#CCCCCC), no fill
- Purpose: Structural reference; outermost composition frame
- Group name: `GUIDE/CANVAS`
- Export: Hidden

### LAYER 6: BACKGROUND TEXTURE
- Base tone: #F8F1E1
- Vignette: Radial gradient (edges → #E6D8B5 @ ~35% opacity; Multiply or Soft Light)
- Optional motifs:
  - Faint laurel curls (Gold #D4AF37 @ 8–10% opacity)
  - Concentric crest sigil rings (Overlay @ 12–18%)
- Texture: Subtle organic paper noise (4–6% opacity overlay)
- Group name: `ART/BACKGROUND`

(Additional CREST + TITLE + INVOCATION + MOTTO layers are defined in `dual-purpose-banner-template.md`.)

---

## 3. Naming Convention (Suggested)

| Category | Prefix | Example |
|----------|--------|---------|
| Guide sets | GUIDE/ | GUIDE/SAFE_SHARED |
| Text (semantic) | TXT/ | TXT/INVOCATION |
| Crest & emblem | CREST/ | CREST/PRIMARY |
| Effects overlays | FX/ | FX/GLOW_CREST |
| Background art | ART/ | ART/BACKGROUND |
| Archive / disabled | Z_/ | Z_/OLD_MOTTO |

---

## 4. Visibility States (Before Export)

| Layer Group | Working | Export Final |
|-------------|---------|--------------|
| GUIDE/*     | Visible | Hidden |
| ART/*       | Visible | Visible |
| CREST/*     | Visible | Visible |
| TXT/*       | Visible | Visible |
| FX/*        | Visible (validate) | Visible |
| Z_/*        | Hidden | Hidden |

Checklist:
- [ ] All GUIDE groups hidden
- [ ] No partial opacity on semantic text
- [ ] Crest centered; safe zone respected
- [ ] Gold gradient consistent (#F8E7A8 → #D4AF37 → #8F7530)
- [ ] Invocation violet contrast ≥ 4.5:1 (darken to #3D266E if needed)

---

## 5. Quick Ops Script Tag (Embed Comment In Source)
```
KYPRIA_LAYER_ARCH:
  version: 2025.09.09
  spec_ref:
    - dual-purpose-banner-template.md
    - dual-purpose-banner-safe-zone-overlay.md
  audit: pending
```

---

## 6. Integration Note
The overlay (`dual-purpose-banner-safe-zone-overlay.md`) remains a neutral transparency guide asset. This document governs the master layered file logic—use both together to ensure consistent reproduction.

© Kypria LLC — Stewardship in Perpetuity.