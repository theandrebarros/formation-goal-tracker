# Figma Make — Formation Goal Tracker

Paste the prompt below into Figma Make to generate the interactive design file.
Once generated, copy the Figma Make URL and paste it into the `FIGMA_MAKE_URL`
constant at the top of `index.html`.

---

## Prompt to paste into Figma Make

```
Build an interactive goal-tracking dashboard for a design systems engineer at FanDuel.
Use the FanDuel Formation Design System visual language throughout.

## Brand & tokens
- Primary font: Inter (400, 600, 700)
- Label/metadata font: Roboto Condensed (uppercase, letter-spacing 1px)
- Primary colour: #0070EB
- Background dark: #0a0a0a (base), #1C1D1D (surface), #2B2D2E (layer)
- Background light: #EAF0F6 (base), #ffffff (surface), #F7FBFF (layer)
- Text dark: #CED4DB (default), #ffffff (strong), #969DA3 (subtle)
- Text light: #1C1D1D (default), #05285A (strong), #6A6F73 (subtle)
- Border dark: #6A6F73. Border light: #B0B7BF
- Border radius: 4px for cards/inputs/buttons, 9999px for pills
- Spacing: 4px base grid (4, 8, 12, 16, 20, 24, 32, 40px)

## Page layout (max-width 920px, centred)
Start in dark mode. Include a light/dark toggle.

### 1 — Header bar
Left: eyebrow label "FanDuel Formation DS · 2026" (Roboto Condensed, 11px, uppercase),
H1 "Goal Tracker" (Inter 700, 26px), subtitle "Andre Barros · Design System Engineer"
(13px, subtle colour; "Design System Engineer" in primary blue).

Right: row of action buttons —
- Sync status badge pill (showing "No sync" by default, states: syncing / synced / error)
- "Figma Make" button (icon: grid/dots, links externally)
- "Review" toggle button (eye icon)
- "Print" button
- Settings gear icon button
- Light/dark toggle icon button

### 2 — Stats strip
4 tiles in a row, each: large number (28–32px, bold), label below (Roboto Condensed 10px uppercase).
Tiles: Total Goals · Active · Completed · Progress (shows %).
Progress tile number is in primary blue. Completed is green (#00732C light / #7FD9A1 dark).

Below the strip: a thin 3px progress bar (full width, gradient #005FC8 → #0070EB).

### 3 — Tab navigation
3 tabs below the stats: "My Goals", "Team Goals", "Org Goals".
Each tab has a small count badge (pill, 18px height). Active tab underlines in primary blue.
Border-bottom on the tab bar.

### 4 — Goal cards (My Goals tab active)
Sub-section heading: "Q1 Priority" (Roboto Condensed, uppercase, with a horizontal rule).

Each goal card (surface background, 1px border, 4px radius, 20px padding):
- Row: [20×20px checkbox] [goal meta: stream label (10px label) + title (15px bold)] [status pill]
- Below (indented to match checkbox): KR text (12px, subtle), optional callout quote (left-border accent),
  "Add notes" toggle (12px, primary), expandable textarea (when open).

Status pill variants (pill shape, 9999px radius, 9px Roboto Condensed):
- Active → blue tint background, blue text + dot
- Done → green tint background, green text + dot, card opacity 0.7, title strikethrough
- Upcoming → orange tint background, orange text + dot
- No KR → neutral grey

Show 4 Q1 goals:
1. "Design Lint Figma Plugin" — Active — stream "AI × DS Readiness"
2. "Library Architecture Investigation" — Active — stream "AI × DS Readiness"
3. "Communicate Value (numbers + no jargon)" — Active — stream "AI Prompting Guardrails" (with a quote callout from Matias)
4. "Make Formation Info Easy to Access" — Active — stream "AI × DS Consumption"

Below Q1, a collapsible "Later Quarters" section (collapsed by default, chevron toggle):
- 3 cards: Teams Using Tools (Upcoming), Recipe Creation via MCP (Upcoming), Translation Tooling (No KR)

### 5 — Team Goals tab (not active by default)
Section heading "Formation DS · Team Objectives".
4 cards: Formation v2 Adoption (Active), Storybook MCP Rollout (Active), Component Docs Coverage (Upcoming), Token Misuse Audit (Active).

### 6 — Org Goals tab (not active by default)
Section heading "FanDuel · Organisational Goals".
4 cards: AI-First Product Development (Active), Cross-Platform Design Consistency (Upcoming), Developer Experience Improvements (Active), Accessibility Compliance (Upcoming).

### 7 — Settings modal
Full-screen overlay (dark backdrop, blur). Centred card (460px wide, 4px radius).
Header: "Sync Settings" + close button.
Body sections:
- "Your identity" → name text input
- "GitHub sync" → PAT password input + Gist ID input with "New Gist" button
- Status message area (info/success/error)
Footer: danger buttons ("Clear credentials", "Reset data") on left; "Save & sync" primary button on right.

### 8 — Toast notification
Bottom-right corner, slide-up animation. Contains: icon, message text, optional action link, dismiss button.
Example state: "🔄 Matias updated the tracker." with "Refresh now" action link.

### 9 — Review mode
When toggled: hides checkboxes, edit controls, notes textareas. Shows notes as read-only italic text. Header action buttons collapse to just the Exit Review button.

## Interactions to wire
- Light/dark mode toggle
- Tab switching (My Goals / Team / Org)
- Goal checkbox tick (cycles Active → Done → Active)
- Status pill click (same cycle)
- Notes toggle (expand/collapse textarea)
- Collapsible Later Quarters section
- Settings modal open/close (gear icon)
- Review mode toggle
- Toast appear/dismiss
```

---

## After generating

1. Click **Share** in Figma Make → copy the Make file URL
2. Open `index.html`, find line: `const FIGMA_MAKE_URL = '';`
3. Replace with: `const FIGMA_MAKE_URL = 'YOUR_URL_HERE';`
4. Save and push — the "Figma Make" button will appear in the header automatically
