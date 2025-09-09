# Appendix E — Accessibility & Contrast Audit  
Kypria Visual Identity Canon  
Version: 0.1.2  

## Purpose  
To ensure all Kypria visual assets meet or exceed WCAG 2.1 AA contrast requirements, preserving legibility and ceremonial integrity across all mediums.

## Contrast Ratio Targets  
| Element Pair                              | Min Ratio (AA) | Min Ratio (AAA) | Pass/Fail Notes            |
|-------------------------------------------|----------------|-----------------|----------------------------|
| Gold (#D4AF37) on Parchment (#F8F1E1)     | 3.0:1          | 4.5:1           | Pass AA large text only    |
| Deep Violet (#4B2E83) on Parchment        | 7.0:1          | 7.0:1           | Pass AAA                   |
| Dark Brown (#3B2F2F) on Parchment         | 12.0:1         | 12.0:1          | Pass AAA                   |
| Gold (#D4AF37) on Deep Violet (#4B2E83)   | 4.6:1          | 7.0:1           | Pass AA                    |

## Minimum Text Sizes  
- Body text: 16 px / 12 pt minimum.  
- Small caps / decorative headings: 18 px / 13.5 pt minimum.  
- Gold on parchment: 20 px / 15 pt minimum for AA compliance.

## Tooling Recommendations  
- Stark (Figma/Sketch/Adobe XD): https://www.getstark.co/  
- axe DevTools: https://www.deque.com/axe/  
- WebAIM Contrast Checker: https://webaim.org/resources/contrastchecker/

## Crest Watermark Scaling  
- Minimum crest height: 200 px for watermark use.  
- Opacity: 8–12% to avoid overpowering text.  
- Maintain emboss effect for tactile perception.

---

Enforcement note: Any new palette, token, or asset PR must cite this appendix and document contrast evidence for body, large text, and interactive states.
