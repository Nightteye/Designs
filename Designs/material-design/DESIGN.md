# Design System Strategy: The Architectural Gallery

## 1. Overview & Creative North Star
This design system moves beyond the rigid, utilitarian nature of standard Material Design 3 and adopts a "Creative North Star" we call **The Architectural Gallery**. 

The goal is to treat digital real estate like a high-end physical space—think of a modern museum or a premium boutique. We achieve this by moving away from "boxes on a screen" and toward a sense of **tonal depth**. By utilizing Material 3’s color tokens to create subtle shifts in environment rather than using heavy borders, we create an experience that feels instructional yet sophisticated. We prioritize breathable layouts, intentional asymmetry in content placement, and an editorial approach to information hierarchy.

---

## 2. Colors & Surface Logic
The palette is rooted in the sophisticated `primary` (#46608a) and `surface` (#f9f9fe) tones. To achieve a premium feel, we follow a strict logic of environmental transitions.

- **The "No-Line" Rule:** Prohibit the use of 1px solid borders for sectioning or containment. Boundaries must be defined through background color shifts. For instance, a Hero section using `surface` transitions into a feature section using `surface-container-low`.
- **Surface Hierarchy & Nesting:** Use surface tiers to imply physical layers. 
    - **Base Layer:** `surface` (#f9f9fe)
    - **Secondary Content Areas:** `surface-container-low` (#f3f3fa)
    - **Interactive Elements/Cards:** `surface-container-lowest` (#ffffff) to create a "lifted" appearance without shadows.
- **The "Glass & Gradient" Rule:** For the Hero page, use a subtle linear gradient on the primary CTA: `primary` (#46608a) to `primary-dim` (#3a537d). This provides a "soul" to the button that flat colors lack. Use `surface_variant` with a 60% opacity and 20px backdrop-blur for floating navigation bars to create a "frosted glass" effect.

---

## 3. Typography: The Editorial Voice
While we utilize the `Inter` family for its mathematical precision, our scale is leveraged to create an editorial, high-quality hierarchy.

- **Display (LG/MD):** Used exclusively for Hero headlines. Set with tight letter-spacing (-0.02em) to give a custom, "printed" feel.
- **Headline (SM/MD):** These act as the "anchors" for your sections. Use `on_surface` (#2f323a) for maximum authority.
- **Body (LG):** This is your primary instructional tool. It should feel airy. Increase line-height to 1.6 for long-form descriptions to ensure a professional, readable flow.
- **Label (MD/SM):** Use `on_surface_variant` (#5c5f68) in all-caps with increased letter-spacing (+0.05em) for small category tags above headlines.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are largely discarded in favor of **Tonal Layering**. We communicate "upward" movement through color luminosity.

- **The Layering Principle:** To highlight a card, do not add a shadow. Instead, place a `surface-container-lowest` card on a `surface-container` background. The slight shift from #ecedf6 to #ffffff creates a cleaner, more modern "lift."
- **Ambient Shadows:** Only use shadows for "floating" elements like Modals or Floating Action Buttons. Shadows must use the `on_surface` color at 6% opacity with a 32px blur—mimicking soft, natural sunlight rather than a digital glow.
- **The "Ghost Border" Fallback:** If accessibility requires a border, use `outline_variant` at 15% opacity. This provides a "suggestion" of a boundary without cluttering the visual field.

---

## 5. Components

### Buttons
- **Primary:** Gradient fill (`primary` to `primary_dim`), `on_primary` text, `xl` (1.5rem) rounding.
- **Secondary:** `secondary_container` fill with `on_secondary_container` text. No border.
- **Tertiary:** No fill. `primary` text. Use for low-priority actions like "Cancel" or "Learn More."

### Input Fields
- **Styling:** Use `surface_container_highest` for the field background with a `none` border.
- **States:** On focus, transition the background to `surface_container_lowest` and add a 2px "Ghost Border" using the `primary` token.

### Cards & Sections
- **Construction:** Absolutely no dividers. Separate content using the **Spacing Scale** (e.g., 64px vertical gaps between sections). 
- **Hero Card:** For high-impact areas, use `primary_container` with `on_primary_container` text to create a high-contrast instructional block.

### Signature Component: The "Instructional Inset"
A specialized container for this system: Use `tertiary_container` with `md` rounding and a subtle `tertiary` left-hand accent bar (4px wide). Use this for "Pro-tips" or "Key Insights" to break the vertical rhythm of the hero page.

---

## 6. Do’s and Don’ts

### Do:
- **Embrace White Space:** If a section feels crowded, double the padding. This system thrives on "breathing room."
- **Use Nested Surfaces:** Place `surface_container_low` elements inside `surface` sections to guide the eye.
- **Asymmetric Layouts:** Shift your Hero text to the left and your imagery slightly off-center to the right to break the "template" feel.

### Don't:
- **Don't use 1px black/grey borders.** This instantly makes a high-end system look "cheap" and "standard."
- **Don't use standard shadows.** Avoid the default "Drop Shadow" presets in your design tool; always hand-craft soft, tinted ambient blurs.
- **Don't use dividers.** If you need to separate two pieces of content, use a background color shift or 48px of empty space.