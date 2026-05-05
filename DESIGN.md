```markdown
# Design System Strategy: Metropolitan Brutalism

## 1. Overview & Creative North Star: "Metropolitan Brutalism"
The Creative North Star for this design system is **Metropolitan Brutalism**. Unlike standard e-commerce templates that rely on soft shadows and rounded corners, this system embraces the raw, architectural energy of Managua’s urban landscape. 

We are moving away from the "friendly" web. This system is defined by **hard edges (0px radius)**, intentional **asymmetry**, and **stark tonal shifts**. By utilizing a high-contrast palette and sophisticated editorial typography, we create a space that feels like a premium streetwear lookbook rather than a generic storefront. We break the grid by overlapping large-scale typography with sharp-edged imagery, creating a sense of motion and "street" urgency.

---

## 2. Colors & The Tonal Architecture
The palette is built on a foundation of deep charcoals and pure blacks, punctuated by high-energy reds.

### Color Roles
*   **The Void (Background):** `#131313` is our canvas. It provides a premium, "night-mode" default that makes product photography and red CTAs pop.
*   **The Pulse (Primary):** Use `primary_container` (`#ff5545`) for high-contrast actions. This isn't a subtle red; it’s a signal. Use it sparingly to guide the eye toward conversion.
*   **The Concrete (Neutrals):** `secondary` (`#c6c6c7`) and `surface_variant` (`#353535`) handle the heavy lifting for secondary information.

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. We define boundaries through background color shifts. 
*   To separate a section, transition from `surface` (`#131313`) to `surface_container_low` (`#1b1b1b`). 
*   The transition must feel architectural, not decorative.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked slabs. 
*   **Base:** `surface` (`#131313`)
*   **Nested Content:** `surface_container` (`#1f1f1f`)
*   **Elevated Interaction:** `surface_bright` (`#393939`)
This creates depth through "Tonal Layering" rather than artificial shadows.

### Signature Textures
While the system is flat, we introduce "soul" through subtle gradients. Main CTAs should use a vertical gradient from `primary` (`#ffb4aa`) to `primary_container` (`#ff5545`) to create a "machined" metallic look that feels premium and industrial.

---

## 3. Typography: Editorial Impact
We utilize a dual-typeface system to balance "Street Edgy" with "Data Professional."

*   **Display & Headlines (Space Grotesk):** This is our "Voice." Space Grotesk is a quirky, bold sans-serif that feels technical yet rebellious. Use `display-lg` (3.5rem) with tight letter-spacing (-0.02em) for hero sections. Headlines should often be all-caps to lean into the brutalist aesthetic.
*   **Body & Labels (Inter):** For data-heavy sections (shipping info, product specs, forms), we switch to Inter. It is invisible, highly readable, and professional.
*   **Hierarchy Tip:** Contrast a `display-sm` headline in Space Grotesk with a `label-sm` in Inter for a "poster-style" layout that feels intentionally designed.

---

## 4. Elevation & Depth
In this design system, shadows are almost entirely replaced by color-value layering.

*   **The Layering Principle:** Place a `surface_container_highest` (`#353535`) card on top of a `surface_container_low` (`#1b1b1b`) background. The difference in hex value provides the "lift."
*   **Ambient Shadows:** If a floating element (like a mobile nav or modal) requires a shadow, use a "Tinted Ambient Shadow." The shadow color should be a 10% opacity version of `surface_container_lowest` (`#0e0e0e`) with a 40px blur. No hard "drop" shadows allowed.
*   **The "Ghost Border" Fallback:** For input fields or cards where accessibility is a concern, use a "Ghost Border": `outline_variant` (`#603e39`) at 20% opacity. It should be felt, not seen.
*   **Glassmorphism:** For overlays, use `surface_container` with a 12px backdrop-blur and 80% opacity. This allows the high-contrast urban photography to bleed through the UI, maintaining the brand's atmospheric depth.

---

## 5. Components

### Buttons
*   **Primary:** Rectangular (0px radius), background `primary_container` (`#ff5545`), text `on_primary_fixed` (`#410001`). Bold Space Grotesk caps.
*   **Secondary:** Ghost style. No background. `outline` color border at 20% opacity. White text.
*   **Hover State:** Shift background from red to `primary_fixed` (`#ffdad5`). The transition should be instant (50ms) to feel "edgy" and responsive.

### Input Fields
*   **Style:** Underline only or full block. 
*   **Block Style:** Background `surface_container_high` (`#2a2a2a`), 0px radius. Bottom-heavy 2px border using `primary` only on focus.
*   **Error State:** Use `error` (`#ffb4ab`) text and a subtle `error_container` (`#93000a`) background tint.

### Cards & Lists
*   **Constraint:** Zero dividers. Use vertical whitespace (32px, 48px, or 64px) to separate items.
*   **Hover:** On hover, a card’s background should shift from `surface` to `surface_container_low`. This "quiet" interaction maintains the professional tone.

### Streetwear Specific Components
*   **Size Picker:** Large, square (0px) tiles. Selected state is `primary_container` with white text; unselected is `surface_container_highest` with grey text.
*   **Flash-Sale Ticker:** A high-contrast bar using `inverse_primary` (`#c0000a`) background with scrolling `label-md` text.

---

## 6. Do’s and Don’ts

### Do:
*   **Do** embrace the 0px radius. Even images must be sharp-edged.
*   **Do** use asymmetrical margins. For example, a left margin of 10% and a right margin of 20% for text blocks.
*   **Do** use "Extreme Scale." Contrast a massive 3.5rem headline with a tiny 0.75rem label right next to it.
*   **Do** use high-quality, high-grain urban photography.

### Don’t:
*   **Don’t** use rounded corners. A single 4px radius will break the entire "Metropolitan Brutalism" aesthetic.
*   **Don’t** use standard "Grey" shadows. They look muddy on a `#131313` background.
*   **Don’t** use dividers or 1px lines to separate sections. If the layout feels messy, increase the padding or shift the background tone.
*   **Don’t** use center-alignment for everything. Streetwear is about the "edge"—keep layouts primarily left-aligned or staggered.

---
**Director's Final Note:** This system succeeds when it feels "expensive and aggressive." It should feel like a high-end streetwear boutique in the middle of a concrete jungle. Stay sharp. Stay high-contrast.```