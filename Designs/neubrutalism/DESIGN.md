# Design System Strategy: The Raw Editorial

## 1. Overview & Creative North Star: "The Graphic Manifesto"
This design system rejects the "polite" UI of the last decade. It moves away from soft gradients and apologetic shadows, embracing instead **The Graphic Manifesto**. This is a high-impact, editorial-driven approach that treats every screen like a bold poster or a zine cover. 

The Creative North Star is **Intentional Friction**. We are not aiming for "seamlessness"; we are aiming for "presence." By using massive weights, unyielding black borders, and an unapologetic 0px radius, we create a digital experience that feels tactile, physical, and raw. The layout should feel like a series of cut-and-paste modules, using intentional asymmetry and overlapping elements to break the "template" feel of modern SaaS.

---

## 2. Colors & Surface Philosophy
We utilize a high-octane palette where "Primary" isn't just a color—it’s an architectural element.

### The "Anti-Depth" Surface Hierarchy
Unlike traditional systems that use shadows for depth, this system uses **Color Blocking** and **Nesting**.
*   **Surface Hierarchy:** Instead of soft elevations, use the `surface-container` tiers to create "Cutouts." A `surface-container-highest` card doesn't "float" over a `surface`; it is slammed onto it with a `4px` black border.
*   **The No-Line Rule (Reinterpreted):** In this system, 1px lines are strictly forbidden. If you need to separate sections, use a background shift to `surface-container-low` OR use a heavy `4px` black stroke (`on-surface`). There is no middle ground.
*   **Vibrant Functionalism:** 
    *   **Primary (#6d5a00 / #fdd400):** Our "Warning Yellow." Use for main actions and hero containers.
    *   **Secondary (#a400a4):** "Electric Magenta." Use for high-contrast accents and secondary interactive elements.
    *   **Tertiary (#006571):** "Deep Cyan." Provides a cooling counter-balance to the warmth of the yellow and pink.

### The Signature Shadow
Standard shadows are banned. All "depth" is achieved through **Hard-Drop Shadows**.
*   **Token Logic:** `X: 4px, Y: 4px, Blur: 0, Spread: 0, Color: #000000`. 
*   This creates a "sticker" effect that reinforces the raw, physical nature of the UI.

---

## 3. Typography: Bold Grotesque
Typography is the primary visual driver. We use a combination of **Space Grotesk** (Display) and **Be Vietnam Pro** (Body) to balance raw impact with functional readability.

*   **Display (Space Grotesk):** Set with tight letter-spacing (-0.02em) and heavy weights. These should feel like headlines in a street-style magazine.
*   **Body (Be Vietnam Pro):** A highly legible sans-serif. While the headers are loud, the body text remains grounded to ensure the UX is not sacrificed for the aesthetic.
*   **Scale Hierarchy:** 
    *   `display-lg` (3.5rem) is reserved for hero statements.
    *   `label-md` (0.75rem) should be set in All-Caps with a heavy weight to maintain the "labeling" aesthetic.

---

## 4. Elevation & Structural Rigidity
We achieve hierarchy through **Impact, not Atmosphere.**

*   **The 0px Rule:** Every corner is a hard 90-degree angle. This removes the "friendliness" of modern UI and replaces it with a professional, architectural rigidity.
*   **The "Shadow Offset" Principle:** To indicate an active or hovered state, the element should move physically. 
    *   *Resting:* 4px Shadow.
    *   *Hover:* 8px Shadow (Element appears to lift).
    *   *Pressed:* 0px Shadow (Element is "pushed" into the page).
*   **Strokes:** Use a uniform `4px` border for all containers. For smaller components like Chips or Inputs, a `2px` border is acceptable to maintain internal balance, but never 1px.

---

## 5. Components

### Buttons: The "Sticker" Component
*   **Primary:** Background: `primary_container` (#fdd400), Border: 4px `on-surface`, Shadow: 4px `on-surface`.
*   **Secondary:** Background: `secondary_container` (#ffbdf3), Border: 4px `on-surface`, Shadow: 4px `on-surface`.
*   **Typography:** Labels must be `label-md` or `label-sm` in bold, uppercase.

### Cards & Lists: The Modular Grid
*   **Rule:** Forbid divider lines. Separate list items using alternating background colors (`surface` vs `surface-container-low`) or by wrapping each item in its own 4px-bordered box.
*   **Nesting:** When placing a card inside a section, the card should use a contrasting background (e.g., a `primary_fixed` card on a `surface` background) to scream for attention.

### Inputs: The Industrial Form
*   **Style:** 4px black border, 0px radius. 
*   **Focus State:** The border color remains black, but the shadow increases to 8px, and the background shifts to `surface-bright`.
*   **Error State:** Border remains 4px, but shifts to `error` (#b02500) with a hard error-colored shadow.

### Chips: The Navigation Tabs
*   Selection chips should look like physical tabs. When "Selected," the chip should have a 0px shadow (pressed state) and a vibrant `secondary` background.

---

## 6. Do’s and Don'ts

### Do:
*   **Over-scale icons:** Use thick-stroke icons (2pt+) to match the 4px border weight of your containers.
*   **Embrace Asymmetry:** Place a heavy shadow on only the bottom and right sides of a container to imply a fixed light source.
*   **Use High Contrast:** Ensure text on vibrant backgrounds always hits AAA accessibility by using the `on-primary` and `on-secondary` tokens correctly.

### Don’t:
*   **Don't use 1px lines:** They look like mistakes in this system. If a line is needed, make it a statement.
*   **Don't use gradients:** Except for very specific "Editorial Gradients" in hero sections, keep surfaces flat and matte.
*   **Don't use Border Radius:** Any curve breaks the "Brutalist" illusion. 0px is the only allowed value.
*   **Don't use Soft Shadows:** If you can't see the hard edge of the shadow, it doesn't belong here.