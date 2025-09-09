# Kypria Visual Identity — Designer README

© Kypria LLC — Stewardship in Perpetuity.  
Status: Draft (pending ratification)  
Document Class: Canonical Design Operations Reference  
Version: 0.1.0 (proposed)  

---

## 0. Purpose & Stewardship Principle

This document establishes the authoritative rules and reusable primitives for creating, extending, and auditing Kypria visual assets (GitHub profile materials, social banners, documentation visuals, ceremonial graphics, and future product surfaces).  
All contributors act as stewards: every change should preserve semantic clarity, symbolic coherence, and long‑horizon maintainability.

---

## 1. Core Identity Elements

### 1.1 Crest (Primary Mark)
- Form: (Describe: e.g., circular seal / shield / layered emblem) — INSERT canonical description here.
- Protected Space: Maintain a minimum clear space equal to 1× crest diameter (or height) around the mark where no other semantic element intrudes.
- Minimum Display Size:
  - Raster: Not below 128 px width in standard contexts.
  - Vector: Scale freely; respect stroke proportions.
- Do NOT:
  - Distort proportions
  - Add drop shadows (unless in a sanctioned stylistic set)
  - Recolor arbitrarily
  - Place over low‑contrast backgrounds without an approved contrast plate/backer.

### 1.2 Secondary & Micro Marks
If micro or monochrome variants exist, enumerate them here:
- Monochrome Crest: 1‑color silhouette (Gold on dark, Deep Neutral on light)
- Outline Variant: Only for emboss / engraving simulation contexts.

(If these variants do not yet exist, mark as “Reserved / Not Yet Issued”.)

### 1.3 Motto / Invocation Lockups
- The motto and/or invocation must never reduce crest safe spacing.
- Use predefined lockup templates (to be added in /design/lockups).

---

## 2. Color System

Color tokens are defined in semantic layers. Replace any TBD hex with ratified values once finalized. Keep a central JSON/YAML design token file (future addition) for programmatic reuse.

| Token | Role | Hex (Proposed) | Notes |
|-------|------|----------------|-------|
| color.brand.gold.primary | Core accent / symbolic wealth / highlight | `#FFD700` | Canonical “Kypria Gold” (already used in safe zones) |
| color.brand.gold.deep | Depth variant (shadows / gradients) | `#C9A200` | Suggested; confirm |
| color.brand.parchment.light | Base background / texture base | `#F4E9D2` (TBD) | Soft parchment |
| color.brand.parchment.deep | Contrast panel / layered card | `#E2D2B4` (TBD) | Used for tonal layering |
| color.text.primary | Default heading & body on light | `#1F1A12` | High readability |
| color.text.inverse | Text on dark plates | `#FFFFFF` | |
| color.line.hairline | Subtle dividers | `#D2C6AF` (TBD) | |
| color.state.info | Informational highlight | `#4DA3FF` | Borrowed from guide blue (dual usage acknowledged) |
| color.state.success | Emergent / affirmation | `#4DFF88` | Matches safe-height green (reassess if divergence needed) |
| color.state.warning | Reserved | `#FFB347` (TBD) | |
| color.state.alert | Reserved | `#D94A3D` (TBD) | |
| color.utility.neutral.mid | Neutral stroke / frame | `#CCCCCC` | Already used in Full Canvas frame |
| color.utility.safezone.gold | Shared safe zone highlight | `#FFD700` | Alias of brand gold |

Guidelines:
- Gold must not be flattened into gradients without preserving a true-color anchor.
- Parchment textures must average to WCAG contrast ratios ≥ 4.5:1 with primary text.
- Limit simultaneous use of both info (blue) and success (green) unless semantically justified.

---

## 3. Typography

| Token | Family | Fallback Stack | Use Case |
|-------|--------|----------------|----------|
| font.display | (e.g., Cinzel / Trajan / EB Garamond) | Serif fallback stack | Ceremonial headings, crest-adjacent titles |
| font.body | (e.g., Source Serif / Georgia) | `Georgia, Times, serif` | Long-form documentation |
| font.interface | (e.g., Inter / Source Sans) | `-apple-system, BlinkMacSystemFont, Segoe UI, Roboto, sans-serif` | UI overlays, controls |
| font.monospace | (e.g., JetBrains Mono) | `ui-monospace, SFMono-Regular, Menlo, monospace` | Code or technical blocks |

Typographic Rules:
- Heading Scale (suggested): 1.00, 1.25, 1.56, 1.95, 2.44 (≈ Major Third). Confirm or adjust to modular scale preference.
- Line Length: 60–75 characters for body.
- Avoid artificial letter‑spacing on body text; small caps allowed for ritual/ceremonial headings only.
- Never stretch or compress letterforms.

---

## 4. Layout & Spatial System

### 4.1 Global Canvas Archetypes
| Context | Ratio / Size | Notes |
|---------|--------------|-------|
| Dual‑Purpose Banner | 1500 × 640 | See Section 5 reference |
| Social Avatar / Seal | 1024 × 1024 | Central crest + radial balance |
| Documentation Panel | 1200 × 800 (flex) | Safe interior margin 64 px |
| Narrow Card | 800 × 600 | Maintain 56 px internal padding |

### 4.2 Spacing Tokens (proposed)
| Token | px | Use |
|-------|----|-----|
| space.xs | 8 | Tight grouping |
| space.sm | 16 | Standard inter-element |
| space.md | 24 | Section separation |
| space.lg | 40 | Major grouping |
| space.xl | 64 | Edge padding / macro rhythm |

Maintain consistent rhythm. Avoid arbitrary 1–5 px nudges unless for optical alignment.

---

## 5. Dual‑Purpose Banner System (Cross‑Reference)

Primary Spec: profile/dual-purpose-banner-safe-zone-overlay.md (Sections 1–13)  
Legend Duplicate: profile/safe-zone-color-legend.md  

Critical Rule: All semantic elements (crest, title, invocation, motto) must reside fully within the Shared Safe Zone (1120×400 px gold).  
Decorative parchment, gradients, faint laurels, or symbolic filigree may extend beyond but must not provide essential meaning or text.

---

## 6. Imagery & Texture

Parchment Layer:
- Source: High-resolution subtle fiber texture (≥ 300 DPI in master).
- Treatment: Desaturate slightly; overlay color blend with a warm neutral (#E9DABF median).
- Do not create strong directional lighting conflicting with crest shadows.

Gold Treatment:
- Allowed: Flat, subtle gradient (top: #FFE680, mid anchor #FFD700, shadow #C9A200).
- Avoid: Excessive bevel / lens flare / metallic noise unless in special ceremonial variant.

Laurel / Filigree Motifs:
- Opacity guideline: 8–18% overlay or multiply for background frames.
- Do not interfere with safe zone label clarity during construction.

---

## 7. Iconography

If icon set not yet formalized:
- Reserve a 2 px stroke or 1.5 px optical stroke grid.
- Corner Radii: Softened geometry optional (2–3 px rounding) for unity with crest curvature.

Add library index here once icons exist.

---

## 8. Accessibility & Contrast

Minimum contrast:  
- Text vs background ≥ 4.5:1 (body) / 3:1 (large headings ≥ 24 px regular or 18 px bold).  
Do not rely solely on gold (#FFD700) for text on light parchment—apply an outline or use darker neutral.

---

## 9. File Naming & Versioning

Naming Pattern:
```
kypria-{asset-family}-{descriptor}-vYYYY.MM.DD[-variant].(png|svg|psd|fig|pdf)
```
Examples:
- `kypria-banner-parchment-gold-v2025.09.10.png`
- `kypria-crest-monochrome-v2025.09.10.svg`

Source of Truth:
- Vector: Prefer SVG (text converted to outlines only at publish stage).
- Raster: PNG for transparency, JPEG only for photographic composites.

---

## 10. Export Guidelines

| Asset Type | Format | Color Profile | Notes |
|------------|--------|---------------|-------|
| Crest (Flat) | SVG + PNG | sRGB | Keep vector master |
| Banner | PNG | sRGB | Transparent overlays separate |
| Documentation Figures | PNG or SVG | sRGB | Avoid heavy compression artifacts |
| Texture Sheets | PNG | sRGB | Maintain original fidelity |

Do not embed unoptimized large photographic backdrops unless required.

---

## 11. Governance & Change Control

All modifications to:
- Crest geometry
- Core color tokens (brand.gold.primary, parchment base)
- Typography families
… must undergo a “Design Steward Audit”.

Add CHANGELOG entry (future: design/CHANGELOG.md) with:
```
DATE:
  change: summary
  rationale: why
  impact: backward-compat / none
  steward: handle
```

---

## 12. Restricted / Prohibited Usage

| Misuse | Status | Reason |
|--------|--------|--------|
| Random gradient overlays on crest | Prohibited | Dilutes symbolic clarity |
| Outline-only crest for primary contexts | Restricted | Weakens presence |
| Unapproved gold hex substitutions | Prohibited | Undermines brand continuity |
| Drop shadow behind safe-zone overlays | Prohibited | Reduces precision |
| Warping crest to fit non-proportional frames | Prohibited | Violates geometry |

---

## 13. Design Tokens (Future Externalization)

A future `design/tokens.*` file (YAML or JSON) will canonicalize:
- Colors
- Spacing scale
- Typography scale
- Safe-zone geometry
- Shadow / elevation presets (if adopted)

Example (proposed YAML skeleton):
```yaml
tokens:
  color:
    brand:
      gold:
        primary: "#FFD700"
        deep: "#C9A200"
    parchment:
      light: "#F4E9D2"
      deep: "#E2D2B4"
  spacing:
    xs: 8
    sm: 16
    md: 24
    lg: 40
    xl: 64
  safezone:
    banner:
      full:
        width: 1500
        height: 640
      shared:
        width: 1120
        height: 400
```

---

## 14. Implementation Notes (Engineering Crossover)

When embedding graphics in documentation:
- Prefer `<picture>` with SVG fallback to PNG.
- Provide descriptive alt text: “Kypria crest — circular seal with …”
- Avoid base64 inlined raster assets for large textures.

---

## 15. Metadata Block

Embed (commented) at top of major source files:

```
KYPRIA_DESIGN_README:
  version: 0.1.0
  status: draft
  steward: Kypria LLC Stewardship
  next_audit: pending
```

---

## 16. Open Items / To Ratify

| Item | Status | Owner | Notes |
|------|--------|-------|-------|
| Final crest geometry spec sheet | Pending | Design Steward | Add vector layering doc |
| Confirm parchment exact palette | Pending | Design Steward | Sample from texture |
| Select production display font | Pending | Design + Brand | Evaluate licensing |
| Approve icon stroke system | Pending | Design | |
| Publish token file | Pending | Design + Eng | |

---

## 17. Audit Checklist

- [ ] Crest spacing preserved
- [ ] Colors from authorized palette only
- [ ] Typography matches assigned context
- [ ] Safe zones respected (where applicable)
- [ ] File naming pattern followed
- [ ] Version metadata embedded
- [ ] Contrast requirements met
- [ ] No disallowed visual effects

---

## 18. Appendices (Future)

- A: Crest Construction Grid
- B: Parchment Texture Licensing & Source
- C: Gold Finish Light Study
- D: Lockup Templates Index

---

End of Document  
© Kypria LLC — Stewardship in Perpetuity.
