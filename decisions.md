# Globetrotter — Decisions Log

## Milestone 0: Setup and Planning
- Destination chosen: San Luis Potosí - chosen because it is the city my parents are from in Mexico
- Primary audience: First-time visitors who want to discover the variety of activities and places in the city
- One design decision that reflects the destination: Using a palette of warm rose/terracotta tones (#A0605F, #C8847E, #D4858D) with desert sand accents (#F5EDE3, #E8D5C4), directly inspired by the cantera rosa (pink volcanic stone) used in the city's colonial buildings
- Wireframe format used (hand-drawn / Figma / other): Digital wireframes created to show navigation placement, content blocks, and responsive layouts for all pages

## Milestone 1: HTML Structure
- **HTML Structure Choice**: Used semantic `<figure>` and `<figcaption>` elements for the photo gallery instead of generic `<div>` containers. This provides proper semantic meaning for image-caption pairs and improves accessibility for screen readers.
- **Claude-Generated Change**: Claude initially generated the attractions page with `<section>` wrappers around each attraction. I changed these to use a consistent `.attraction-card` class structure within a single container for better Flexbox control later.
- **Wireframe-Guided Decision**: The wireframe showed a clear hero section at the top of the home page. This guided the decision to use a full-width `.hero` container with absolute positioning for the overlay text, ensuring the design matched the intended visual hierarchy.

## Milestone 2: CSS Styling
- **Color/Font Choice**: Selected 'Playfair Display' serif font for headings to evoke the baroque elegance of San Luis Potosí's colonial architecture, while pairing it with 'Lato' sans-serif for body text to maintain modern readability. This combination balances the historic character of the destination with contemporary web design standards.
- **Claude Suggestion Rejected**: Claude initially suggested using a bright red accent color for links and buttons. I rejected this because it clashed with the rose-terracotta palette and didn't reflect the subtle elegance of cantera rosa stone. Instead, I used #D4858D (soft rose) for interactive elements.
- **Style Adjustment**: The navigation hover effect initially only changed color. I added a bottom border on hover (`border-bottom: 2px solid #D4858D`) to make the interactive state more visible and improve user feedback, especially on larger screens where the subtle color change wasn't as noticeable.

## Milestone 3: Flexbox Layout
- **Flexbox Property Choice**: Used `flex: 1` with `min-width: 300px` and `max-width: 380px` for gallery items and guide entries. This allows items to grow equally while maintaining readable proportions, and ensures consistent sizing across different screen widths without items becoming too wide or too narrow.
- **Layout Mismatch**: Claude initially generated the preview cards with fixed widths and float positioning. This didn't match the flexible, responsive grid shown in the wireframe. I changed to Flexbox with `flex-wrap: wrap` and flexible item sizing to create the intended fluid layout.
- **HTML Structure Adjustment**: The attractions container initially lacked a wrapper element, making it difficult to apply proper Flexbox layout. I added a `.attractions-container` div with `display: flex` and `flex-direction: column` to properly control spacing and alignment between attraction cards.

## Milestone 4: Responsive Design
- **Breakpoints Used**: Used a single primary breakpoint at `max-width: 768px` for mobile devices. This value was chosen because most of the layout needed only two states: a multi-column desktop view and a stacked mobile view. Tablet sizes (768px-1024px) inherit the desktop styles and scale naturally with the flexible Flexbox layouts.
- **Mobile Layout Difference**: The preview cards section transforms from a side-by-side browsing experience to a vertical feed on mobile. Changed `min-width: 100%` on cards at the mobile breakpoint to force vertical stacking, creating a more intentional scrolling experience suited to one-handed navigation rather than just shrinking the desktop grid.
- **Claude Breakpoint Suggestion**: Claude suggested adding a third breakpoint at 1200px for large desktop screens. I rejected this because the `max-width: 1200px` on the main content container already provides appropriate bounds, and the Flexbox layouts scale well between 768px and ultra-wide screens without needing additional media queries.

## Stretch Features
- **Custom Google Fonts**: Implemented 'Playfair Display' and 'Lato' from Google Fonts to enhance typography and reflect the destination's character.
- **Advanced Hover Effects**: Added CSS transitions with `transform: translateY()` on cards to create subtle lift effects on hover, improving interactivity beyond basic color changes.
- **Box Shadow Depth**: Used multi-level box shadows (`box-shadow: 0 4px 6px` default, `0 12px 20px` on hover) to create depth and visual hierarchy, a property not covered in basic labs.