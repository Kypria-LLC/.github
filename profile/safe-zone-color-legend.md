# Kypria Dual‑Purpose Banner — Safe‑Zone Color Legend

Canonical color + stroke definitions for the guide rectangles used across the dual‑purpose (GitHub + Twitter/X) banner system.  
Primary references:  
- `dual-purpose-banner-safe-zone-overlay.md`  
- `banner-layer-architecture.md`

---

## 1. Legend Table

| Guide Layer | Purpose | Stroke Color | Hex | Stroke Width |
|-------------|---------|--------------|-----|--------------|
| Full Canvas Outline | Defines total working area (1500×640 px) | Light Grey | `#CCCCCC` | 2 px |
| GitHub Safe Width | GitHub preview width (1120 px); anything outside may crop | Light Blue | `#4DA3FF` | 2 px |
| Twitter/X Safe Height | Twitter/X banner height (400 px); top/bottom outside may crop | Light Green | `#4DFF88` | 2 px |
| Shared Safe Zone | Overlap (1120×400 px); all critical elements must stay inside | Gold | `#FFD700` | 3 px |

---

## 2. Usage Guidance
- Opacity: 100% stroke opacity; no fills.
- Z‑Order: Gold Shared Safe Zone above other guide rectangles.
- Layer Locking: Lock all guide layers post-alignment to prevent accidental movement.
- Export Contexts:
  - Overlay PNG: Leave only strokes; hide labels if producing a minimalist variant.
  - Master Banner: All guide layers hidden prior to final export.
- Fidelity: Do not substitute colors; these pairings are part of reproducible spec identity.

---

## 3. Quick Integrity Checklist
- [ ] Stroke widths match legend (3 px only on shared safe zone).
- [ ] No fills applied.
- [ ] Colors exact (verify hex, avoid color-managed shifts).
- [ ] Guide geometry unchanged (1120×400 safe zone centered).
- [ ] Shared safe zone not obscured by art layers during design.

---

## 4. Metadata Block
```
KYPRIA_SAFEZONE_LEGEND:
  version: 2025.09.09
  refs:
    - dual-purpose-banner-safe-zone-overlay.md
    - banner-layer-architecture.md
  status: canonical
```

© Kypria LLC — Stewardship in Perpetuity.