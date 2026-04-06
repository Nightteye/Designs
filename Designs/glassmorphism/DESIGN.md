# Design System Document: The Ethereal Lens

## 1. Overview & Creative North Star
**Creative North Star: "The Digital Prism"**

This design system moves beyond the static web to create an immersive, multi-dimensional experience. The goal is to simulate a high-end physical environment where interface elements are not "drawn" on a screen, but rather "suspended" in a deep, atmospheric space. By utilizing glassmorphism, we lean into the physics of light—refraction, diffusion, and soft luminance.

To break the "template" look, we abandon rigid, boxy layouts in favor of **Intentional Asymmetry**. Overlapping elements are encouraged; a hero image might bleed behind a semi-transparent glass card, or a secondary headline might be positioned with wide tracking to anchor a corner, creating an editorial, "curated" feel that demands attention through sophistication rather than noise.

---

## 2. Colors & Surface Logic

### The Palette
We utilize a deep, nocturnal foundation (`surface: #060e20`) to allow our vibrant secondary (`#00e3fd`) and tertiary (`#ff6c95`) accents to pop with neon-like intensity.

*   **Primary (`#e4d7fd`)**: A soft lavender used for high-importance text and soft glows.
*   **Secondary (`#00e3fd`)**: A piercing cyan for interactive highlights.
*   **Tertiary (`#ff6c95`)**: A vibrant rose for error states or "Stop-and-Look" moments.

### The "No-Line" Rule
Traditional 1px solid borders are strictly prohibited for layout sectioning. Boundaries must be defined through **Tonal Transitions**. For instance, a footer should be distinguished from the main body by shifting from `surface` to `surface-container-low`, creating a seamless, architectural flow.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked sheets. 
*   **Base:** `surface`
*   **Layer 1 (The Canvas):** `surface-container-low`
*   **Layer 2 (The Focus):** `surface-container-high`
*   **Floating Elements:** Semi-transparent versions of `primary` or `surface-bright` with `backdrop-filter: blur(24px)`.

### The "Glass & Gradient" Rule
To achieve "Visual Soul," every glass element must sit atop a vibrant gradient background (transitioning from `secondary-container` to `tertiary-container`). Use `surface-tint` at 5% opacity within the glass cards to create a subtle shimmer that mimics the grain of real frosted glass.

---

## 3. Typography
We use a dual-font strategy to balance authority with readability.

*   **Display & Headlines (Plus Jakarta Sans):** A modern, geometric sans-serif. Use `display-lg` (3.5rem) with tighter letter-spacing (-0.02em) for hero titles to create a high-fashion, editorial impact.
*   **Body & Labels (Manrope):** A highly legible, contemporary face. `body-lg` (1rem) provides a clean, neutral balance to the expressive headlines.
*   **Hierarchy Note:** Use `on-surface-variant` (`#a3aac4`) for secondary body text to ensure the eye is naturally drawn first to the high-contrast `on-surface` (`#dee5ff`) headlines.

---

## 4. Elevation & Depth

### The Layering Principle
Depth is achieved through stacking tokens. Place a `surface-container-highest` card on top of a `surface-container-low` background. The subtle 4-6% shift in luminance provides all the separation needed without cluttering the UI with lines.

### Ambient Shadows
For "Floating" glass cards, use a dual-shadow approach:
1.  **Inner Glow:** A 1px "Ghost Border" using `outline-variant` at 20% opacity to simulate the edge of the glass catching light.
2.  **Outer Diffusion:** A shadow with `32px blur`, `0px offset`, and `4% opacity`, using the `secondary` or `tertiary` color instead of black to simulate colored light passing through the glass.

### Glassmorphism Specs
*   **Background:** `rgba(25, 37, 64, 0.4)` (derived from `surface-variant`)
*   **Backdrop Blur:** `20px` to `40px` depending on the complexity of the background.
*   **Saturate:** `150%` (to make the colors underneath feel more vibrant through the frost).

---

## 5. Components

### Buttons
*   **Primary:** A gradient from `secondary` to `primary-container`. `border-radius: full`. Text: `on-secondary`.
*   **Secondary (Glass):** Semi-transparent background with `backdrop-filter: blur(8px)` and a `1px` ghost border (`outline-variant` at 30%).
*   **Interaction:** On hover, increase the `backdrop-filter` strength and the `outline` opacity.

### Cards
Cards must never have solid background colors. Use the `surface-container` tiers with a `10%` opacity layer of the `surface-tint` to create a "sheen." Use `xl` (1.5rem) corner rounding for a soft, premium feel.

### Input Fields
*   **Background:** `surface-container-lowest` at 60% opacity.
*   **Border:** Use the "Ghost Border" fallback—`outline-variant` at 15% opacity.
*   **Active State:** The border transitions to `secondary` with a subtle outer glow.

### Chips & Tags
Use `secondary-fixed-dim` for backgrounds with `on-secondary-fixed` text. Keep these small (`label-md`) and use `full` roundedness to contrast against the more architectural cards.

---

## 6. Do's and Don'ts

### Do:
*   **Embrace Negative Space:** Allow display typography to "breathe" by giving it 2x the standard padding.
*   **Use Colored Light:** Use soft, large-scale blurs of `primary` and `secondary` in the background to create a sense of deep space.
*   **Layer with Purpose:** Ensure that if an element overlaps another, the `backdrop-filter` is strong enough to maintain text legibility.

### Don't:
*   **Don't use pure black (#000) for shadows.** It kills the "glass" illusion. Use a dark navy or a tinted version of the surface.
*   **Don't use divider lines.** Separate list items using `8px` of vertical white space and a 2% shift in background color on hover.
*   **Don't over-blur.** If the background is too blurry, it loses the "glass" feel and just looks like a solid color. You should still see the "ghost" of the shapes behind the glass.
*   **Don't use high-contrast borders.** Anything more than 20% opacity on a border will break the ethereal aesthetic.