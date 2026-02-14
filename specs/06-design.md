# 06. Design: Visual Specifications for The CKB Firm Website

This document outlines the core design elements, visual tokens, and component specifications that will define the award-winning aesthetic of The CKB Firm's digital rebirth. The goal is to convey sophistication, trust, clarity, and modern professionalism.

## I. Design Tokens

### A. Colors

The color palette is refined from the existing brand, evolving traditional legal tones into a contemporary, authoritative, and approachable scheme.

*   **Primary Brand Colors:**
    *   **Deep Midnight Blue:** `#1A2C4A` (RGB: 26, 44, 74)
        *   *Usage:* Main headings, primary buttons, navigation background, footer background, key graphic elements. Evokes trust, stability, professionalism.
    *   **Regal Crimson:** `#C13B5C` (RGB: 193, 59, 92)
        *   *Usage:* Accent color for CTAs, interactive elements (links on hover), key callouts, subtle graphic details. Adds dynamism and distinction.
*   **Neutral Palette:**
    *   **Charcoal Black (Text):** `#2C2C2C` (RGB: 44, 44, 44)
        *   *Usage:* Primary body text, secondary headings. Ensures maximum readability and a premium feel.
    *   **Mid-Tone Slate (Secondary Text/Borders):** `#6A7B8C` (RGB: 106, 123, 140)
        *   *Usage:* Sub-headings, meta-information, disabled states, subtle borders.
    *   **Light Grey (Subtle Background/Dividers):** `#E8EDF2` (RGB: 232, 237, 242)
        *   *Usage:* Subtle section backgrounds, form field borders, dividers.
    *   **Soft Cloud (Alternate Background):** `#F8F9FA` (RGB: 248, 249, 250)
        *   *Usage:* Background for cards, testimonials, or alternate section backgrounds.
    *   **Pure White:** `#FFFFFF` (RGB: 255, 255, 255)
        *   *Usage:* Main content background, card backgrounds. Provides clean, open space.
*   **System/Feedback Colors:**
    *   **Success Green:** `#4CAF50` (RGB: 76, 175, 80)
        *   *Usage:* Form success messages, positive feedback.
    *   **Error Red:** `#EF5350` (RGB: 239, 83, 80)
        *   *Usage:* Form error messages, validation feedback.

### B. Typography

A sophisticated pairing of a classic serif for headlines and a modern sans-serif for body text, ensuring both gravitas and clarity.

*   **Headings Font:** **Playfair Display** (Serif)
    *   *Usage:* H1, H2, H3, H4, prominently for section titles and hero text.
    *   *Rationale:* Elegant, authoritative, and evokes a sense of tradition with a modern twist.
    *   **H1:** `4.5rem` (72px) / `line-height: 1.1` / `font-weight: 700` / `letter-spacing: -0.02em` (Desktop)
        *   `3rem` (48px) (Tablet)
        *   `2.25rem` (36px) (Mobile)
    *   **H2:** `3.5rem` (56px) / `line-height: 1.2` / `font-weight: 700` / `letter-spacing: -0.01em` (Desktop)
        *   `2.5rem` (40px) (Tablet)
        *   `2rem` (32px) (Mobile)
    *   **H3:** `2.5rem` (40px) / `line-height: 1.3` / `font-weight: 700` (Desktop)
        *   `2rem` (32px) (Tablet)
        *   `1.75rem` (28px) (Mobile)
    *   **H4:** `1.75rem` (28px) / `line-height: 1.4` / `font-weight: 700` (Desktop)
        *   `1.5rem` (24px) (Tablet)
        *   `1.25rem` (20px) (Mobile)
    *   **H5:** `1.25rem` (20px) / `line-height: 1.5` / `font-weight: 600`
    *   **H6:** `1rem` (16px) / `line-height: 1.6` / `font-weight: 600`
*   **Body Font:** **Inter** (Sans-serif)
    *   *Usage:* Body text, navigation links, button text, forms, captions, attorney bios.
    *   *Rationale:* Highly readable, modern, and clean, providing excellent contrast to Playfair Display.
    *   **Body Large:** `1.125rem` (18px) / `line-height: 1.6` / `font-weight: 400`
    *   **Body Regular:** `1rem` (16px) / `line-height: 1.6` / `font-weight: 400`
    *   **Body Small:** `0.875rem` (14px) / `line-height: 1.5` / `font-weight: 400`
    *   **Links:** Inherit body font, `font-weight: 500`, `color: #1A2C4A`, `text-decoration: underline` on hover.

### C. Spacing

A consistent 8px grid system for all spacing, ensuring harmony and precision.

*   **Base Unit:** `8px`
*   **Small:** `8px` (e.g., icon-text spacing, small button padding)
*   **Medium:** `16px` (e.g., component internal padding, card gaps)
*   **Large:** `24px` (e.g., section internal padding, larger component gaps)
*   **X-Large:** `32px` (e.g., vertical rhythm between content blocks)
*   **XX-Large:** `48px` (e.g., larger section gaps)
*   **XXX-Large:** `64px` (e.g., hero section top/bottom padding)
*   **Page Margin (Desktop):** `80px` left/right for main content container.
*   **Page Margin (Tablet):** `40px` left/right.
*   **Page Margin (Mobile):** `24px` left/right.

### D. Borders & Shadows

Subtle, professional, and indicative of interactive elements.

*   **Border Radius:** `4px` (for buttons, input fields, cards – minimal roundness for sophistication).
*   **Border Color:** `#D1D9E0` (RGB: 209, 217, 224) for default inputs, card outlines.
*   **Focus Ring:** `2px solid #C13B5C` with `4px` offset (for accessibility).
*   **Box Shadow (Subtle Lift):** `0px 4px 12px rgba(0, 0, 0, 0.08)` (for cards on hover, modals).

## II. Component Specifications

### A. Buttons

*   **Primary Button:**
    *   *Background:* `Deep Midnight Blue` (`#1A2C4A`)
    *   *Text:* `Pure White` (`#FFFFFF`)
    *   *Border:* `none`
    *   *Padding:* `16px 32px`
    *   *Font:* Inter, `1rem` (16px), `font-weight: 600`
    *   *Hover:* Background `#2E4878` (darker blue), subtle `box-shadow` `0px 4px 12px rgba(0, 0, 0, 0.12)`.
    *   *Active:* Background `#0E1B32` (even darker blue).
*   **Secondary Button:**
    *   *Background:* `Pure White` (`#FFFFFF`)
    *   *Text:* `Deep Midnight Blue` (`#1A2C4A`)
    *   *Border:* `1px solid #1A2C4A`
    *   *Padding:* `16px 32px`
    *   *Font:* Inter, `1rem` (16px), `font-weight: 600`
    *   *Hover:* Background `#F8F9FA` (Soft Cloud), Border `1px solid #2E4878`.
    *   *Active:* Background `#E8EDF2` (Light Grey).
*   **Ghost Button:**
    *   *Background:* `transparent`
    *   *Text:* `Deep Midnight Blue` (`#1A2C4A`)
    *   *Border:* `1px solid #D1D9E0`
    *   *Padding:* `16px 32px`
    *   *Font:* Inter, `1rem` (16px), `font-weight: 600`
    *   *Hover:* Background `#F8F9FA` (Soft Cloud), Border `1px solid #6A7B8C`.
    *   *Active:* Background `#E8EDF2` (Light Grey).

### B. Form Fields

*   **Input/Textarea/Select:**
    *   *Background:* `Pure White` (`#FFFFFF`)
    *   *Text:* `Charcoal Black` (`#2C2C2C`)
    *   *Border:* `1px solid #D1D9E0`
    *   *Padding:* `12px 16px`
    *   *Font:* Inter, `1rem` (16px), `font-weight: 400`
    *   *Placeholder Text:* `Mid-Tone Slate` (`#6A7B8C`)
    *   *Focus State:* `Border: 1px solid #1A2C4A`, `box-shadow: 0 0 0 2px rgba(26, 44, 74, 0.2)`.
    *   *Error State:* `Border: 1px solid #EF5350`.

### C. Navigation

*   **Global Navigation (Desktop):**
    *   *Background:* `Deep Midnight Blue` (`#1A2C4A`)
    *   *Link Text:* `Pure White` (`#FFFFFF`)
    *   *Link Font:* Inter, `1rem` (16px), `font-weight: 500`
    *   *Link Hover:* `text-decoration: underline`, or subtle `background-color: rgba(255, 255, 255, 0.1)`.
    *   *Active Link:* `font-weight: 700`, `border-bottom: 2px solid #C13B5C`.
    *   *CTA Button in Nav:* Primary button style.
*   **Dropdown/Mega Menu:**
    *   *Background:* `Pure White` (`#FFFFFF`)
    *   *Link Text:* `Charcoal Black` (`#2C2C2C`)
    *   *Link Hover:* `background-color: #F8F9FA` (Soft Cloud), `text-decoration: none`.
    *   *Border:* `1px solid #D1D9E0`.
    *   *Box Shadow:* `0px 8px 24px rgba(0, 0, 0, 0.1)`.

### D. Cards (Service, Attorney, Article)

*   **Background:** `Pure White` (`#FFFFFF`) or `Soft Cloud` (`#F8F9FA`) for alternating sections.
*   **Border:** `1px solid #E8EDF2`.
*   **Border Radius:** `4px`.
*   **Padding:** `24px`.
*   **Hover State (for interactive cards):** Subtle `box-shadow: 0px 4px 12px rgba(0, 0, 0, 0.08)`, `transform: translateY(-2px)`.

### E. Hero Sections

*   **Structure:** Full-width, often with a large background image or gradient overlay.
*   **Text Alignment:** Centered or left-aligned depending on content and visual balance.
*   **Headline/Sub-headline:** `Playfair Display` for headlines, `Inter` for sub-headlines, `Pure White` (`#FFFFFF`) or `Deep Midnight Blue` (`#1A2C4A`) depending on background contrast.
*   **CTAs:** Primary and/or Secondary buttons.

### F. Iconography

*   **Style:** Minimalist, line-art, sophisticated.
*   **Color:** `Deep Midnight Blue` (`#1A2C4A`) or `Pure White` (`#FFFFFF`) depending on background.
*   **Usage:** To visually reinforce section themes, services, or callouts.

## III. Animation Guidelines

Animations should be subtle, purposeful, and enhance the user experience without distracting.

*   **Transitions:**
    *   *Property:* `all` (or specific properties like `background-color`, `transform`, `opacity`)
    *   *Duration:* `0.2s` to `0.3s`
    *   *Timing Function:* `ease-out` (for smooth deceleration).
*   **Hover Effects:** Gentle `transform: translateY(-2px)` for cards, `background-color` changes for buttons/links.
*   **Page Transitions:** Subtle fade-ins or slide-ups for content on page load, if performance allows, to feel polished.
*   **Scroll-triggered Animations:** Minimal, such as elements fading in or sliding up slightly as they enter the viewport, to add a dynamic touch. Avoid excessive or heavy animations that impact performance.

## IV. Responsive Breakpoints

Standard breakpoints will be used to ensure optimal display across devices.

*   **Desktop Large:** `min-width: 1440px`
*   **Desktop:** `min-width: 1024px` (Base for main design)
*   **Tablet:** `min-width: 768px` and `max-width: 1023px`
*   **Mobile Large:** `min-width: 480px` and `max-width: 767px`
*   **Mobile Small:** `max-width: 479px`

This design specification provides a robust framework for creating a visually stunning, highly functional, and award-winning website that truly reflects the reborn identity of The CKB Firm.