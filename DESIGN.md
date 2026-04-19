# Design System: Warm Prestige Editorial

## 1. Overview & Creative North Star
**Creative North Star: The Sovereign Curator**
This design system rejects the clinical, "tech-first" aesthetic of typical property apps in favor of a "High-End Editorial" experience. It treats student housing not as a commodity, but as a lifestyle curation. We break the "template" look through **intentional asymmetry**, high-contrast typography scales, and a departure from rigid grid containers. The UI should feel like a premium West African architectural digest—authoritative, warm, and deeply rooted in contemporary Nigerian excellence.

**The signature is "Soft Power":** bold enough to be energetic (Bold Modernism), yet refined enough to command trust (Premium).

---

## 2. Color & Tonal Depth
The palette is built on "Warm Prestige"—eschewing the cold greys of Silicon Valley for deep, earthen tones and golden highlights.

### The Palette Roles
- **Primary & Containers:** `primary` (#00281c) and `primary_container` (#00402e) act as the anchor. They provide the "Forest Green" depth that signifies stability and growth.
- **Secondary (The Pulse):** `secondary` (#944925) and its variants provide the Terracotta energy. Use these for interactive moments that require "heat" and urgency.
- **Tertiary (The Glow):** `tertiary` (#735c00) and `tertiary_fixed` (#ffe088) are your Champagne/Gold accents. These are reserved for prestige markers like "Verified" status or premium listings.

### The "No-Line" Rule
**Explicit Instruction:** Do not use 1px solid borders to section content. Boundaries must be defined solely through background color shifts. Use `surface_container_low` for sections sitting on a `surface` background. If a container needs to stand out, move up the tier to `surface_container_high`. We define space through mass, not lines.

### The "Glass & Gradient" Rule
To avoid a flat, "out-of-the-box" look:
- **Floating Elements:** Use `surface_container_lowest` at 80% opacity with a 20px `backdrop-blur`.
- **Hero CTAs:** Apply a subtle linear gradient from `primary` to `primary_container` (135°) to give buttons a three-dimensional "soul."

---

## 3. Typography: Assertive Editorial
We use **Manrope** exclusively, but we manipulate its weight and scale to create a "Voice."

- **Display (The Statement):** `display-lg` (3.5rem) in ExtraBold. Use this for hero value propositions. Use tight letter-spacing (-0.02em) to emphasize the "Bold Modernism."
- **Headlines (The Anchor):** `headline-lg` through `sm` in ExtraBold. These should feel heavy and permanent.
- **Body (The Narrative):** `body-lg` (1rem) in Regular or Medium. Maintain a generous line-height (1.6) to ensure the "Warmth" translates to readability.
- **Prestige Labels:** `label-md` (0.75rem) should always be in All-Caps with +0.05em tracking when used for "Verified" badges or "Exclusive" tags.

---

## 4. Elevation & Depth: Tonal Layering
Traditional drop shadows are too "digital." We use **Ambient Depth**.

- **The Layering Principle:** Stack `surface-container` tiers. 
    - *Example:* A `surface-container-lowest` card (Pure White) should sit on a `surface-container-low` (Warm Off-white) background. This creates a natural, soft lift.
- **Ambient Shadows:** If a card must float, use a shadow with a 40px blur, 0px offset, and 6% opacity, tinted with the `on-surface` color (#1c1c18). It should look like a glow of shadow, not a hard edge.
- **Signature Textures:** Within `primary_container` surfaces, overlay a 3% opacity geometric Adire pattern. This texture should be "felt, not seen"—a tactile layer that adds cultural prestige.

---

## 5. Components

### Buttons (The Statement Pieces)
- **Primary:** `primary` background, `on_primary` text. Use `xl` (0.75rem) roundedness for a modern, approachable feel. No borders.
- **Secondary:** `secondary_container` background with `on_secondary_container` text. This is for high-energy actions (e.g., "Book Now").
- **Ghost (Tertiary):** No background, `primary` text. Underline on hover only.

### Cards & Property Lists
- **Rule:** Forbid divider lines. Separate property features (beds, baths, price) using `3` (1rem) spacing scale increments.
- **Verified Landlord Badge:** A `tertiary_fixed` container with a subtle `secondary` icon. It should feel like a gold wax seal.
- **Status Indicators (Roommate Matching):** Use `secondary_fixed` for "Looking" and `primary_fixed` for "Matched." These should be pill-shaped (`full` roundedness) with `label-sm` typography.

### Input Fields
- **Surface:** Use `surface_variant` backgrounds. 
- **The Ghost Border:** If an input requires a boundary, use `outline_variant` at 20% opacity. 
- **States:** On focus, transition the background to `surface_container_lowest` and add a 2px `primary` bottom-border only (Editorial style).

### Specialized Components
- **The "Curated" Carousel:** Use asymmetrical image sizing (e.g., a large vertical image followed by two smaller stacked horizontal images) to break the "standard app" feel.
- **Ankara Overlay:** Use a decorative `primary_container` element with a low-opacity Adire pattern at the edge of hero sections to anchor the eye.

---

## 6. Do’s and Don’ts

### Do
- **Do** use `surface_container_highest` for "sticky" navigation bars with a backdrop blur.
- **Do** use large, high-fashion imagery of West African students in collaborative, high-end environments (Lekki/Abuja aesthetics).
- **Do** allow typography to overlap image containers slightly to create a sense of depth and "Editorial" layout.

### Don't
- **Don't** use pure black (#000000). Always use `on_surface` (#1c1c18) for text.
- **Don't** use standard 1px grey dividers. If you need a separator, use a 8px height block of `surface_container_low`.
- **Don't** use cool-toned blues or teals. If the UI feels "cold," increase the use of `secondary` (Terracotta) or `background` (Warm White).
- **Don't** cram content. Use the `8` (2.75rem) or `10` (3.5rem) spacing tokens to let the "Prestige" breathe.