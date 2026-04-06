```markdown
# Design System Specification: The Tactile Atelier

## 1. Overview & Creative North Star
**Creative North Star: "The Analog Precision"**
This design system rejects the "flat" web. We are building a digital environment that feels machined, stitched, and molded. The goal is to move beyond mere skeuomorphism into a realm of high-fidelity "Neo-Tactility." We treat the screen not as a flat plane of pixels, but as a shallow physical box containing materials like brushed aluminum, top-grain leather, and smoked glass.

To break the "template" look, designers must embrace **intentional asymmetry**. Do not center every element; allow heavy "weighted" objects (like a brushed metal control panel) to sit offset against a soft leather "desk" surface. Overlap elements—let a glass card cast a multi-layered shadow over a recessed metal track—to prove the physical relationship between layers.

## 2. Color Palette & Materiality
The palette is rooted in charcoal (`#131313`), silver (`#C6C6C6`), and cream (`#E4E4CC`), punctuated by a hyper-modern electric cyan (`#3CD7FF`).

### The "No-Line" Rule
**Borders are forbidden.** In the physical world, objects are defined by light and shadow, not 1px outlines. Use the `surface-container` tiers to define boundaries. A `surface-container-highest` button sits *inside* a `surface-container-low` well. The "edge" is created by the transition from a highlight to a shadow, never a stroke.

### Surface Hierarchy & Nesting
*   **The Foundation (`surface` / `#131313`):** The base "desk" or "casing." Use a subtle noise texture to mimic matte charcoal plastic or leather.
*   **The Well (`surface-container-lowest` / `#0E0E0E`):** Used for recessed areas (input tracks, empty states). These must feature a `2px` inner shadow to imply depth.
*   **The Instrument (`surface-container-high` / `#2A2A2A`):** The primary material for cards and panels.
*   **The Glass Overlay (`surface-bright` at 40% opacity):** Use for floating HUD elements with a `24px` backdrop-blur.

### Signature Textures & Gradients
*   **Brushed Metal:** Apply a linear gradient from `secondary` to `secondary_fixed_dim` at a 45-degree angle. Add a 1px "specular highlight" on the top edge using `on_secondary_container` at 30% opacity.
*   **Vibrant CTAs:** Use a radial gradient for primary buttons: `primary` (#3CD7FF) at the center fading to `on_primary_container` (#00A1C2) at the edges. This creates a "glowing bulb" effect.

## 3. Typography
We utilize a hierarchy that balances technical precision with editorial authority.

*   **Display & Headlines (Manrope):** These are your "engraved" elements. For `display-lg` and `headline-md`, apply a 1px `drop-shadow(0px 1px 0px rgba(255,255,255,0.1))` and an `inner-shadow(0px 1px 2px rgba(0,0,0,0.8))`. This makes the text look stamped into the metal or leather.
*   **Body (Inter):** High-readability utilitarian text. Use `on_surface_variant` for secondary info to maintain a low-contrast, premium feel.
*   **Labels (Space Grotesk):** These represent "technical markings." Use `label-md` in all-caps with `letter-spacing: 0.1em`. They should look like silk-screened labels on a high-end amplifier.

## 4. Elevation & Depth: The Stacking Principle

### Tonal Layering
Avoid traditional drop shadows for layout separation. Instead, use "Tonal Stacking":
1.  **Level 0 (Base):** `surface`
2.  **Level 1 (Recessed):** `surface-container-lowest` (Negative elevation)
3.  **Level 2 (Raised):** `surface-container-high` (Positive elevation)

### Multi-Layered Shadows
When an object must "float" (e.g., a modal or a primary toggle), use three layers of shadows:
1.  **The Occlusion:** `0px 2px 4px rgba(0,0,0,0.5)` (Tight and dark)
2.  **The Ambient:** `0px 10px 20px rgba(0,0,0,0.3)` (Soft and wide)
3.  **The Tint:** `0px 20px 40px rgba(0,0,0,0.2)` (Using a tint of `primary` if the object is an active CTA).

### The "Ghost Border" Fallback
If contrast fails, use a "Light Leak" instead of a border. Apply a 1px inner-shadow on the top-left using `outline_variant` at 15% opacity to simulate light hitting the edge of the material.

## 5. Components

### Buttons (The "Machined Switch")
*   **Primary:** A "pushed" state is not just a color change; it is a physical shift. The default state has a `4px` bottom shadow. The `:active` state removes the shadow and applies a `2px` inner shadow to show the button has physically depressed into the housing.
*   **Secondary:** Brushed silver texture with embossed `Space Grotesk` labels.

### Input Fields (The "Inset Track")
*   **Styling:** Use `surface-container-lowest` with a `rounded-md` corner.
*   **Depth:** Apply a `inset 0px 2px 4px rgba(0,0,0,0.4)` shadow. The text should have a 1px bottom highlight (`on_surface` at 10%) to look like it's glowing slightly from within the track.

### Cards & Lists
*   **No Dividers:** Separate list items using a `12px` gap. Each item should sit on a slightly different tonal plane.
*   **Selection:** A selected list item should transition from `surface-container` to a `primary_container` gradient, appearing to "light up" from behind.

### The "Anode" Toggle (Custom Component)
A physical-style toggle switch. The "track" is `surface-container-lowest`. The "knob" is a `secondary_fixed` circular element with a radial "CD-track" texture. When "on," a small `primary` LED-style dot glows.

## 6. Do’s and Don’ts

### Do:
*   **Do** use `backdrop-filter: blur()` on all glass panels to maintain the illusion of thickness.
*   **Do** vary your corner radii slightly between nested elements (e.g., an `lg` card containing `md` buttons) to create a "nested" look.
*   **Do** use "Specularity." Add a tiny, high-contrast white dot (opacity 0.6) on the top corner of interactive dials to simulate a light source.

### Don't:
*   **Don't** use pure `#000000` or `#FFFFFF`. The world has color; use `surface-container-lowest` and `on_surface`.
*   **Don't** use 100% opaque borders. They break the skeuomorphic illusion.
*   **Don't** use "flat" icons. Icons must have a subtle `drop-shadow` or `inner-shadow` to match the material they sit on.