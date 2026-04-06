# Design System Document: Tactile Minimalism

## 1. Overview & Creative North Star
**Creative North Star: "The Sculpted Surface"**

This design system moves away from the flat, digital abstraction of the last decade and returns to a sense of physical presence. We are not building "pages"; we are carving interfaces out of a singular, continuous material. By utilizing the principles of Neumorphism—reimagined through a high-end editorial lens—we create a hero experience that feels extruded, soft, and tactile.

To break the "standard template" look, this system rejects rigid grids in favor of **intentional asymmetry** and **tonal depth**. Elements should overlap slightly, using nested layers to create a "topographical" layout where the interface feels like a physical object responding to light.

---

## 2. Colors & Tonal Soul
The palette is a sophisticated, monochromatic cool-grey with blue undertones, designed to mimic the behavior of natural light on a matte surface.

### The Palette
- **Base Surface:** `#f6f9ff` (Surface) — This is our primary canvas.
- **Primary Accent:** `#50606c` (Primary) — Used sparingly for high-contrast moments.
- **Success/Neutral:** `#e4effc` (Surface Container) — The mid-tone for "recessed" areas.

### The "No-Line" Rule
**Prohibit 1px solid borders for sectioning.** Boundaries must be defined solely through background color shifts or the interaction of light and shadow. To separate the hero section from the navigation or the next fold, transition from `surface` to `surface-container-low` (`#ecf4fe`). 

### Signature Textures & Gradients
To provide "soul," use subtle linear gradients on large surfaces. A Hero CTA should not be a flat block; it should transition from `primary` (`#50606c`) to `primary-container` (`#d3e5f3`) at a 135-degree angle to simulate a light source from the top-left.

---

### 3. Typography: The Editorial Voice
We pair the architectural strength of **Manrope** for displays with the functional clarity of **Inter** for UI elements.

*   **Display (Manrope):** Use `display-lg` (3.5rem) for hero statements. Set with tight letter-spacing (-0.02em) to create an authoritative, "printed" feel.
*   **Headlines (Manrope):** `headline-lg` (2rem) should be used for secondary value propositions.
*   **Body (Inter):** `body-lg` (1rem) for descriptions. Ensure a line-height of 1.6 to maintain "breathability" against the tactile UI.
*   **Labels (Inter):** `label-md` (0.75rem) in uppercase with increased tracking (+0.05em) for small tactile buttons or eyebrow copy.

---

## 4. Elevation & Depth: The Neumorphic Physics
Hierarchy is achieved through **Tonal Layering** and directional light, not structural lines.

### The Layering Principle
Stacking defines importance. 
- **The Base:** `surface` (`#f6f9ff`).
- **The Extrusion (Raised):** Use two shadows. 
    - *Light Shadow:* Top-left, `-8px -8px 20px #ffffff`.
    - *Dark Shadow:* Bottom-right, `8px 8px 20px #d2e5f7`.
- **The Cavity (Sunken):** For input fields or depressed states, use `inset` shadows with the same logic.

### Ambient Shadows & Glassmorphism
When an element needs to "float" (like a navigation bar or a modal), use **Glassmorphism**:
- **Background:** `surface_container_lowest` (`#ffffff`) at 70% opacity.
- **Backdrop-blur:** `20px`.
- **Shadow:** A diffused "Ambient Shadow" using `on-surface` (`#233442`) at 4% opacity with a `40px` blur.

### The "Ghost Border" Fallback
If a border is required for accessibility, use the `outline-variant` token at 15% opacity. Never use 100% opaque borders; they shatter the illusion of a continuous sculpted surface.

---

## 5. Components

### Buttons (The Tactile Trigger)
- **Primary (Extruded):** Background `surface`. Roundedness `xl` (1.5rem). Use the dual-shadow technique to make it pop from the background. On hover, the shadows should slightly contract (blur reduced from 20px to 12px) to simulate being pressed.
- **Tertiary (Text):** No background. Use `primary` color text. Ensure the hit area is defined by a `surface-container-highest` background only on hover.

### Input Fields (The Carved Cavity)
- Forbid standard box-borders. Use an `inset` shadow on `surface-container-low` to make the field look carved into the page.
- **Typography:** Use `body-md`.
- **Corner Radius:** `md` (0.75rem).

### Cards
- **Rule:** Forbid divider lines. Use vertical white space from the spacing scale (e.g., 32px or 48px) to separate content sections within a card.
- **Styling:** Cards should sit on `surface-container-highest` (`#d2e5f7`) with a very subtle `0.5rem` (DEFAULT) corner radius to feel like heavy, premium cardstock.

### Hero Imagery
Avoid standard rectangular containers. Use organic, rounded shapes or "floating" transparent PNGs that cast the same soft ambient shadows as the UI components, integrating the photography into the "sculpted" world.

---

## 6. Do's and Don'ts

### Do:
*   **Use Light Direction:** Ensure all shadows (light and dark) across the page assume a light source from the top-left (135 degrees).
*   **Embrace Negative Space:** Neumorphism requires "room to breathe" to avoid looking cluttered. Increase your standard padding by 20%.
*   **Prioritize Contrast:** Ensure text on soft pastel backgrounds meets WCAG AA standards by using the `on-surface` (`#233442`) token for maximum legibility.

### Don't:
*   **Don't use pure black shadows:** Shadows should always be a tinted, darker version of the background color (`#d2e5f7`) to maintain the "soft" aesthetic.
*   **Don't over-stack:** Limit depth to 3 layers (Base > Raised Card > Inset Button). Any more will make the UI feel heavy and dated.
*   **Don't use 1px borders:** Rely on the `surface` color shifts to define edges. If you can see a line, it’s not tactile enough.