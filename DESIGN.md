# Design System Specification: The Gastronomic Editorial

## 1. Overview & Creative North Star
The Creative North Star for this design system is **"The Culinary Monograph."** 

We are moving away from the "fast-food" digital template and toward a high-end, editorial experience that mirrors the precision and heritage of Pakistani cuisine. This system treats the interface as a premium printed journal—combining bold, authoritative typography with a sophisticated use of tonal depth. 

We break the "standard" layout by embracing **intentional asymmetry**. Hero elements should overlap container boundaries, and large-scale typography should act as a structural element rather than just a label. This creates a sense of "Reliable Craftsmanship" that feels both modern and deeply rooted in the diner’s prestige.

---

## 2. Colors: Tonal Hunger
Our palette uses "Rich Reds" and "Deep Oranges" not as decorative accents, but as psychological triggers. We use high-chroma tones to evoke appetite, balanced by a sophisticated neutral foundation to maintain professional reliability.

### The Palette (Material Design Tokens)
*   **Primary (The Spice):** `#930009` (Primary) / `#ba1a1a` (Primary Container). Used for high-impact brand moments.
*   **Secondary (The Hearth):** `#a83900` (Secondary) / `#fc6018` (Secondary Container). Used to draw the eye toward "appetizing" interactions.
*   **Neutral Foundation:** `#f9f9f9` (Surface) / `#ffffff` (Surface Container Lowest).

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders are strictly prohibited for sectioning or containment. Boundaries must be defined through:
1.  **Tonal Shifts:** A `surface-container-low` section sitting against a `surface` background.
2.  **Negative Space:** Using the spacing scale to create clear psychological groupings.

### Signature Textures
To avoid a "flat" digital feel, main CTAs and Hero sections should utilize **Radial Gradients**. Transitioning from `primary` (#930009) to `primary_container` (#ba1a1a) creates a "glow" effect reminiscent of a tandoor oven, adding visual "soul" that flat hex codes cannot achieve.

---

## 3. Typography: The Editorial Voice
We utilize a high-contrast pairing: **Epilogue** for its bold, architectural headings and **Manrope** for its clean, Swiss-influenced readability.

*   **Display (Epilogue):** Set with tight letter-spacing (-0.02em). These are the "headlines" of our diner. Use `display-lg` (3.5rem) for hero statements, allowing text to overflow or overlap imagery.
*   **Headline (Epilogue):** Bold and modern. Used to categorize menu sections with authority.
*   **Body (Manrope):** Set with generous line-height (1.6) to ensure the descriptions of Haripur’s flavors are effortless to read. 
*   **Labels (Manrope):** High-tracking (+0.05em) and uppercase for technical details like "Spice Level" or "Wait Time."

---

## 4. Elevation & Depth: Tonal Layering
We reject the "drop shadow" defaults of the early web. Depth in this design system is achieved through physical stacking logic.

*   **The Layering Principle:** Treat the UI as layers of fine paper. 
    *   *Base:* `surface` (#f9f9f9)
    *   *Sub-Section:* `surface-container-low` (#f3f3f3)
    *   *Interactive Card:* `surface-container-lowest` (#ffffff)
*   **Glassmorphism & Depth:** For floating elements (like a "Cart" summary or "Special of the Day" pop-out), use `surface_container_lowest` at 80% opacity with a `20px backdrop-blur`. This allows the rich reds of the food photography to bleed through the interface.
*   **The "Ghost Border" Fallback:** If a container requires definition against a similar tone, use `outline-variant` (#e4beb9) at **15% opacity**. It should be felt, not seen.

---

## 5. Components

### Buttons: The "Pill" Aesthetic
*   **Primary:** Solid `primary` (#930009) with `on_primary` (#ffffff) text. Use `xl` (1.5rem) or `full` (9999px) roundedness to create a friendly, organic feel.
*   **Secondary:** `secondary_container` (#fc6018) background. This is our "Hunger" button.
*   **States:** On hover, use a subtle `surface-tint` overlay rather than a color change to maintain tonal integrity.

### Cards & Menu Items
*   **Rule:** Forbid the use of divider lines between items.
*   **Layout:** Use a `surface-container-lowest` card with an `xl` corner radius. The image should be "bleeding" off the top or side edge of the card to create an editorial, uncontained feel.
*   **Typography:** The price should be `title-lg` in `secondary` (#a83900) to ensure it is visible but not aggressive.

### Inputs & Text Fields
*   **Style:** Minimalist. Use `surface-container-high` as the background with no border.
*   **Focus:** Transition the background to `primary-fixed` (#ffdad5) with a subtle `primary` underline.

### Additional Signature Components
*   **Flavor Tags:** Small, `md` rounded chips using `secondary_fixed` (#ffdbcf) backgrounds.
*   **The "Heritage Overlay":** A semi-transparent overlay using the `tertiary` (#004783) blue for specific "University" or "History" related callouts, providing a professional, academic counter-balance to the warm reds.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** use large amounts of white space (minimum 64px between major sections).
*   **Do** overlap text on top of images using the "Glassmorphism" rule.
*   **Do** use the `primary` red for semantic "Quality" indicators.

### Don't:
*   **Don't** use pure black (#000000) for text; always use `on_surface` (#1a1c1c) to keep the "Editorial" warmth.
*   **Don't** use standard 4px "Material" shadows. If a shadow is needed, use a 32px blur at 4% opacity, tinted with the primary red color.
*   **Don't** use icons that are too "playful." Use thin-stroke, modern geometric icons to maintain professional reliability.