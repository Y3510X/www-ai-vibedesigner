# Design System Specification: The Frontier Aesthetic

## 1. Overview & Creative North Star

### Creative North Star: "The Agentic Prism"
This design system is not a static interface; it is a high-performance environment designed for the "Designer from the Future." It rejects the flat, corporate "SaaS-blue" aesthetic in favor of a **Frontier AI Lab** atmosphere—one that feels alive, calculating, and hyper-functional.

We move beyond the "template" look by utilizing **intentional asymmetry** and **tonal depth**. The UI should feel like a sophisticated HUD (Heads-Up Display) projected in a dark space. Elements should overlap, light should bleed from interactive components, and the hierarchy must be driven by luminosity and blur rather than traditional borders or boxes.

---

## 2. Colors & Surface Logic

The color palette is built on a foundation of absolute darkness, punctuated by high-energy light sources.

### Core Palette
*   **Background (`#0e0e0f`):** The void. All interfaces emerge from this deep charcoal/black.
*   **Primary (`#c1fffe`) / Primary Container (`#00ffff`):** The "Neon Cyan" logic. Use for high-action agentic states and primary data points.
*   **Secondary (`#ff51fa`) / Secondary Container (`#a900a9`):** The "Magenta" logic. Reserved for creative overrides, AI suggestions, and high-vibrancy accents.
*   **Tertiary (`#a0ffc4`) / Tertiary Container (`#00fc9d`):** The "Electric Green" logic. Used for system health, "Go" states, and successful computation pulses.

### The "No-Line" Rule
**Explicit Instruction:** 1px solid borders for sectioning are strictly prohibited. 
Boundaries are defined by:
1.  **Background Shifts:** Transitioning from `surface` to `surface-container-low`.
2.  **Luminous Glow:** Using a `0 0 20px` outer glow on an element to define its edge against the dark background.
3.  **Tonal Transitions:** Subtle gradients that bleed from one surface tier to another.

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, semi-transparent layers. 
*   **Base:** `surface` (`#0e0e0f`)
*   **Low-Level Grouping:** `surface-container-low` (`#131314`)
*   **Active Interaction Planes:** `surface-container-highest` (`#262627`) with a 20px backdrop-blur.

### Signature Textures
To achieve the "Frontier Lab" feel, backgrounds should never be truly flat. Implement:
*   **Neural Patterns:** 2% opacity SVG mesh patterns.
*   **Particle Glow:** Fixed-position radial gradients of `primary` and `secondary` at 5% opacity, creating a sense of "atmospheric light" behind the content.

---

## 3. Typography: Technical Authority

We use **Inter** for functional readability and **Space Grotesk** for high-impact technical display.

*   **Display (Space Grotesk):** Large, wide, and commanding. `display-lg` (3.5rem) should be used for hero data points or "Agent Status."
*   **Headline (Space Grotesk):** `headline-md` (1.75rem) provides a clean, monospaced-adjacent feel for section titles.
*   **Body (Inter):** `body-md` (0.875rem) is the workhorse. High tracking (+0.02em) is encouraged to maintain a "technical manual" legibility.
*   **Label (Inter):** `label-sm` (0.6875rem) in All-Caps should be used for metadata, paired with a `0.5` spacing unit for a tight, high-performance look.

---

## 4. Elevation & Depth

In this system, depth is a product of **Light and Refraction**, not shadows.

### The Layering Principle
Avoid traditional drop shadows. Instead, use "Tonal Stacking." An inner card (`surface-container-highest`) placed on a section (`surface-container-low`) creates natural lift. 

### Glassmorphism & Depth
All floating panels (Modals, Popovers, Hover Cards) must use the **Glass Logic**:
*   **Fill:** `surface-variant` at 40% opacity.
*   **Blur:** `backdrop-filter: blur(20px)`.
*   **Edge:** A "Ghost Border" using `outline-variant` at 15% opacity. This mimics the edge of a glass pane catching a stray photon.

### Ambient Glows
When an element is "Active" (e.g., a processing AI agent), apply a pulse effect:
*   `box-shadow: 0 0 30px 2px rgba(0, 255, 255, 0.2);`
*   This replaces the need for thick outlines, allowing the light to define the container.

---

## 5. Components

### Buttons
*   **Primary:** Background `primary_container`, Text `on_primary`. No border. Apply a `0 0 15px` glow of the same color.
*   **Secondary:** `surface-container-high` background with a `ghost-border` (10% opacity white). 
*   **Tertiary:** Text-only in `primary_dim` with a subtle `2px` underline that expands on hover.

### Input Fields
*   **States:** Default state is a `surface-container-lowest` fill. 
*   **Focus:** The background shifts to `surface-bright` and the "Ghost Border" pulses in `primary`. 
*   **Details:** Add a tiny "faint code trace" (e.g., `0x71F...`) in the corner of the input using `label-sm` to lean into the technical aesthetic.

### Cards & Lists
*   **Rule:** No dividers. Separate items using `spacing-4` (1.4rem) or subtle background shifts.
*   **Interactive Cards:** On hover, the background should not just lighten—it should "activate." Use a slight scale (1.02x) and increase the `backdrop-blur` from 20px to 40px.

### Chips
*   **Selection:** High-vibrancy `secondary` fill with `secondary_fixed_dim` text. These should look like glowing neon indicators.

---

## 6. Do’s and Don’ts

### Do:
*   **Use Asymmetry:** Place a large `display-lg` title overlapping a glass container to break the "grid-prison."
*   **Leaning into Darkness:** Ensure at least 80% of the screen real estate is `surface` or `surface-container-lowest`.
*   **Pulse over Blink:** Use slow, 3-second ease-in-out animations for "Processing" states.

### Don’t:
*   **Don't use 100% opaque borders:** They kill the glassmorphism and make the UI feel dated and heavy.
*   **Don't use standard Grey:** If you need a neutral, use a tinted version of the background (`#1a191b`) to maintain the "Deep Space" color temperature.
*   **Don't crowd the UI:** Use the spacing scale (specifically `spacing-8` and `spacing-12`) to give high-intensity neon elements room to "breathe" without overwhelming the user's retina.

---

## 7. Spacing & Geometry
*   **Rounding:** Use `sm` (0.125rem) for technical components (inputs, small buttons) and `xl` (0.75rem) for major containers to create a "Soft-Tech" contrast.
*   **The Grid:** Use an 8px base, but allow elements to "float" off-grid by `spacing-0.5` increments to achieve the intentional, bespoke editorial look.