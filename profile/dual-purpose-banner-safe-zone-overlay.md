# Kypria Dual‑Purpose Banner Safe‑Zone Overlay — Build Instructions

This overlay file is used as a construction guide when designing the dual‑purpose (GitHub + Twitter/X) banner. It should NEVER be flattened into the final artwork—only placed above it during la...

---

## 1. Canvas

| Property | Value |
| |----------|-------|
| | Dimensions | 1500 × 640 px |
| | Background | Fully transparent |
| | Color Mode | RGB |
| | Resolution (master source) | 300 DPI (export PNG can be 72–96 DPI equivalent) |

---

## 2. Rectangles (Guides)

| Guide Name | Size (W×H) | Position (Top‑Left X,Y) | Stroke | Color | Notes |
| |------------|------------|--------------------------|--------|-------|-------|
| | Full Canvas Border | 1500 × 640 | 0,0 | 2 px | #CCCCCC | Outer frame |
| | GitHub Safe Width | 1120 × 640 | 190,0 | 2 px | #4DA3FF | GitHub crops width only; full height used |
| | Twitter/X Safe Height | 1500 × 400 | 0,120 | 2 px | #4DFF88 | Twitter/X may crop vertical edges on some displays |
| | Shared Safe Zone | 1120 × 400 | 190,120 | 3 px | #FFD700 | Place ALL semantic elements here |

Coordinate math:
- Horizontal side margin for 1120 width: (1500 − 1120)/2 = 190 px (left & right)
- Vertical top/bottom margin for 400 height: (640 − 400)/2 = 120 px

---

## 3. Labels

| Target | Text |
| |--------|------|
| | Full Canvas Border | “Full Canvas — 1500×640” |
| | GitHub Safe Width | “GitHub Safe Width — 1120 px” |
| | Twitter/X Safe Height | “Twitter/X Safe Height — 400 px” |
| | Shared Safe Zone | “Shared Safe Zone — 1120×400 px” |

Style:
- Font: Arial
- Size: 18 pt (≈ 24 px if using pixel units)
- Color: White (#FFFFFF)
- Outline / Stroke: 1–2 px Black (#000000) for legibility
- Placement: Just OUTSIDE and adjacent to each rectangle (do not overlap safe areas)

---

## 4. Layer Order (Top → Bottom)

1. Labels group
2. Guide rectangles group (each on its own sublayer or grouped by function)
3. Transparent base (blank)

Optional: Put each rectangle in a named layer prefix: `GUIDE/…`

---

## 5. Opacity & Visual Hierarchy

| Guide | Recommended Opacity |
| |-------|---------------------|
| | Shared Safe Zone | 100% stroke |
| | Twitter/X Safe Height | 80% stroke |
| | GitHub Safe Width | 70% stroke |
| | Full Canvas Border | 50–60% stroke |

Do NOT add fills—keep interior fully transparent.

---

## 6. Export

| Parameter | Value |
| |-----------|-------|
| | File name | Kypria_SafeZone_Overlay.png |
| | Format | PNG (preserve transparency) |
| | Compression | Lossless |
| | Background | None (alpha fully transparent) |

---

## 7. Canva Instructions (Quick Method)

1. Create new design: Custom size 1500 × 640 px.
2. Add a rectangle shape → Set to 1500 × 640 → Stroke #CCCCCC, 2 px, no fill.
3. Duplicate for GitHub safe width → Resize to 1120 × 640 → Position X:190, Y:0 → Stroke #4DA3FF.
4. Duplicate for Twitter safe height → Resize to 1500 × 400 → Position X:0, Y:120 → Stroke #4DFF88.
5. Duplicate for Shared safe zone → Resize to 1120 × 400 → Position X:190, Y:120 → Stroke #FFD700 (3 px).
6. Add text labels outside each rectangle; apply white text + black outline (Effects → Outline).
7. Download → PNG → Enable “Transparent background.”
8. Archive source as `kypria-safe-zone-overlay-vYYYY.MM.DD.canva` (or export PDF w/ vectors).

---

## 8. Figma / Affinity / Photoshop Coordinates

| Layer Name | X | Y | W | H |
| |------------|---|---|---|---|
| | guide/full-canvas | 0 | 0 | 1500 | 640 |
| | guide/github-width | 190 | 0 | 1120 | 640 |
| | guide/twitter-height | 0 | 120 | 1500 | 400 |
| | guide/shared-safe | 190 | 120 | 1120 | 400 |

Figma stroke alignment: Center.

Photoshop shape mode: Path or Shape Layer (no fill).

---

## 9. Optional SVG (Vector Source)

```svg
<svg xmlns="http://www.w3.org/2000/svg" width="1500" height="640">
  <title>Kypria Dual-Purpose Banner Safe-Zone Overlay</title>
  <rect x="0" y="0" width="1500" height="640" fill="none" stroke="#CCCCCC" stroke-width="2"/>
  <rect x="190" y="0" width="1120" height="640" fill="none" stroke="#4DA3FF" stroke-width="2"/>
  <rect x="0" y="120" width="1500" height="400" fill="none" stroke="#4DFF88" stroke-width="2"/>
  <rect x="190" y="120" width="1120" height="400" fill="none" stroke="#FFD700" stroke-width="3"/>
  <!-- Labels (convert to outlines if embedding in production) -->
  <g font-family="Arial" font-size="24" fill="#FFFFFF" stroke="#000" stroke-width="2" paint-order="stroke">
    <text x="20" y="30">Full Canvas — 1500×640</text>
    <text x="200" y="20">GitHub Safe Width — 1120 px</text>
    <text x="20" y="115">Twitter/X Safe Height — 400 px</text>
    <text x="210" y="115">Shared Safe Zone — 1120×400 px</text>
  </g>
</svg>
```

(Adjust label positions to avoid overlap visually.)

---

## 10. Optional ImageMagick Script

```bash
magick convert -size 1500x640 xc:none \
  -stroke '#CCCCCC' -strokewidth 2 -fill none -draw 'rectangle 1,1 1499,639' \
  -stroke '#4DA3FF' -strokewidth 2 -draw 'rectangle 190,0 1310,640' \
  -stroke '#4DFF88' -strokewidth 2 -draw 'rectangle 0,120 1500,520' \
  -stroke '#FFD700' -strokewidth 3 -draw 'rectangle 190,120 1310,520' \
  Kypria_SafeZone_Overlay.png
```

(Labels not included; add later in a design tool.)

---

## 11. Validation Checklist

- [ ] Canvas 1500×640 transparent
- [ ] All four guide rectangles present & correctly positioned
- [ ] Shared safe zone stroke thicker (3 px gold)
- [ ] Labels legible with outline
- [ ] No fills accidentally applied
- [ ] Export includes alpha channel
- [ ] Source file versioned (date stamp)

---

## 12. Version Block (Embed in Source Comment)

```
KYPRIA_SAFEZONE_OVERLAY_SPEC:
  version: 2025.09.09
  spec_author: Kypria LLC Stewardship
  last_audit: pending
  purpose: dual-purpose banner construction guide
```

---

## 13. Safe‑Zone Color Legend

| Guide Layer | Purpose | Stroke Color | Hex Code | Stroke Width |
|-------------|---------|--------------|----------|--------------|
| Full Canvas Outline | Defines total working area (1500×640 px) | Light Grey | `#CCCCCC` | 2 px |
| GitHub Safe Width | GitHub preview width (1120 px); outside may crop | Light Blue | `#4DA3FF` | 2 px |
| Twitter/X Safe Height | Twitter/X banner height (400 px); top/bottom outside may crop | Light Green | `#4DFF88` | 2 px |
| Shared Safe Zone | Overlap (1120×400 px); all critical elements must be inside | Gold | `#FFD700` | 3 px |

### Usage Tips
- Opacity: Keep strokes at 100% while designing (no fills).
- Layer Order: Place Shared Safe Zone (gold) above other guides so it remains visible.
- Lock Guides: Lock all guide layers once positioned to prevent drift.
- Transparency: Overlay export must retain full alpha (no background).
- Consistency: Colors and stroke widths are canonical—do not modify.
- Minimal Variant: A labels‑free overlay variant may omit Section 3 labels for distraction‑free composition.

---

© Kypria LLC — Stewardship in Perpetuity.