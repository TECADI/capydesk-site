# Design System Documentation: The Modern Executive Editorial

## 1. Overview & Creative North Star
The design system is built upon a Creative North Star titled **"The Empathetic Architect."** 

In the B2B SaaS world, "Enterprise-grade" often translates to rigid, cold, and monochromatic layouts. This system breaks that convention. We aim to balance the high-stakes reliability of deep tech with the serene, approachable nature of the capybara. The experience is designed to feel like an upscale editorial magazine: authoritative yet breathable, structured yet organic. 

By utilizing intentional asymmetry, sophisticated tonal layering, and high-contrast typography, we move away from "boxed-in" UI toward an expansive, premium digital environment.

---

## 2. Colors & Surface Philosophy

The color strategy leverages a deep tech foundation punctuated by vibrant, character-rich highlights.

### The Palette
*   **Primary (`#002045`):** The "Executive Blue." Used for foundational elements and high-authority text.
*   **Primary Container (`#1A365D`):** The deep tech indigo used for large brand moments.
*   **Secondary (`#13696A` / Teal):** Represents action and precision.
*   **Tertiary (`#F8BC4B` / Amber):** The warmth of the mascot. Used sparingly for high-attention alerts or "delight" moments.
*   **Background (`#FAF9FD`):** A soft, off-white lavender-tinted base to reduce eye strain and feel more premium than pure white.

### The "No-Line" Rule
To achieve a high-end feel, **1px solid borders for sectioning are strictly prohibited.** We define space through background shifts. 
*   A side navigation might sit on `surface-container-low` while the main content area resides on `surface`.
*   Floating panels use `surface-container-lowest` (pure white) to contrast against the `background`.

### Surface Hierarchy & Nesting
Treat the UI as a series of physical layers. 
*   **Base:** `surface` (#FAF9FD)
*   **Recessed Sections:** `surface-container` (#EFEDF1)
*   **Elevated Cards:** `surface-container-lowest` (#FFFFFF)
*   **Hover/Active States:** `surface-container-high` (#E9E7EB)

### The "Glass & Gradient" Rule
For hero sections and primary CTAs, avoid flat fills. Use a subtle linear gradient from `primary` to `primary_container` (at a 135-degree angle) to add depth. For floating overlays, implement **Glassmorphism**: 
*   **Fill:** `surface_variant` at 60% opacity.
*   **Effect:** Backdrop blur of 12px-20px. 
This ensures the mascot and background textures "bleed through" the UI, making it feel integrated and custom.

---

## 3. Typography: Editorial Authority

We use a dual-typeface system to bridge the gap between "Professional" and "Approachable."

*   **Display & Headlines (Plus Jakarta Sans):** Chosen for its modern, geometric curves and open counters. It reflects the friendly roundness of the capybara while maintaining a clean, tech-forward edge. Use `display-lg` for impactful hero statements to establish an editorial hierarchy.
*   **Body & Titles (Inter):** The industry standard for legibility. Used for all functional data and long-form reading to ensure the "Enterprise-grade" promise of clarity.

**The Signature Scale:** Use extreme contrast between `display-lg` (3.5rem) and `label-md` (0.75rem). This high-contrast ratio is the hallmark of premium design, moving away from the "medium-size-fits-all" approach of generic SaaS.

---

## 4. Elevation & Depth

Depth in this system is a result of light and shadow, not lines and boxes.

### The Layering Principle
Rather than shadows, use **Tonal Layering**. Place a `surface-container-lowest` card on a `surface-container-low` background. This creates a "soft lift" that feels architectural rather than digital.

### Ambient Shadows
When an element must float (e.g., a dropdown or a primary mascot card), use the **Ambient Shadow**:
*   **Color:** `on-surface` (#1A1C1E) at 4% to 8% opacity.
*   **Blur:** 24px to 40px.
*   **Offset:** Y: 8px.
This mimics natural light and avoids the "muddy" look of standard 90s-era drop shadows.

### The "Ghost Border" Fallback
If accessibility requires a container boundary, use a **Ghost Border**: `outline-variant` (#C4C6CF) at 15% opacity. It provides a hint of structure without interrupting the visual flow of the whitespace.

---

## 5. Components

### Buttons
*   **Primary:** Gradient fill (`primary` to `primary_container`), `lg` roundedness (1rem), and `title-sm` (Inter Semi-bold) text. 
*   **Secondary:** Teal (`secondary`) text on a `secondary_container` background. No border.
*   **Tertiary:** Ghost style. `on-surface` text. Only visible on hover via a `surface-container-high` background shift.

### Input Fields
*   **Structure:** No heavy borders. Use `surface-container-highest` as a subtle fill.
*   **Focus State:** A 2px `secondary` (Teal) bottom-bar animation or a "Ghost Border" at 40% opacity. 
*   **Roundedness:** `DEFAULT` (0.5rem) to keep them feeling professional but tactile.

### Cards & Lists
*   **Forbid Dividers:** Do not use horizontal lines between list items. Use `spacing-4` (1.4rem) of vertical whitespace or alternating `surface` and `surface-container-low` background tints.
*   **The Mascot Integration:** Use the mascot ({{DATA:IMAGE:IMAGE_1}}) as a "Contextual Guide." Place the mascot partially overlapping the edge of empty-state cards or dashboard welcome headers to break the rigid grid and add brand personality.

### Signature Component: The "Capy-Tray"
A bottom-anchored, glassmorphic slide-out panel for quick actions. It uses `surface_container_lowest` with 70% opacity and a heavy backdrop blur, allowing the dashboard data to remain visible behind the "frosted" interface.

---

## 6. Do’s and Don'ts

### Do
*   **DO** use white space as a structural element. If a layout feels cluttered, increase the spacing to `spacing-8` (2.75rem).
*   **DO** use the `lg` (1rem) corner radius for large containers to echo the friendly curves of the brand mascot.
*   **DO** use the teal (`secondary`) color for data visualization and success states—it’s our "action" color.

### Don’t
*   **DON'T** use 1px black or grey borders. They feel cheap and "template-like."
*   **DON'T** center-align everything. Use intentional left-aligned typography with asymmetric image placement to maintain the editorial feel.
*   **DON'T** use the mascot as a watermark. It should be a crisp, high-contrast element that interacts with the UI (e.g., "peeking" over a card).
*   **DON'T** use pure black (#000000). Always use `on-background` (#1A1C1E) for high-contrast text to keep the palette sophisticated.