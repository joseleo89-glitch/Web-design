```markdown
# Design System Document

## 1. Overview & Creative North Star: "The Architectural Precision"
This design system is built upon the concept of **Architectural Precision**. For a tech consultancy like this, we move beyond generic "IT blue" boxes. Instead, we treat the digital interface as a high-end physical space—think of a glass-walled executive suite overlooking a clean, structured landscape. 

The "template" look is intentionally broken through **dynamic asymmetry**. We use large, editorial-style typography scales and overlapping "glass" layers to create depth. By prioritizing breathing room (negative space) over structural lines, we signal a brand that is organized, high-value, and focused on clarity over clutter.

---

## 2. Color Strategy & Tonal Depth
Our palette is rooted in a sophisticated transition from deep trust (Primary Blue) to growth (Accent Green).

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders for sectioning. Structural boundaries must be defined solely through:
1.  **Background Color Shifts:** Use `surface-container-low` (#f2f3ff) for sections sitting on a `surface` (#faf8ff) background.
2.  **Tonal Transitions:** Use soft shifts in saturation to denote the end of one content block and the start of another.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. We use the **Surface Tiering** model to create depth without visual noise:
*   **Level 0 (Base):** `surface-container-lowest` (#ffffff) for the main canvas.
*   **Level 1 (Sections):** `surface-container-low` (#f2f3ff) for secondary content areas.
*   **Level 2 (Cards/Modules):** `surface-container` (#eaedff) for interactive components.
*   **Level 3 (Floating):** `surface-container-highest` (#dae2fd) for temporary modals or popovers.

### The "Glass & Gradient" Signature
To inject "soul" into the professional aesthetic, apply a subtle **Linear Gradient** (`primary` #005fa0 → `secondary` #006972) to high-impact CTAs and hero decorative elements. Use **Glassmorphism** (semi-transparent `surface` colors with a 12px-20px backdrop-blur) for floating navigation bars to ensure the layout feels integrated and fluid.

---

## 3. Typography: The Editorial Authority
We utilize **Inter** not just for legibility, but as a brand-defining element. 

*   **Display & Headlines:** Use `display-lg` (3.5rem) and `headline-lg` (2rem) with **Bold** weight to create a rhythmic hierarchy. Large headings should be treated as "anchors" for the page, often offset to the left to create asymmetrical interest.
*   **Body & Labels:** Use `body-lg` (1rem) for general content and `body-sm` (0.75rem) for metadata. Keep line-heights generous (1.5x - 1.6x) to maintain a "premium" feel.
*   **The Contrast Rule:** Pair a Bold `title-lg` with a Medium `label-md` in `on_surface_variant` (#404752) to create a sophisticated, high-contrast information architecture.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are largely replaced by **Tonal Layering**.

*   **The Layering Principle:** Instead of adding a shadow to a card, place a `surface-container-lowest` (#ffffff) card on top of a `surface-container-low` (#f2f3ff) background. The 2% shift in brightness provides a cleaner, more modern lift.
*   **Ambient Shadows:** If a floating state is required (e.g., a primary CTA or a Modal), use an extra-diffused shadow: `box-shadow: 0 20px 40px rgba(19, 27, 46, 0.06)`. Note the use of the `on-surface` tint (#131b2e) rather than pure black.
*   **The "Ghost Border" Fallback:** If accessibility requires a stroke, use `outline-variant` (#bfc7d4) at **15% opacity**. Never use 100% opaque borders.

---

## 5. Component Guidelines

### Buttons (The Kinetic Signature)
*   **Primary:** Gradient fill (`primary` to `secondary`), `rounded-md` (0.375rem), white text. 
*   **Secondary:** `surface-container-lowest` fill with a `ghost-border`.
*   **Tertiary:** Text-only, using `primary-container` color for the label, with a subtle underline appearing only on hover.

### Cards & Information Modules
*   **Forbid Divider Lines:** Use vertical white space from the spacing scale (e.g., `spacing-8` or `spacing-12`) to separate content within cards.
*   **Asymmetry:** In hero cards, favor left-aligned text with an image or graphic that slightly breaks the container's "visual boundary" for a custom, non-boxed feel.

### Input Fields
*   **Layout:** Use `surface-container-low` for the input background. No bottom border. Focus states should transition the background to `surface-container-lowest` and add a subtle `primary` glow (2px blur).

### Specialized Components
*   **The "Success Pulse":** Use `tertiary-fixed` (#aff74b) for data visualization and success indicators. It provides a sharp, professional contrast to the deep blues.
*   **Service Chips:** Use `secondary-container` (#54eefe) with `on-secondary-container` (#006972) text for categorization.

---

## 6. Do’s and Don’ts

### Do:
*   **Use White Space as a Tool:** Treat empty space as a luxury feature.
*   **Layer with Intent:** Ensure every "layer" serves a functional purpose in the information hierarchy.
*   **Optical Alignment:** When using large `display-lg` type, align it optically rather than strictly to the grid to maintain visual balance.

### Don’t:
*   **Avoid "Sci-Fi" Tropes:** No glowing lines, no circuit-board patterns, and no robot imagery.
*   **No Heavy Borders:** Never use a solid dark stroke to separate sections.
*   **Limit the Gradient:** Use the primary-to-green gradient sparingly—only for "Success" moments or the most important CTA on the screen to maintain its value.
*   **No Excessive Radii:** Stick to `md` (0.375rem) or `lg` (0.5rem). Avoid fully rounded "pill" buttons unless they are small utility chips.

---

## 7. Spacing & Rhythm
Rhythm is maintained using a strict **4px/8px baseline**. All gaps must be multiples of the spacing scale.
*   **Section Padding:** Standardize on `spacing-24` (6rem) for vertical separation between major page sections to give the content "room to breathe."
*   **Component Internal Padding:** Use `spacing-4` (1rem) for standard cards and `spacing-6` (1.5rem) for featured editorial cards.