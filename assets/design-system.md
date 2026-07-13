# Design System & Folder Conventions

This document serves as the single source of truth for the Sarthak Srivastava GitHub Profile Redesign.

## Folder Conventions
- `assets/` - Root directory for all media
  - `assets/svg/` - All handcrafted SVG components
  - `assets/svg/defs/` - Reusable SVG definition templates
  - `assets/scripts/` - Any generation scripts (if needed)

## 1. Color Palette (Dark Mode Premium)
- **Backgrounds**
  - Base: `#000000`
  - Subdued: `#0A0A0A`
  - Card/Surface: `#111111`
  - Glass: `rgba(255, 255, 255, 0.03)` to `rgba(255, 255, 255, 0.08)`
  - Border (Subtle): `rgba(255, 255, 255, 0.1)`
- **Typography**
  - Primary: `#EDEDED`
  - Secondary: `#A1A1AA`
  - Muted: `#71717A`
- **Accents (Liquid Gradients)**
  - Cyan: `#23C4FF`
  - Deep Blue: `#1A4DFF`
  - Soft Purple: `#7928CA`

## 2. Spacing Scale (8px Grid)
- `4px` (xxs)
- `8px` (xs)
- `12px` (sm)
- `16px` (md)
- `24px` (lg)
- `32px` (xl)
- `48px` (xxl)
- `64px` (xxxl)

## 3. Typography Scale
- **Font-Family**: System UI, -apple-system, BlinkMacSystemFont, "Segoe UI", Roboto, sans-serif
  - *Note: GitHub SVG proxy blocks external fonts like Inter without base64 embedding, so we rely on pristine system stacks or embed if absolutely necessary.*
- `12px` - Metadata, tags
- `14px` - Secondary text, standard body
- `16px` - Primary body, subtitles
- `20px` - Card headers, section titles
- `24px` - Major section headers
- `32px` - Hero subtitle
- `48px` - Hero title

## 4. Visual Effects
- **Border Radius**: 
  - Cards: `12px`
  - Inner Elements / Buttons: `8px`
  - Pills: `99px`
- **Glow Values (feGaussianBlur)**:
  - Soft: `stdDeviation="4"`
  - Medium: `stdDeviation="12"`
  - Ambient: `stdDeviation="32"`
- **Glassmorphism Blur**:
  - Backdrop Blur: `stdDeviation="16"` (implemented via `feGaussianBlur` on a copied background patch)
- **Shadows (feDropShadow)**:
  - Floating Card: `dx="0" dy="8" stdDeviation="24" flood-opacity="0.4"`
  - Inner Glow: (Simulated via 1px border stroke with linear gradient)

## 5. Animation Rules
- **Durations**:
  - Breathing/Floating: `8s` - `12s`
  - Background Mesh: `20s`
  - Hover/Micro (CSS if applicable): `0.3s`
- **Easing Curves**:
  - `keySplines="0.25 0.1 0.25 1.0"` (Smooth Ease-in-out)
  - `calcMode="spline"`

## SVG Workflow Rule
Always copy `<defs>` from `assets/svg/defs/template.svg` into any new SVG to ensure consistent gradients, filters, and animations.
