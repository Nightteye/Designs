# Design System Document: High-End Editorial Flatness

## 1. Overview & Creative North Star: "The Modern Cartographer"

This design system moves beyond the "standard" corporate flat design. Our Creative North Star is **The Modern Cartographer**. Like a high-end travel guide or a precision-engineered map, the system relies on absolute clarity, vibrant navigational cues, and intentional asymmetry to guide the user through complex information. 

While the request specifies "no shadows or gradients," we achieve depth through **Tonal Architecture**. We treat the screen not as a flat canvas, but as a series of meticulously cut paper layers. The "editorial" feel is established by using extreme shifts in typographic scale—pairing massive `display-lg` headlines with tightly tracked `label-sm` metadata—creating a rhythm that feels curated and professional rather than templated.

## 2. Colors: Vibrancy through Tonal Layering

The palette is anchored in a deep, sophisticated navy (`on_background`: #2e2a50) and energized by a high-performance primary blue (`primary`: #2f42eb). 

### The "No-Line" Rule
To maintain a premium editorial feel, **1px solid borders are strictly prohibited for sectioning.** Traditional dividers feel "default" and cluttered. Instead, define boundaries through background color shifts. A section should transition from `surface` (#f9f5ff) to `surface_container_low` (#f3eeff) to create a clear, sophisticated break in content without a single line being drawn.

### Surface Hierarchy & Nesting
Treat the UI as a physical stack. Importance is dictated by how "close" a surface is to the user, represented by its container tier:
*   **Base Layer:** `surface` (#f9f5ff) — Used for the main page body.
*   **Secondary Content:** `surface_container` (#eae5ff) — Used for grouped sidebar content.
*   **Prominent Callouts:** `surface_container_highest` (#ded8ff) — Use this for "Step-by-Step" tutorial blocks to make them pop against the base.

### Interaction & Accent
*   **The Power of Tertiary:** Use `tertiary` (#6b5b00) and `tertiary_container` (#fcd800) exclusively for "Aha!" moments, tips, or highlights within a tutorial. Its yellow-gold hue provides a vibrant counter-beat to the primary blue.

## 3. Typography: The Editorial Voice

We utilize two high-end sans-serifs to create a "Signature Editorial" look.

*   **The Display Voice (Plus Jakarta Sans):** Used for all `display`, `headline`, and `title` levels. It is modern, geometric, and carries a premium weight. 
    *   *Editorial Tip:* Use `display-lg` for hero sections but offset it with an asymmetrical margin to create a custom, "non-bootstrap" feel.
*   **The Informational Voice (Manrope):** Used for `body` and `label` levels. Manrope provides exceptional legibility for long-form guide content and tutorials.
*   **Hierarchy as Navigation:** Use `label-md` in all-caps with increased letter-spacing for "Step Numbers" or "Categories." This creates an authoritative, "Guidebook" aesthetic.

## 4. Elevation & Depth: Tonal Stacking

Since shadows and gradients are forbidden, we convey hierarchy through **Tonal Layering**.

*   **The Layering Principle:** Depth is achieved by "stacking" container tiers. To make a "Card" look elevated, place a `surface_container_lowest` (#ffffff) card atop a `surface_container_low` (#f3eeff) background. The subtle shift in hex code provides a cleaner, more modern "lift" than a drop shadow.
*   **The "Ghost Border" Fallback:** In rare cases where elements of the same color must touch (e.g., a search input on a white card), use a "Ghost Border." Apply the `outline_variant` (#aea8d7) at **15% opacity**. It should be felt, not seen.
*   **Asymmetrical Compositions:** To avoid the "generic flat" look, overlap vector illustrations across surface color shifts. This "breaks the box" and makes the layout feel custom-designed rather than modular.

## 5. Components: Precision Primitives

### Buttons
*   **Primary:** Solid `primary` (#2f42eb) with `on_primary` (#f3eeff) text. Use `md` (0.375rem) roundedness. No borders.
*   **Secondary:** Solid `secondary_container` (#80deff) with `on_secondary_container` (#004e61) text. This provides a vibrant, approachable alternative for secondary actions.
*   **Tertiary/Ghost:** No container. Use `primary` text with `label-md` styling (all caps) for a high-end navigational look.

### Cards & Tutorials
*   **The "No Divider" Rule:** Forbid the use of line dividers in lists. Use `surface_container_high` (#e4dfff) for the "active" or "hover" state of a list item, and use vertical white space (32px+) to separate distinct tutorial steps.
*   **Step Indicators:** Use `tertiary_container` (#fcd800) circles with `on_tertiary_container` text to mark tutorial progress.

### Input Fields
*   **Style:** Use `surface_container_lowest` (#ffffff) as the fill. 
*   **Active State:** Instead of a shadow, use a 2px solid `primary` (#2f42eb) border only on the *bottom* or as a full frame to denote focus.

### Additional Signature Components
*   **The "Progress Ribbon":** A slim, 4px tall bar using `primary_container` (#8d98ff) that runs across the top of the page, filling with `primary` as the user scrolls through the guide.
*   **Contextual Callouts:** Large-format blocks using `secondary_container` (#80deff) with `lg` (0.5rem) roundedness to house "Pro-Tips" or "Note" sections.

## 6. Do's and Don'ts

### Do:
*   **Do** use asymmetrical layouts (e.g., a 7-column main content area with a 5-column empty space or offset illustration).
*   **Do** lean into the "Vibrant" aspect of the prompt by using `secondary` and `tertiary` containers for background blocks.
*   **Do** ensure high contrast; use `on_surface` (#2e2a50) for all primary reading text to ensure accessibility against light lavender backgrounds.

### Don't:
*   **Don't** use 1px lines or dividers. If you feel you need one, increase the padding and change the background color of the next section instead.
*   **Don't** use any opacity on text. Use the specific "on-surface-variant" tokens to ensure the color remains solid and "flat."
*   **Don't** center-align long-form tutorial text. Keep it left-aligned for an editorial, "book-like" feel.