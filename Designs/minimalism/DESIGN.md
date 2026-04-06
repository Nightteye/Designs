# Design System Strategy: The Editorial Curator

## 1. Overview & Creative North Star
This design system is built upon the concept of **"The Digital Curator."** We are moving away from the "web-template" aesthetic and toward a high-end editorial experience—think premium print journals or luxury museum monographs. 

The North Star is **Intentional Restraint**. By utilizing a razor-sharp monochrome palette and extreme whitespace, we create a vacuum of noise where content becomes the focus. We break the rigid, boxy grid of standard web design through **asymmetric balancing**: using large-scale typography and high-quality imagery to "weight" a page, rather than relying on structural lines or containers. This system feels expansive, breathable, and authoritative.

---

## 2. Color & Tonal Depth
Our palette is a sophisticated range of warm grays and off-whites. The goal is a "paper-like" feel that avoids the harshness of pure #000 and #FFF.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to section off content. Physical boundaries are an admission of failed hierarchy. Instead:
- **Color Shifts:** Use `surface` (default) against `surface-container-low` to define a new section.
- **Negative Space:** Use the Spacing Scale to create "voids" that act as invisible barriers.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack of fine paper. 
- **Base Layer:** `surface` (#f9f9f9)
- **Primary Content Blocks:** `surface-container-low` (#f2f4f4)
- **High-Priority Floating Elements:** `surface-container-lowest` (#ffffff) for maximum "lift."
- **In-Set Details:** Use `surface-container-high` (#e4e9ea) only for small interactive areas like search bars or code snippets.

### Signature Textures (Glass & Gradient)
To prevent a "flat" or "cheap" feel, implement these two custom treatments:
1.  **The Editorial Wash:** Use a subtle linear gradient from `primary` (#5f5e5e) to `primary-dim` (#535252) for main CTA backgrounds. This adds a "silk" finish.
2.  **The Frosted Pane:** For floating navigation or modals, use `surface` at 80% opacity with a `24px` backdrop-blur. This allows the high-quality imagery underneath to bleed through, softening the layout.

---

## 3. Typography: The Narrative Voice
We use two typefaces: **Manrope** for structural authority (Display/Headline) and **Inter** for clarity and utility (Body/Labels).

*   **The Hero (Display-lg):** `Manrope`, 3.5rem. Set with tight letter-spacing (-0.02em). This is your signature. It should be used as an architectural element, often overlapping imagery or sitting in vast whitespace.
*   **The Narrative (Body-lg):** `Inter`, 1rem. High line-height (1.6) is mandatory. This ensures the guide feels readable and premium, not cluttered.
*   **The Metadata (Label-md):** `Inter`, 0.75rem. Use `on-surface-variant` (#596061) to create a clear secondary tier for dates, tags, or categories.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "digital." We achieve depth through **Tonal Layering**.

*   **The Layering Principle:** Place a `surface-container-lowest` card on a `surface-container-low` background. The difference in hex value creates a soft, natural lift that mimics heavy cardstock without the need for a shadow.
*   **Ambient Shadows:** If a shadow is required for a floating "Menu," use: `box-shadow: 0 20px 40px rgba(45, 52, 53, 0.06);`. The color is a tinted `on-surface` (#2d3435), not black.
*   **The Ghost Border:** If a border is required for accessibility (e.g., in input fields), use `outline-variant` (#acb3b4) at **15% opacity**. It should be barely perceptible.
*   **Hard Edges:** All `borderRadius` tokens are set to **0px**. In this system, precision is luxury. Rounded corners feel "friendly" and "consumer"; sharp corners feel "curated" and "architectural."

---

## 5. Components

### Buttons
*   **Primary:** `primary` background, `on-primary` text. No radius. Padding: `16px 32px`.
*   **Secondary:** `surface-container-high` background, `on-surface` text.
*   **Tertiary:** No background. Underline using `primary` at 2px weight, offset by 4px.

### Cards & Lists
*   **The Divider Ban:** Never use a horizontal rule `<hr>`. Separate list items using 24px of vertical whitespace or a transition from `surface` to `surface-container-low`.
*   **Card Styling:** No borders. Depth is achieved via `surface-container-lowest` on top of `surface`.

### Inputs
*   **Text Fields:** Bottom-border only (the "Ghost Border"). When active, the border transitions to `primary`. No "box" containers for inputs.

### Custom Component: The "Hero Plate"
A specific layout for guide headers: A full-bleed image (aspect-ratio 21:9) with a `surface-container-lowest` text block overlapping the bottom-left corner by 40px. This "overlap" breaks the grid and creates professional tension.

---

## 6. Do’s and Don'ts

### Do:
*   **Embrace Asymmetry:** Align the headline to the left and the body text to a 60% width column on the right.
*   **Use Tonal Shifts:** Change the background color of the entire section to denote a change in topic.
*   **High-End Imagery:** Only use photography with a consistent grain and desaturated palette to match the monochrome UI.

### Don't:
*   **Don't Use Borders:** If you feel the need to draw a line, increase your spacing by 2x instead.
*   **Don't Use Shadows:** Shadows are for apps; we are building an experience. Use tonal stacking.
*   **Don't Round Corners:** 0px radius across the entire system. Sharpness equals sophistication.
*   **Don't Over-Color:** Accent colors (`error`, etc.) should only appear in response to user error. The rest of the interface stays monochrome to let the *content's* colors shine.