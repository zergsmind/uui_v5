# UII v1 Blueprint
> Reference summary extracted from `projects/UI_website` (v1 complete design)
> Call elements by their label in brackets, e.g. [COLORS], [HERO], [TEAM]

---

## [IDENTITY]
- **Project**: Urban Innovation Institute (UII)
- **Type**: Independent foundation registered in Romania
- **Mission**: Systemic integration infrastructure for urban innovation — connecting public administration, private sector, academia, civil society, and communities
- **Doctrine**: "We don't compete with consultancies, NGOs, or public administration. We compete with the absence of an integration mechanism. And in that space, we have no competition."

---

## [COLORS]
60/30/10 system — Green palette

| Role | Variable | Hex | Usage |
|------|----------|-----|-------|
| Dominant (60%) | `--color-dominant` | `#F5FBF7` | Base backgrounds |
| Secondary (30%) | `--color-secondary` | `#6B8E7F` | Muted sage/forest green |
| Secondary Light | `--color-secondary-light` | `#8BA89F` | Subtle accents |
| Accent (10%) | `--color-accent` | `#E8A66F` | Warm peach/coral highlights |
| Accent Dark | `--color-accent-dark` | `#D9915A` | Hover states |
| Text Dark | `--text-dark` | `#2C3E34` | Headings, body |
| Text Mid | `--text-mid` | `#556B5F` | Secondary text |
| Text Light | `--text-light` | `#8A9B8E` | Captions, labels |

> Note: README mentions Teal `#1B5E5A` / Coral `#D4613A` / Offwhite `#F7F4EF` as the brand identity — the CSS uses a softened green palette variation.

---

## [FONTS]
- **Headings**: Spectral (serif, weights 300–700)
- **Body**: DM Sans (sans-serif, weights 300–600)
- Import: Google Fonts

---

## [STACK]
- React 18 + TypeScript
- Vite 5 (dev server on port 3001)
- Three.js (WebGL 3D animation)

---

## [SECTIONS] — Page layout (5 cards + footer)

| # | ID | Content |
|---|----|---------|
| — | Hero | Title + subtitle + WebGL background |
| 01 | `about` | What We Are + doctrine quote |
| 02 | `services` | How We Work (3-column grid) |
| 03 | `stats` | Track Record (4-stat grid) |
| — | `cta` | CTA buttons |
| — | footer | Address + contact |

---

## [HERO]
- **EN title**: "Where urban systems become action"
- **RO title**: "Unde sistemele urbane devin actiune"
- **NL title**: "Waar stedelijke systemen in actie worden omgezet"
- **Subtitle**: Independent platform for systemic urban innovation connecting public admin, private sector, academia, civil society, communities
- **CTA button**: "Discover Our Work"

---

## [ABOUT] — Section 01
- UII = neutral, competent, operationally independent structure at intersection of all stakeholders
- NOT: think tank / consulting firm / NGO
- IS: transforms conversations and decisions into contracted, funded, and delivered projects

---

## [SERVICES] — Section 02 (3 columns)
1. **Public Administration Consulting** — EU fund applications, New European Bauhaus, smart city strategies, participatory design
2. **EU Consortium & Funding Facilitation** — EUI Call 4, NEB Facility, URBACT IV, Interreg Danube, LIFE Programme (3–5 year commitments)
3. **International Corporate Partnerships** — Market entry for Japanese & European corps in Romania/CEE

---

## [STATS] — Section 03 (Track Record)
| Stat | Label |
|------|-------|
| 100+ | Public space & urban regeneration projects delivered |
| 3 | Decision levels covered: sector, municipality, ministry |
| 10 | Japanese organizations in active pipeline post-Osaka 2025 |
| 2025 | Representation at Smart City Expo Barcelona & Osaka Expo |

---

## [TEAM]
| Name | Role | Background |
|------|------|------------|
| Costin | CEO · Strategy & International Relations | Architect, entrepreneur, PhD UAUIM. Founder DreaModule & Atelier MCA |
| Samih | CSO · Strategy, Development & Innovation | Architect, Technical Director CIPU Sector 6, co-founder Edificator Studio |
| Mihai | CTO · Technical & Public Administration Interface | Urban dev specialist, CEO CIPU Sector 6 (June 2025), PhD UAUIM |

---

## [LANGUAGES]
- **RO** — Romanian (Română)
- **EN** — English
- **NL** — Dutch (Nederlands)
- Persisted via `localStorage`

---

## [WEBGL] — Three.js UrbanScene
- Urban geometric shapes + particle system
- Physics: ADSR-style damping
- `SHAPE_ROTATION_SLOWDOWN = 0.2` (80% slower — architectural feel)
- `PARTICLE_SLOWDOWN = 0.44` (graceful floating)
- `DAMPING = 0.98` (organic deceleration)
- `BOUNCE_ENERGY = 0.9` (energy loss on collision)
- Spans full page as background layer

---

## [COMPONENTS]
| File | Purpose |
|------|---------|
| `App.tsx` | Main layout, section assembly, scroll tracking |
| `UrbanScene.tsx` | Three.js WebGL animation |
| `Header.tsx` | Top navigation bar |
| `LanguageContext.tsx` | i18n state provider |
| `LanguagePicker.tsx` | RO/EN/NL selector |
| `ScrollIndicator.tsx` | Floating scroll progress navigator |
| `SectionDivider.tsx` | Numbered visual section breaks |
| `translations.ts` | All copy in RO/EN/NL |

---

## [CONTACT]
- **Email**: contact@urbaninnovationinstitute.ro
- **Location**: Bucharest, Romania
