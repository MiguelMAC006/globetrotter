What location are you building this guide for, and why did you choose it?
- I am building this guide for San Luis Potosí because it is the city that my parents are from in Mexico.

Who is your primary audience? (e.g., first-time visitors, backpackers, families, local residents)
- My primary audience is first-time visitors.

What do you want visitors to feel or know after spending 5 minutes on your site?
- I want my visitors to feel that there is a variety of activities and places to visit in my city and would want to visit there.

What's one design decision — color, layout, or tone — that reflects your destination's identity?
- San Luis Potosí is famous for its pink volcanic stone (cantera rosa) used in colonial buildings. One decision that reflects this could be using a palette of warm rose/terracotta tones with desert sand accents, reflecting those iconic baroque facades and the surrounding high desert landscape.

## Design Intent

What color palette reflects your destination? Name three words that describe the feeling.
- The color palette uses warm rose (#A0605F, #C8847E, #D4858D) and desert sand tones (#F5EDE3, #E8D5C4) inspired by the cantera rosa stone. Three words: elegant, warm, historic.

What typography (heading font / body font) fits your destination's character?
- Headings use 'Playfair Display' (serif) to evoke colonial baroque architecture and elegance. Body text uses 'Lato' (sans-serif) for modern readability and clean presentation.

What's one visual choice that connects to your destination's identity?
- The rose-terracotta color scheme directly references the pink volcanic stone used in San Luis Potosí's iconic colonial buildings, creating an immediate visual connection to the city's architectural identity.

## Flexbox Layout Plan

**Header & Navigation:**
- Navigation links arranged horizontally in a single row on desktop using Flexbox with consistent gap spacing.
- On mobile (below 768px), header stacks vertically and navigation wraps with centered alignment.

**Hero Section:**
- Full-width image with centered, overlaid text using Flexbox positioning.
- Height adjusts from 300px (desktop) to 250px (mobile).

**Preview Cards (Home Page):**
- Three preview cards arranged horizontally in a row on desktop with equal flex sizing.
- Cards wrap to full width on mobile, stacking vertically.
- Each card maintains consistent internal spacing and hover effects.

**Attractions & Food Guide:**
- Desktop: Items arranged using Flexbox wrap, displaying 2-3 items per row depending on available space.
- Mobile: All items stack to full width for easier reading.
- Consistent spacing between all items using gap property.

**Photo Gallery:**
- Gallery items arranged using Flexbox wrap, displaying 3 items per row on desktop.
- Mobile: Items stack to full width (100%).
- Each figure maintains consistent sizing and spacing.

**Footer:**
- Footer links arranged horizontally using Flexbox with centered alignment.
- Links wrap naturally on smaller screens.

## Breakpoints Plan

What are the three device sizes you're designing for, and what width defines each breakpoint?
- Mobile: 320px - 767px (primary breakpoint at max-width: 768px)
- Tablet: 768px - 1023px (inherits desktop styles, scales naturally)
- Desktop: 1024px and above (default styles)

For each major section of your site, what needs to change at each breakpoint?
- **Header/Navigation**: Desktop has horizontal layout with items side-by-side. Mobile stacks vertically with wrapped, centered navigation.
- **Hero**: Desktop shows 300px height. Mobile reduces to 250px with smaller text (2rem → 1.5rem).
- **Preview Cards/Gallery/Guide**: Desktop shows 2-3 items per row with flexible widths. Mobile forces all cards to 100% width, stacking vertically.
- **Typography**: Main headings scale down from 2.5rem to 2rem on mobile for better readability.
- **Spacing**: Content gaps reduce from 2rem to 1.5rem on mobile to maximize screen real estate.

Are there any sections where the mobile experience should feel meaningfully different from desktop, not just smaller?
- Yes, the preview cards and gallery sections transform from a multi-column browsing experience on desktop to a focused, scrollable feed on mobile. This creates a more intentional, story-like experience suited to one-handed mobile navigation rather than just shrinking the desktop layout.