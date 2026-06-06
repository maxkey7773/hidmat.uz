---
name: Premium Silk Road Modernism
colors:
  surface: '#f8f9ff'
  surface-dim: '#cbdbf5'
  surface-bright: '#f8f9ff'
  surface-container-lowest: '#ffffff'
  surface-container-low: '#eff4ff'
  surface-container: '#e5eeff'
  surface-container-high: '#dce9ff'
  surface-container-highest: '#d3e4fe'
  on-surface: '#0b1c30'
  on-surface-variant: '#45464d'
  inverse-surface: '#213145'
  inverse-on-surface: '#eaf1ff'
  outline: '#76777d'
  outline-variant: '#c6c6cd'
  surface-tint: '#565e74'
  primary: '#000000'
  on-primary: '#ffffff'
  primary-container: '#131b2e'
  on-primary-container: '#7c839b'
  inverse-primary: '#bec6e0'
  secondary: '#7c580f'
  on-secondary: '#ffffff'
  secondary-container: '#ffcc7a'
  on-secondary-container: '#79550b'
  tertiary: '#000000'
  on-tertiary: '#ffffff'
  tertiary-container: '#111c2d'
  on-tertiary-container: '#79849a'
  error: '#ba1a1a'
  on-error: '#ffffff'
  error-container: '#ffdad6'
  on-error-container: '#93000a'
  primary-fixed: '#dae2fd'
  primary-fixed-dim: '#bec6e0'
  on-primary-fixed: '#131b2e'
  on-primary-fixed-variant: '#3f465c'
  secondary-fixed: '#ffdeac'
  secondary-fixed-dim: '#f0bf6e'
  on-secondary-fixed: '#281900'
  on-secondary-fixed-variant: '#604100'
  tertiary-fixed: '#d8e3fb'
  tertiary-fixed-dim: '#bcc7de'
  on-tertiary-fixed: '#111c2d'
  on-tertiary-fixed-variant: '#3c475a'
  background: '#f8f9ff'
  on-background: '#0b1c30'
  surface-variant: '#d3e4fe'
  success-emerald: '#064E3B'
  surface-ivory: '#FCFBF7'
  accent-gold-light: '#F5E6C8'
  border-subtle: '#E2E8F0'
typography:
  display-lg:
    fontFamily: manrope
    fontSize: 48px
    fontWeight: '700'
    lineHeight: 56px
    letterSpacing: -0.02em
  display-lg-mobile:
    fontFamily: manrope
    fontSize: 32px
    fontWeight: '700'
    lineHeight: 40px
    letterSpacing: -0.01em
  headline-md:
    fontFamily: manrope
    fontSize: 32px
    fontWeight: '600'
    lineHeight: 40px
  headline-sm:
    fontFamily: manrope
    fontSize: 24px
    fontWeight: '600'
    lineHeight: 32px
  body-lg:
    fontFamily: inter
    fontSize: 18px
    fontWeight: '400'
    lineHeight: 28px
  body-md:
    fontFamily: inter
    fontSize: 16px
    fontWeight: '400'
    lineHeight: 24px
  label-md:
    fontFamily: ibmPlexSans
    fontSize: 14px
    fontWeight: '500'
    lineHeight: 20px
    letterSpacing: 0.01em
  label-sm:
    fontFamily: ibmPlexSans
    fontSize: 12px
    fontWeight: '600'
    lineHeight: 16px
    letterSpacing: 0.05em
rounded:
  sm: 0.125rem
  DEFAULT: 0.25rem
  md: 0.375rem
  lg: 0.5rem
  xl: 0.75rem
  full: 9999px
spacing:
  unit: 4px
  gutter: 24px
  margin-mobile: 16px
  margin-desktop: 48px
  container-max: 1200px
---

## Brand & Style

The design system embodies a "Premium Silk Road Modernism"—a style that balances the heritage of Central Asian hospitality with the precision of global finance. The brand personality is authoritative, sophisticated, and trustworthy, aimed at a discerning audience in Uzbekistan and the wider region. 

The aesthetic follows a **Minimalist** approach with **Corporate Modern** undertones. It prioritizes vast white space, rigorous typographic hierarchy, and a refined color application that feels expensive yet understated. Every interaction is designed to feel intentional and high-quality, moving away from "app-like" playfulness toward a "concierge-like" digital experience.

## Colors

The palette is anchored by **Midnight Blue**, a deep, professional hue that communicates institutional stability and prestige. This is contrasted with **Refined Gold**, used sparingly for high-end service indicators, verified statuses, and premium calls to action.

- **Primary (Midnight Blue):** Used for core branding, primary buttons, and heavy headings.
- **Secondary (Gold):** Reserved for "Gold-tier" services, ratings, and significant highlights.
- **Surface Strategy:** The system uses a clean white background, but utilizes a "Surface Ivory" for sectioning to soften the digital glare and add a touch of luxury. 
- **Functional Colors:** Success states move from a bright emerald to a deeper, more sophisticated forest green to maintain the high-contrast, premium feel.

## Typography

This design system employs a multi-font strategy to differentiate editorial content from functional data. 

- **Manrope** is used for headlines to provide a modern, refined, and balanced geometric feel. 
- **Inter** handles the primary body copy, ensuring maximum legibility and support for diverse character sets across Central Asia.
- **IBM Plex Sans** is used for labels and technical data, providing a structured, systematic feel for prices, dates, and metadata.

Letter spacing is slightly tightened on large displays for a premium "locked-in" look and slightly widened on small labels to ensure clarity.

## Layout & Spacing

The layout philosophy is built on a **Fixed Grid** with generous inner gutters. This creates a sense of "breathable luxury."

- **Grid:** A 12-column grid for desktop with 24px gutters. 
- **Rhythm:** All spacing (padding/margins) must be multiples of the 4px base unit. 
- **Negative Space:** Use double the standard padding for section headers to emphasize the minimalist aesthetic.
- **Mobile:** Transition to a 4-column fluid grid with 16px margins, ensuring content remains centered and legible.

## Elevation & Depth

To maintain a sophisticated and modern feel, this design system avoids heavy, muddy shadows. Instead, it utilizes **Tonal Layers** and **Low-Contrast Outlines**.

- **Depth:** Elevation is communicated through subtle color shifts (e.g., a card using White against a Surface Ivory background) or extremely diffused, low-opacity shadows (Blur 20px, Opacity 4%, Color: Primary).
- **Outlines:** Use 1px borders in `border-subtle` (#E2E8F0) for input fields and secondary cards.
- **Active State:** Elements that are interacted with do not "rise" via shadows but instead may shift in background tone or gain a refined Gold border.

## Shapes

The shape language is **Soft (0.25rem base)**. 

While the previous iteration used a more casual 12px radius, this premium system moves toward a more "tailored" look. Small radii on buttons and cards (4px to 8px) suggest precision and architectural strength. 

- **Standard Elements:** 4px radius (Soft).
- **Cards/Modals:** 8px radius (rounded-lg).
- **Search Bars:** Should remain Soft (4px) or Sharp (0px) to maintain a professional, high-end tool aesthetic, rather than a pill-shaped social aesthetic.

## Components

- **Buttons:** Primary buttons use the Midnight Blue background with White text. Secondary buttons use a transparent background with a Midnight Blue border. The "Premium" button variant uses a Gold background with Midnight Blue text.
- **Input Fields:** Minimalist design with a bottom border or subtle 1px frame. Focus states are indicated by a 1px Midnight Blue border—never a glow.
- **Chips/Badges:** Small, all-caps labels using IBM Plex Sans. Verified badges use the Gold accent.
- **Cards:** White surfaces with 1px `border-subtle`. Content should have generous 24px internal padding.
- **Navigation:** Top-tier navigation should be clean with high-contrast text and no background fill, using the Gold accent for the active state indicator (usually a small 2px underline).
- **Service Indicators:** Use the Refined Gold for high-value features, VIP support status, or premium marketplace listings to instantly signal quality to the user.