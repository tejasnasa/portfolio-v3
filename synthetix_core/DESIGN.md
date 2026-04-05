# Design System Specification: The Engineering Editorial

## 1. Overview & Creative North Star
**Creative North Star: "The Architectural Void"**

This design system moves away from the "busy" clutter of typical developer portfolios. It is built on the philosophy of **Architectural Void**—where the vastness of the deep background (#0A0A0A) represents the clean slate of a backend environment, and the UI elements are the precise, high-performance structures built within it. 

To break the "template" look, we utilize **Intentional Asymmetry**. Instead of a standard centered grid, we lean into wide-margin editorial layouts, where oversized headlines (Display-LG) crash against technical, small-scale labels. This system isn't just a portfolio; it’s a high-end technical product interface that feels both authoritative and ethereal.

---

## 2. Colors & Surface Philosophy
The palette is rooted in a "Deep Space" spectrum, utilizing the contrast between absolute blacks and high-energy luminescent accents.

### Color Tokens
- **Background:** `#131313` (Main canvas)
- **Surface (Primary):** `#131313`
- **Surface Container Highest:** `#353534` (Used for floating glass elements)
- **Primary (Cyber-Blue):** `#a4e6ff`
- **Secondary (Neon-Purple):** `#ecb2ff`
- **Tertiary (Technical Amber):** `#ffd59c`

### The "No-Line" Rule
Traditional 1px solid borders are strictly prohibited for layout sectioning. Visual separation must be achieved through **Tonal Shifts**. 
*   **Example:** A `surface-container-low` section sitting directly on the `background` creates a soft, sophisticated transition that feels like a natural part of the environment rather than a "box."

### Surface Hierarchy & Nesting
Treat the UI as a series of stacked, semi-transparent layers. 
1.  **Level 0:** `background` (#131313) – The base floor.
2.  **Level 1:** `surface-container-low` (#1c1b1b) – Secondary sections or content wells.
3.  **Level 2:** `surface-container-highest` (#353534) with `backdrop-blur(12px)` – Primary cards and navigation modules.

### The "Glass & Gradient" Rule
To achieve the "Tech Product" aesthetic, all primary interactive containers must use **Glassmorphism**. 
*   **Formula:** `background: rgba(53, 53, 52, 0.4)` + `backdrop-filter: blur(16px)`.
*   **Signature Textures:** Apply a `radial-gradient` (20% opacity) of `primary` or `secondary` in the corners of cards to simulate a "system glow" or "status light" within the hardware.

---

## 3. Typography
The system utilizes a dual-font strategy: **Space Grotesk** for structural impact and **Inter** for technical readability.

*   **Display (Space Grotesk):** Set to `-0.04em` tracking. These are the "Hero" moments. Use `display-lg` (3.5rem) to dominate the viewport.
*   **Headlines (Space Grotesk):** Bold, high-contrast. Use these to define technical architecture sections.
*   **Body (Inter):** High-contrast `on-surface` text. Use `body-md` (0.875rem) for most technical descriptions to maintain a "dense, data-rich" engineering feel.
*   **Labels (Inter):** All-caps, slightly tracked out (+0.1em). Use `label-sm` for metadata like "TECH STACK" or "BUILD TIME."

---

## 4. Elevation & Depth

### The Layering Principle
Avoid "drop shadows" that look like dark smudges. Instead, use **Tonal Layering**. Place a `surface-container-highest` element over a `surface-container-lowest` background. The difference in tonal value provides the "lift."

### Ambient Shadows
For floating elements (Modals, Nav), use a **Tinted Ambient Shadow**:
*   `box-shadow: 0 20px 40px rgba(0, 103, 127, 0.08);` (A subtle blue-tinted shadow that feels like light leaking from the screen).

### The "Ghost Border" Fallback
Where containment is required for accessibility, use a **Ghost Border**:
*   `border: 1px solid rgba(133, 147, 153, 0.15);` (Outline-variant at low opacity). This ensures the "Glass" effect feels thin and high-precision.

---

## 5. Components

### Buttons
*   **Primary:** `primary` background with `on-primary` text. No border. Subtle `primary-container` glow on hover.
*   **Secondary (The Glass Button):** Transparent background, `backdrop-blur(8px)`, and a 1px `Ghost Border`.
*   **States:** On hover, primary buttons should "breathe"—a soft, 4px expansion of the glow.

### Input Fields
*   **Style:** Minimalist. No background fill, only a bottom-border using `outline-variant`.
*   **Active State:** The bottom border transitions to a `primary` cyber-blue gradient. Label shifts to `label-sm` in `primary` color.

### Cards & Lists
*   **Rule:** Forbid the use of divider lines. 
*   **Implementation:** Separate list items using 12px of vertical white space. Use a `surface-container-low` background on hover to highlight the active row.
*   **Engineering Component:** **Code Blocks.** Use `surface-container-lowest` as the background, with a `primary` (blue) glow on the top-left edge to indicate "Active Terminal."

### Navigation (The Floating Dock)
The main navigation should be a floating "Dock" at the bottom or top center.
*   **Style:** `surface-container-highest` + `backdrop-blur(20px)` + `Rounded-XL`. It should look like a piece of polished hardware floating in the void.

---

## 6. Do's and Don'ts

### Do:
*   **Do** use extreme white space. Engineering "Density" should come from the typography, not from cramming boxes together.
*   **Do** use `primary` and `secondary` gradients as "background atmosphere" (large, blurry blobs behind cards).
*   **Do** treat your code snippets with the same editorial care as your headlines.

### Don't:
*   **Don't** use 100% white (#FFFFFF). Always use `on-surface` (#e5e2e1) to prevent eye strain in dark mode.
*   **Don't** use sharp corners for glass elements. Always use the `xl` (0.75rem) or `lg` (0.5rem) roundedness to soften the "Cyber" look into something "Premium."
*   **Don't** use standard "Slide-in" animations. Use "Fade and Scale" (from 98% to 100%) to mimic a high-end OS booting up.