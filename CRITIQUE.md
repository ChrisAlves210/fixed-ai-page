# Design Critique: TruckTrack

## What Works

- The headline and supporting copy make the food-truck tracking purpose clear at a glance.
- The truck listings use a consistent layout and include useful details such as cuisine, distance, and whether a truck is open.

## 7-Pass Critique

### 1. Squint

- **Observation:** The desktop hero is a large blue-purple gradient with centered white copy and one prominent button; the same gradient returns in the signup section. **Impact:** The repeated treatment makes the page feel like a generic landing-page template and gives less visual priority to the actual trucks. **Fix:** Give the hero and signup distinct roles; let truck photography or a location preview become the strongest visual after the headline.
- **Observation:** The six truck images are represented by food emoji over bright pink gradient blocks. **Impact:** The listings read as placeholders rather than real nearby businesses, making it harder to judge the food and trust the directory. **Fix:** Use consistent, well-cropped food-truck or dish photography and a neutral image background.

### 2. Alignment

- **Observation:** On desktop, the six truck cards form three columns; on mobile, they become one column. The card contents are consistently left-aligned while the section headings are centered. **Impact:** The cards are easy to scan, but the centered section headings do not share the cards' left edge and feel detached from the list. **Fix:** Align each section heading with the grid's left edge, or use a consistent centered container for both heading and cards.
- **Observation:** At 375px, the brand occupies a centered header row and the three navigation links occupy a second row. **Impact:** Navigation takes extra vertical space before the main task begins. **Fix:** Keep the brand and a compact menu control on one row, or simplify the mobile navigation to the highest-priority destination.

### 3. Spacing

- **Observation:** The mobile screenshot is 4,867px tall, and the six truck cards stack in a single column with large image areas. **Impact:** Visitors must scroll through repeated, tall cards to compare nearby options. **Fix:** Reduce mobile image height and vertical card padding, and consider a compact list layout for narrow screens.
- **Observation:** The mobile hero is about 600px tall before the first content section starts. **Impact:** A visitor sees only the hero on initial load, delaying access to the truck listings. **Fix:** Reduce hero min-height and vertical padding at narrow breakpoints so the next section begins sooner.
- **Observation:** Each truck card gives its image roughly half the card's height, while the name, distance, and status are grouped below it. **Impact:** Repeated image space pushes useful comparison details farther down the page. **Fix:** Shorten the image area and tighten the card's internal spacing, especially on mobile.

### 4. Type

- **Observation:** The page uses a bold sans-serif style for the headline, section headings, card titles, and buttons, with relatively little change in typographic character. **Impact:** The hierarchy relies mostly on size and color, so the page feels less distinctive and the sections compete. **Fix:** Establish a small type scale with a clear display-heading treatment and consistent body and metadata sizes.
- **Observation:** The desktop hero headline stretches across almost the entire 1280px viewport on one line, while the mobile version breaks into three centered lines. **Impact:** The desktop line is difficult to take in as a phrase, and the mobile headline occupies much of the first screen. **Fix:** Set a deliberate maximum line length and tune the heading size and line breaks at the mobile breakpoint.
- **Observation:** Truck cuisine and distance metadata are smaller and lighter than the truck names and status pills. **Impact:** Important comparison details are easy to overlook, especially for visitors with low vision. **Fix:** Increase metadata contrast and keep its text size comfortably readable.

### 5. Color

- **Observation:** Blue-purple gradients dominate both the hero and signup sections, and pink gradients dominate every truck image block. **Impact:** Color is decorative rather than communicating product state or supporting a food-focused identity. **Fix:** Use a restrained brand palette and reserve distinct status colors for open and closed labels.
- **Observation:** Several small text elements, including truck metadata and footer links, appear light gray on white or charcoal backgrounds. **Impact:** Small text may be difficult to read at normal viewing distance. **Fix:** Verify each foreground/background pair with a contrast checker and darken any failing text colors.
- **Observation:** Open and closed states use green and red pills, while the page also uses pink and purple gradients for decoration. **Impact:** Multiple saturated treatments compete, and the status colors are not part of a coherent system. **Fix:** Reduce decorative saturation and define a consistent set of semantic colors for status, action, and background.

### 6. States & Access

- **Observation:** The screenshots show no keyboard-focus treatment on navigation links, buttons, or form fields. **Impact:** Keyboard users may not know which control is active. **Fix:** Tab through the page and add a high-contrast `:focus-visible` style to every interactive element; this needs a keyboard check because the screenshots cannot establish focus behavior.
- **Observation:** The signup form presents name, email, and cuisine fields, but the screenshots show no validation or submission feedback. **Impact:** Visitors may not know which fields are required or whether signup succeeded. **Fix:** Verify required-field labels, error messaging, and a clear success state with keyboard and screen-reader testing.
- **Observation:** Truck cards display open/closed status with colored pills. **Impact:** The text labels help, but color alone would not be sufficient if the labels disappear or become unclear in another state. **Fix:** Keep the explicit status text in every state and verify contrast for both pills.

### 7. Responsive

- **Observation:** At 1280px, the six truck cards use three columns; at 375px, they use one column, resulting in a very long page. **Impact:** Mobile visitors lose the quick side-by-side comparison available on desktop. **Fix:** Keep a single column if card readability requires it, but reduce each card's height or use a compact two-column layout only where its text still fits.
- **Observation:** The mobile section headings “Why TruckTrack?” and “Trucks Near You” each wrap onto two lines, while the hero heading wraps onto three. **Impact:** Heading wraps consume vertical space and create uneven rhythm between sections. **Fix:** Tune heading size, max-width, and line breaks for the 375px layout rather than relying on incidental wrapping.
- **Observation:** The mobile signup fields and button stack vertically and span nearly the full content width. **Impact:** The primary action is easy to find, but the form adds considerable height near the bottom of an already long page. **Fix:** Preserve full-width controls while reducing unnecessary vertical gaps and keeping labels and validation messages visible.

## AI Defaults

- Blue-purple gradient hero with centered white text.
- Headline, supporting paragraph, and prominent call-to-action button.
- Three-column feature section presented as rounded white cards with shadows.
- Emoji used as the feature and truck imagery.
- Repeated rounded cards with soft shadows.
- A second gradient call-to-action section near the bottom of the page.

## Measurements and Notes

- Screenshot widths: desktop 1280px; mobile 375px.
- Truck listing: three columns on desktop; one column with six stacked cards on mobile.
- Mobile screenshot height: 4867px; the hero occupies about 600px before the first content section.
- Initial assessment recorded: “4 contrast errors” and “AIM score 7.9 out of 10.” The specific contrast pairs and scoring method were not recorded, so these still need to be verified and documented.

## Partner Check

Not completed yet. Add two partner-identified problems here and mark each one “(found by partner)” after the review.

## Scope Note

These observations refer to `before/desktop.png` and `before/mobile.png`. The root `index.html` currently shows a different design, and `before/index.html` is not present, so the screenshots are the available record of the before page.