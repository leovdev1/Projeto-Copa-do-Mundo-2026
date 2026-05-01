# Design System Document: The Global Pitch

## 1. Overview & Creative North Star: "Kinetic Prestige"
The Creative North Star for this design system is **Kinetic Prestige**. This isn't just a sports site; it’s a high-octane editorial experience that mirrors the velocity of the world’s greatest tournament. 

To break the "template" look, we move away from static, centered grids. Instead, we utilize **Intentional Asymmetry**—where headlines may overlap hero imagery, and cards are arranged in an offset, rhythmic flow. The layout should feel like a match in progress: fluid, layered, and high-energy. We achieve this through aggressive typographic scales and "The Layering Principle," ensuring the UI feels like a premium broadcast overlay rather than a standard webpage.

---

## 2. Colors & Surface Architecture
The palette is rooted in the depth of the night stadium (`surface: #090e18`) and ignited by the "Golden Hour" of championship glory (`secondary: #feb700`).

### The "No-Line" Rule
**Explicit Instruction:** Designers are prohibited from using 1px solid borders to define sections. Boundaries must be established through:
*   **Background Shifts:** Transitioning from `surface` to `surface-container-low`.
*   **Tonal Transitions:** Using subtle background-color blocks to cordone content.
*   **Negative Space:** Using the 16 (5.5rem) and 20 (7rem) spacing tokens to create mental boundaries.

### Surface Hierarchy & Nesting
Treat the UI as physical layers of glass and light. 
*   **Base:** `surface` (#090e18) for the main background.
*   **Sections:** Use `surface-container-low` (#0e131e) for large content blocks.
*   **Nesting:** Place `surface-container` (#141a26) cards inside low-tier sections to create natural, soft-edged depth.

### The "Glass & Gradient" Rule
To capture the "Global Energy," use **Glassmorphism** for floating navigational elements or score overlays.
*   **Recipe:** `surface-variant` at 40% opacity + 20px Backdrop Blur.
*   **Gradients:** Hero backgrounds and CTAs should leverage a linear gradient from `primary` (#99b8fe) to `primary-container` (#80a0e4) at a 135-degree angle to simulate stadium lighting.

---

### 3. Typography: The Editorial Voice
We pair the aggressive, italicized momentum of sports journalism with the refined clarity of modern tech.

*   **Display (The Roar):** `display-lg` (Inter, 3.5rem). Use **Bold Italic** for all major headlines. This conveys speed. Apply -2% letter spacing to maintain a tight, "locked-in" feel.
*   **Headlines (The Narrative):** `headline-lg` (Inter, 2rem). Reserved for section starters. Always high-contrast (`on-surface`).
*   **Body (The Detail):** `body-lg` (Plus Jakarta Sans, 1rem). We use Plus Jakarta Sans for its modern, open counters, providing high readability against dark backgrounds.
*   **Labels (The Stats):** `label-md` (Plus Jakarta Sans, 0.75rem, All Caps, Monospaced feel). Used for "Live" tags or player positions.

---

## 4. Elevation & Depth
We eschew traditional drop shadows for **Tonal Layering** and **Ambient Light**.

*   **The Layering Principle:** Depth is achieved by stacking. A `surface-container-highest` element placed on a `surface` background provides all the "lift" required.
*   **Ambient Shadows:** If a card must "float" (e.g., a hovered match card), use a shadow with a 40px blur, 0% spread, and 6% opacity using the `on-primary` color. This creates a "glow" rather than a "shadow."
*   **The Ghost Border:** For accessibility in form fields, use the `outline-variant` (#434854) at **15% opacity**. Never use 100% opaque lines.
*   **Glassmorphism:** Use `surface-bright` with a heavy blur for tactical overlays (e.g., halftime stats) to keep the user connected to the match imagery beneath.

---

## 5. Components

### Buttons
*   **Primary:** `secondary` (#feb700) background with `on-secondary` (#533a00) text. Shape: `md` (0.375rem). Use a subtle inner-glow on top to simulate a 3D tactile feel.
*   **Secondary:** Glassmorphic. `surface-variant` at 20% opacity with a `Ghost Border`.

### Dynamic Cards
*   **Construction:** Forbid dividers. Use `spacing-5` (1.7rem) for internal padding. 
*   **Hover State:** Shift background from `surface-container` to `surface-bright` and apply a 2px vertical lift.
*   **Accents:** Each card should feature a 4px "Nation Strip" at the top using the accent colors: `tertiary` (Mexico Green), `error` (Canada Red), or `primary` (USA Blue).

### Data Visualization (Infographics)
*   **The Pulse:** Use `tertiary-container` (#71f69d) for "positive" stats (Possession, Goals) and `secondary` (#feb700) for "highlight" stats (Speed, Power).
*   **Geometry:** Bars and charts should use `full` (9999px) roundedness for a modern, fluid feel.

### Input Fields
*   **Style:** Minimalist. `surface-container-highest` background, no border, `sm` roundedness. 
*   **Focus:** Transition the background to `surface-bright` and add a `primary` glow.

---

## 6. Do’s and Don’ts

### Do:
*   **Use Overlapping Elements:** Let player photography break the container of a card to create 3D depth.
*   **Embrace High Contrast:** Keep `on-surface` text bright against the deep `surface` colors for elite readability.
*   **Use Large Spacing:** Give the high-energy typography room to breathe using the `spacing-16` and `spacing-24` tokens.

### Don’t:
*   **Don't use 1px Dividers:** Content should be separated by space and color-blocking, not "hairlines."
*   **Don't use Default Italic:** Use the "Bold Italic" weight for headlines; "Light Italic" looks weak and unintentional.
*   **Don't use Pure Black:** Always use `surface` (#090e18). Pure black (#000000) is reserved only for `surface-container-lowest` in specific high-contrast "Void" moments.
*   **Don't mix Roundedness:** Stick to the scale. Use `md` for buttons and `xl` for large cards. Mixing too many radii breaks the professional polish.