# Design System Document: Morning Mist Editorial

## 1. Overview & Creative North Star: "The Ethereal Curator"
This design system moves away from the rigid, boxed-in layouts of traditional SaaS and toward a high-end, editorial experience. Our Creative North Star is **The Ethereal Curator**. Imagine a gallery at dawn: the light is soft, the boundaries between objects are blurred by a gentle mist, and every element feels intentional, light, and premium.

To achieve this, we break the "template" look through:
*   **Intentional Asymmetry:** Avoid perfectly centered grids. Use offset typography and varied column widths to create a sense of movement.
*   **Breathing Room:** White space is not "empty"; it is a functional luxury. We use generous margins to let the content exhale.
*   **Layered Translucency:** We replace solid dividers with depth, stacking semi-transparent "glass" sheets to create hierarchy.

---

## 2. Colors & The Surface Philosophy
The palette is a sophisticated blend of botanical greens (`primary`), aquatic teals (`secondary`), and muted plum (`tertiary`), all resting on a foundation of "Morning Mist" neutrals.

### The "No-Line" Rule
**Borders are forbidden for structural sectioning.** To separate a header from a hero or a sidebar from a main feed, use background shifts. 
*   *Example:* Place a `surface-container-low` section directly against a `surface` background. The subtle tonal shift is enough to signal a transition without the "cheapening" effect of a 1px line.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of frosted glass.
*   **Base Layer:** `surface` (#f8fafb)
*   **Sectioning:** `surface-container-low` (#f0f4f6) for large background blocks.
*   **Interaction Containers:** `surface-container-highest` (#dce4e6) for elements that need to pop.
*   **Floating Elements:** `surface-container-lowest` (#ffffff) for cards that should feel like they are catching the most light.

### The "Glass & Gradient" Rule
To capture the "Liquid Glass" aesthetic, use `surface-container-lowest` at 70% opacity with a `backdrop-filter: blur(20px)`. 
*   **Signature Textures:** For primary CTAs, do not use flat colors. Apply a subtle linear gradient from `primary` (#3c6942) to `primary-container` (#bdefbe) at a 135-degree angle. This adds a "soul" to the button that feels liquid and reactive.

---

## 3. Typography: Editorial Authority
We utilize **Plus Jakarta Sans** for its geometric clarity and high-end modernism.

*   **Display (lg/md):** Reserved for "Hero" moments. Use `on-surface` with a slight letter-spacing reduction (-0.02em) to feel like a high-fashion masthead.
*   **Headlines:** These are your anchors. Use `headline-lg` to break up long-form content, ensuring enough `surface-container` padding surrounds them.
*   **Body (lg/md):** Our primary vehicle for information. Use `on-surface-variant` (#596063) for long-form reading to reduce eye strain and maintain the "Mist" softness.
*   **Labels:** Use `label-md` in all-caps with +0.05em tracking for a "system tag" look that feels professional and intentional.

---

## 4. Elevation & Depth: Tonal Layering
In this system, shadow is a last resort, not a default.

*   **The Layering Principle:** Achieve depth by nesting. A `surface-container-lowest` card sitting on a `surface-container-low` background creates a natural, soft lift.
*   **Ambient Shadows:** If a floating element (like a modal or dropdown) requires a shadow, use a "Mist Shadow": 
    *   `box-shadow: 0 12px 40px rgba(44, 52, 54, 0.06);` 
    *   The shadow color is derived from `on-surface`, not pure black, to mimic natural light diffusion.
*   **The "Ghost Border":** For essential accessibility on inputs or cards, use `outline-variant` at 15% opacity. It should be felt, not seen.
*   **Iridescent Accents:** Use the `tertiary-container` (#f8bbd0) as a soft "glow" behind key elements or as a subtle hover state to mimic light hitting a prism.

---

## 5. Components: Fluid Primitives

### Buttons
*   **Primary:** Gradient of `primary` to `primary-container`. `9999px` (full) roundedness. No border.
*   **Secondary:** Glassmorphic. `surface-container-lowest` at 40% opacity, 12px blur, with a `Ghost Border`.
*   **States:** On hover, increase the `backdrop-blur` or slightly shift the gradient angle. Avoid harsh color jumps.

### Cards & Lists
*   **The No-Divider Rule:** Forbid the use of horizontal rules (`<hr>`). Separate list items using `8px` of vertical space or by alternating very subtle background tints between `surface-container-low` and `surface`.
*   **Card Styling:** Use `xl` (1.5rem) corner radius. The large radius contributes to the "Liquid" feel—fluid and non-aggressive.

### Input Fields
*   **Styling:** Use `surface-container-lowest` as the fill. 
*   **Focus State:** Instead of a heavy border, use a subtle `2px` outer glow of `primary-fixed-dim` at 50% opacity.

### Featured Component: "The Mist Overlay"
For high-end interactions, use a full-screen overlay using a semi-transparent `surface-bright` with a heavy `40px` blur. This keeps the user grounded in the previous context while bringing the new content into sharp, editorial focus.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use asymmetrical margins (e.g., 10% left margin, 20% right margin) for headline elements.
*   **Do** layer glass elements. A glass card on a glass header creates a beautiful "frosted" stack.
*   **Do** use `tertiary` (#815163) for small, "human" moments—like a notification dot or a curated tag.

### Don’t:
*   **Don’t** use 100% opaque, high-contrast borders. It breaks the "Morning Mist" immersion.
*   **Don’t** use pure black (#000000) for text. Always use `on-surface` (#2c3436) to maintain the tonal softness.
*   **Don’t** crowd the interface. If you feel like you need a divider, you probably just need more white space.