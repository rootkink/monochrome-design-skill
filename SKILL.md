---
name: monochrome-chrome-design
description: Design any deck, website, poster or social post in the monochrome chrome-glass style with dot-matrix data visuals, HUD wireframes and gradient type.
---

# Monochrome Chrome Design System

A strict greyscale look: near-black spotlit backgrounds with a faint grid, glass cards whose borders catch light from above, white-to-grey gradient headlines in Inter, JetBrains Mono labels, HUD wireframe diagrams (corner brackets, status chips, tick meters) and dot-matrix data visuals. Think Apple keynote x crypto product launch x mission-control dashboard: calm, premium, futuristic, never cluttered.

Use this skill whenever the user asks for this style, "the Veil theme", "monochrome chrome", "glass and dot-matrix", or any visual (pptx, website, landing page, poster, flyer, social post, dashboard, one-pager) that should match it. The user supplies the topic, text and data; this skill supplies everything visual.

## 0. Workflow

1. Get the brief: topic, audience, goal, format, size, sections, real data (and which numbers are only examples), optional hero image. Missing pieces: choose sensibly and say what you chose.
2. Write the content first (one idea per slide or section, short claims as titles).
3. Map each piece of content to a visual using section 5.
4. Build in the target format (section 7: website, poster, pptx).
5. Render and look at the result (section 8), fix, then deliver. Tell the user to install Inter and JetBrains Mono.

Hard rules: greyscale only, no colour accents. Emphasis = brightness (white vs grey), a soft white glow, filled vs outline. Exactly one highlighted element per group. No stock photos, no clip art, no accent bars or stripes, no underlines under titles. Real data is shown exactly; illustrative numbers are flagged as examples.

## 1. Tokens

| Token | Value | Use |
|---|---|---|
| bg | #050506 | Base background |
| text | #EDEDED | Body text, filled dots, active ticks, primary button fill |
| white | #FFFFFF | The single most important element, active status |
| muted | #8A8A92 | Secondary sentences, problem lines, captions |
| dim | #5C5C64 | Mono labels, indices, footer, inactive dots |
| label | #B4B4BC | Badge text |
| chip | #0E0E11 | Badge and chip fill |
| chipLine | #2E2E34 | Badge and chip border |
| hair | #26262B | Dividers |
| tickOff | #2C2C32 | Empty tick bars |

Gradients (all top to bottom):

| Element | Stops |
|---|---|
| Headline text | #FFFFFF 0% to #7E7E86 100% |
| Glass fill | #1D1D22 to #0B0B0E |
| Glass border (lit from above) | #82828A 0%, #2C2C32 35%, #18181C 100% |
| Highlighted fill | #303037 to #121216 |
| Highlighted border | #E2E2E8 0%, #5A5A62 40%, #26262C 100% |
| Giant fading wordmark | #5E5E66 0%, #121215 65%, #050506 100% |

Shadows: glass = black, blur 22, 8 down, 60%. Highlighted = white glow, blur 28, no offset, 12%.

Lighting background: base #050506; radial spotlight from just above the frame (#2E2E34 centre, #16161A at 32%, #08080A at 70%, #050506 edge, radius about 115% of the frame height; brighter #3A3A42 centre for hero/cover/statement frames, placed top-centre; content frames place it top-left at 22% across); a square grid (cell about 3.3% of frame width, white lines 8.5% opacity) visible only near the spotlight; one wide blurred diagonal light sheen (white 5%); a vignette (black 0% at 55% radius to 60% at the edge).

Typography:
- Headlines: Inter regular (not bold), gradient fill, tight and large. Deck: cover 60pt, titles 40pt, statements 46pt. Web: clamp(40px, 6vw, 88px). Poster: headline about 8 to 10% of the frame width.
- Body: Inter, 16 to 18pt (web 16 to 18px), text or muted colour. Nothing smaller than 13pt for sentences.
- Labels, data, status, code: JetBrains Mono, 9 to 11pt, uppercase, letter-spacing 0.06em, dim or muted colour. Numbers always mono or dot-matrix.
- Left-align body text. Centre only statements, captions and diagram labels.

Spacing: outer margin about 5% of the frame width (0.7in on a 13.333in slide), gaps 0.25 to 0.3in (web 24px), generous empty space, at most about 30 words of body text per slide or poster panel.

## 2. Components

| Component | Spec |
|---|---|
| Section badge | Pill, height 0.32in or 28px, chip fill, chipLine border, small white dot with dark centre on the left, Inter 11 label colour, sentence case ("Feature 03 / 08 · Identity"). Sits above every title. |
| Hero badge | Wider pill with an inner white pill "New" (dark bold 10) then grey text. |
| Primary pill button | Fully rounded, fill #EDEDED, dark bold Inter 12 to 13 ("Get started ↓"). |
| Secondary pill | Fully rounded, glass fill + lit border, light text ("Watch demo ▸"). |
| Glass card | Radius 14px or 0.14in, glass fill, glass border, black shadow. Default container. |
| Highlighted card | Highlighted fill and border, white glow. One per group. |
| HUD corner brackets | Four L marks (arms 12 to 16px or 0.12 to 0.16in, 1.25pt) just outside a panel. Dim normally, near-white on the highlighted element. |
| Status chip | Small rounded rect (radius 4px), chip fill and border, tiny dot (white = active, dim = inactive), JetBrains Mono 9 uppercase: "● LIVE", "● VERIFIED", "● NOW", "○ LIMIT", "○ LATER". |
| Tick meter | 20 thin vertical bars (0.065in or 5px wide, gaps 0.06in or 4px). Filled #EDEDED, empty tickOff. Mono label left, % right. |
| Icon box | Square glass tile with corner brackets and one thin-line icon (Lucide, stroke 1.2 to 1.5, light grey; white when highlighted). |
| HUD list row | Glass row: status chip holding the item name, mono value, small ↗ icon right. Stack 3 to 5. |
| Nav bar | Round white logo mark with a dark icon, wordmark Inter 18, 3 to 4 centred grey nav words, white pill on the right. |
| Mono strip | 4 to 6 tiny line icons with mono uppercase labels in #6E6E76, evenly spaced, like a logo row. |
| Three-part text block | Mono 11 dim labels "01 — TODAY", "02 — WITH [NAME]", "03 — WHY IT MATTERS"; first sentence muted, second text colour, third italic with the headline gradient. |
| Footer | Mono 9 dim "[NAME]  //  [TITLE] [YEAR]" left, page number right. |
| Arrows | 1.25pt grey with small triangle heads; key step near-white 1.75 to 2pt; dashed for optional or "checks" links. |

## 3. Visual library

Line or dot art only, white and grey on black, thin strokes.

Dot-matrix family (generators in section 6):
- Dot-matrix numerals: 5x7 dot grid per character, lit dots white, unlit dots small at 7% so the grid shows. For hero stats.
- Dotted bar chart: columns of dots; filled grey 45%, the latest 3 to 4 columns white, unfilled 6%. Mono period label ("30 DAYS").
- Dotted ring gauge: 48 dots, lit share = value, faint inner ring, value centred in mono.
- Big dotted ring: about 160 dots, 60% lit, behind statements; spins slowly.
- Dot-art icons: concepts drawn in dots (database leaking a dot stream, black box with "?", padlock, glitched double face, fingerprint arcs, tick in a ring, nested squares, hub-and-spoke network).

HUD wireframe family:
- Exploded isometric stack: 3 to 5 plates (2:1 rhombus tops, fine inner grid, thin sides), dashed vertical guides, key plate brighter with glow, each with a small symbol and a leader line to a dot aligned with its label. For architecture, stacks, layers, levels.
- Wireframe globe: sphere outline, latitude/longitude ellipses tilted about 22°, ringed nodes, dotted links to a glowing centre node, 3 to 4 pill chips around it on dashed lines. For networks, reach, ecosystems.
- Sequence diagram: two tall glass lanes (actors) with big thin icons, mono names and status chips; 3 to 5 alternating arrows with numbered mono labels ("01  COMMIT") and grey captions; last arrow white and thicker.
- Triangle diagram: three icon boxes, two solid arrows, one dashed, mono edge labels, a white pill on the key arrow.
- Flow chain: 3 to 4 icon boxes joined by arrows, each with a name and caption, ending in a record card.
- Record card: highlighted glass card with brackets, mono header with an ID, status chip, 4 mono key-value rows (keys dim, values light).

App and dashboard family:
- Dashboard card grid: numbered cards ("01  YOUR EARNINGS") each with a status chip, one dot-matrix number or chart, a mono caption.
- Code / settings window: three grey dots and a mono filename, 3 to 5 lines of mono code (keywords white, values grey), hairline, tick-meter sliders, a white and a dark pill.
- Nested layer cards: outer = public, inner = private and highlighted, each with mono label, one line and a status chip.
- Journey cards: 4 to 6 tall cards with mono index and time, dot illustration, gradient title, one-line action, mono stat; last one highlighted.
- Two-panel comparison: left panel highlighted, each with icon, gradient heading and 4 HUD list rows ("● SECURE" vs "○ LIMIT").
- Roadmap: thin line with phase dots (first glowing), mono phase labels, a card per phase with name, mono timeframe, 3 bullets, status chip, tick meter.
- Pricing / tier cards (web): three glass cards, middle highlighted.

Hero image (optional, cover or hero section): turn black into transparency (brightness becomes alpha), tint near-white #ECECF0, feather the edge with a radial fade, put a soft radial white glow behind it (16% centre to 0) and a thin dotted halo ring with 3 to 4 brighter dots; slow spin. Script in section 6. Without an image use the big dotted ring or the globe.

## 4. Layout recipes

Decks (13.333 x 7.5in): badge at y 0.42, title at x 0.7 y 0.92 (same spot on every content slide), content y 1.95 to 6.55, footer y 7.0.

| Frame | Recipe |
|---|---|
| Cover / hero | Nav bar top. Hero badge. Two-line gradient headline left. One grey sentence. Primary + secondary pills. Hero image or ring right, large. Mono strip along the bottom. |
| Problem | 4 glass cards in a row, each: mono index, "○ ISSUE" chip, dot-art icon, gradient name, one grey line. |
| Statement | Big dotted ring centred, centred badge, one centred gradient sentence, two pills splitting the idea. |
| How it works | Isometric stack left, labels right on the leader lines, one mono note at the bottom. |
| Feature A | Visual across the top, three-part text block as three columns below. |
| Feature B / C | Visual one side, three-part text block the other; alternate sides. |
| Data | Dashboard card grid two-thirds, narrow text block one-third. |
| Journey | Persona pill near the title, 5 journey cards. |
| Comparison | Two panels side by side. |
| Roadmap | Timeline with phase dots, phase cards below. |
| Closing | Small hero image top centre, badge, one gradient line, grey line, two pills, a giant bold wordmark fading into the background and cut off by the bottom edge. |

Websites (single page, max width 1200px): nav bar; hero (badge, gradient headline, sentence, pills, hero visual); mono strip; feature section (badge + gradient h2 + bento grid of glass cards with visuals); dashboard or results section (dot-matrix stats, highlighted cards); pricing or plans (three cards, middle highlighted); testimonials or FAQ as glass rows; footer with links in mono and the giant fading wordmark.

Posters and social posts (portrait): top row = logo mark + mono meta (date, place); badge; huge gradient headline (2 to 3 lines) in the top third; one hero visual (hero image, ring, globe or isometric stack) in the middle third; a row of 2 to 4 dashboard cards or a three-part text block in the bottom third; mono footer strip with details and a white pill CTA. Keep at least 5% margins. Standard sizes: A4 2480x3508 px and A3 3508x4961 px at 300dpi, Instagram post 1080x1350, story 1080x1920, LinkedIn 1200x627, 16:9 1920x1080.

## 5. Content to visual

| Content | Visual |
|---|---|
| One headline number | Dot-matrix numeral in a dashboard card |
| Values over time | Dotted bar chart (latest bars white) |
| Share, score, completion | Dotted ring gauge or tick meter |
| Several weights or settings | Stack of tick meters |
| Layers, stack, levels | Isometric stack |
| Exchange between two parties | Sequence diagram |
| Three parties with trust or flow | Triangle diagram |
| Ordered steps | Flow chain |
| Network, reach, ecosystem | Wireframe globe with chips |
| Levels of access or audience | Nested layer cards |
| Pros vs cons, strengths vs limits | Two-panel comparison |
| Phases or timeline | Roadmap |
| A user's day, a customer journey | Journey cards |
| A concept or problem | Dot-art icon in a glass card |

## 6. Code: CSS, generators, hero image, fonts

Ready-to-run copies of every code block below are in `scripts/` next to this file (chrome.css, generators.js, hero_blend.py, pptx_gradients.py, pptx_animate.py). Use them directly when the skill folder is available; the blocks here are the same code.

CSS kit (websites, HTML posters, HTML-to-image):

```css
@import url('https://fonts.googleapis.com/css2?family=Inter:wght@400;500;700&family=JetBrains+Mono:wght@400;700&display=swap');
:root {
  --bg: #050506; --text: #EDEDED; --white: #FFFFFF; --muted: #8A8A92; --dim: #5C5C64; --label: #B4B4BC;
  --chip: #0E0E11; --chip-line: #2E2E34; --hair: #26262B; --tick-off: #2C2C32;
  --glass: linear-gradient(180deg, #1D1D22, #0B0B0E);
  --glass-rim: linear-gradient(180deg, #82828A 0%, #2C2C32 35%, #18181C 100%);
  --hi: linear-gradient(180deg, #303037, #121216);
  --hi-rim: linear-gradient(180deg, #E2E2E8 0%, #5A5A62 40%, #26262C 100%);
  --head: linear-gradient(180deg, #FFFFFF, #7E7E86);
  --sans: 'Inter', system-ui, sans-serif; --mono: 'JetBrains Mono', ui-monospace, monospace;
}
body { margin: 0; background: var(--bg); color: var(--text); font: 400 17px/1.55 var(--sans); }
.stage { position: relative; isolation: isolate; overflow: hidden;
  background: radial-gradient(ellipse 120% 115% at var(--sx, 22%) var(--sy, -18%), var(--spot, #2E2E34) 0%, #16161A 32%, #08080A 70%, #050506 100%); }
.stage.hero { --sx: 50%; --sy: -8%; --spot: #3A3A42; }
.stage::before { content: ''; position: absolute; inset: 0; z-index: -1; pointer-events: none;
  background-image: linear-gradient(rgba(255,255,255,.085) 1px, transparent 1px), linear-gradient(90deg, rgba(255,255,255,.085) 1px, transparent 1px);
  background-size: 44px 44px;
  -webkit-mask-image: radial-gradient(circle at var(--sx, 22%) var(--sy, -18%), #000 0%, transparent 75%);
  mask-image: radial-gradient(circle at var(--sx, 22%) var(--sy, -18%), #000 0%, transparent 75%); }
.stage::after { content: ''; position: absolute; inset: 0; z-index: -1; pointer-events: none;
  background: radial-gradient(circle at 50% 50%, transparent 55%, rgba(0,0,0,.6) 100%); }
.grad-text { background: var(--head); -webkit-background-clip: text; background-clip: text; color: transparent; }
h1, h2 { font-weight: 400; letter-spacing: -0.02em; line-height: 1.05; margin: 0; }
h1 { font-size: clamp(40px, 6vw, 88px); } h2 { font-size: clamp(32px, 4vw, 56px); }
.mono { font-family: var(--mono); font-size: 11px; letter-spacing: .06em; text-transform: uppercase; color: var(--dim); }
.muted { color: var(--muted); }
.glass { background: var(--glass) padding-box, var(--glass-rim) border-box; border: 1px solid transparent; border-radius: 14px; box-shadow: 0 8px 22px rgba(0,0,0,.6); }
.glass.hi { background: var(--hi) padding-box, var(--hi-rim) border-box; box-shadow: 0 0 28px rgba(255,255,255,.12); }
.badge { display: inline-flex; align-items: center; gap: 8px; height: 28px; padding: 0 12px 0 6px; border-radius: 99px;
  background: var(--chip); border: 1px solid var(--chip-line); color: var(--label); font-size: 12px; }
.badge::before { content: ''; width: 16px; height: 16px; border-radius: 50%; background: radial-gradient(circle, #0A0A0D 0 3px, #EDEDED 3.5px); }
.pill { display: inline-flex; align-items: center; gap: 8px; height: 44px; padding: 0 22px; border-radius: 99px; font: 600 14px var(--sans); text-decoration: none; }
.pill.primary { background: #EDEDED; color: #0A0A0D; }
.pill.secondary { background: var(--glass) padding-box, var(--glass-rim) border-box; border: 1px solid transparent; color: var(--text); }
.chip { display: inline-flex; align-items: center; gap: 6px; height: 22px; padding: 0 8px; border-radius: 4px;
  background: var(--chip); border: 1px solid var(--chip-line); font: 400 10px var(--mono); letter-spacing: .06em; text-transform: uppercase; color: var(--text); }
.chip::before { content: ''; width: 6px; height: 6px; border-radius: 50%; background: #EDEDED; }
.chip.off { color: var(--muted); } .chip.off::before { background: var(--dim); }
.hud { position: relative; }
.hud::after { content: ''; position: absolute; inset: -6px; pointer-events: none; --c: var(--bracket, #5C5C64); --l: 14px; --t: 1.25px;
  background:
    linear-gradient(var(--c), var(--c)) top left / var(--l) var(--t) no-repeat, linear-gradient(var(--c), var(--c)) top left / var(--t) var(--l) no-repeat,
    linear-gradient(var(--c), var(--c)) top right / var(--l) var(--t) no-repeat, linear-gradient(var(--c), var(--c)) top right / var(--t) var(--l) no-repeat,
    linear-gradient(var(--c), var(--c)) bottom left / var(--l) var(--t) no-repeat, linear-gradient(var(--c), var(--c)) bottom left / var(--t) var(--l) no-repeat,
    linear-gradient(var(--c), var(--c)) bottom right / var(--l) var(--t) no-repeat, linear-gradient(var(--c), var(--c)) bottom right / var(--t) var(--l) no-repeat; }
.hud.hi { --bracket: #EDEDED; }
.ticks { display: flex; gap: 4px; } .ticks i { width: 5px; height: 22px; background: var(--tick-off); } .ticks i.on { background: #EDEDED; }
.wordmark { font: 700 clamp(120px, 22vw, 360px)/0.8 var(--sans); text-align: center; letter-spacing: .02em;
  background: linear-gradient(180deg, #5E5E66 0%, #121215 65%, #050506 100%); -webkit-background-clip: text; background-clip: text; color: transparent; }
/* motion: add class + style="--d:300ms" for stagger */
@keyframes fade { from { opacity: 0 } }
@keyframes rise { from { opacity: 0; transform: translateY(24px) } }
@keyframes zoom { from { opacity: 0; transform: scale(.85) } }
@keyframes wipe { from { clip-path: inset(0 100% 0 0) } to { clip-path: inset(0 0 0 0) } }
@keyframes spin { to { transform: rotate(360deg) } }
.a-fade { animation: fade .5s ease-out both var(--d, 0ms); }
.a-rise { animation: rise .65s cubic-bezier(.2,.7,.2,1) both var(--d, 0ms); }
.a-zoom { animation: zoom .7s cubic-bezier(.2,.7,.2,1) both var(--d, 0ms); }
.a-wipe { animation: wipe .55s ease-out both var(--d, 0ms); }
.a-spin { animation: spin 60s linear infinite; } .a-spin.rev { animation-duration: 90s; animation-direction: reverse; }
@media (prefers-reduced-motion: reduce) { [class*='a-'] { animation: none !important; } }
```

For long web pages, start each section's animations when it scrolls into view (IntersectionObserver adding a class that sets animation-play-state: running; default paused).

SVG generators (plain JavaScript; works in the browser or in Node, where you rasterise with sharp: `await sharp(Buffer.from(svgString)).png().toBuffer()`; render at about 200 dpi for print or decks):

```js
const f = n => n.toFixed(1), rad = d => d * Math.PI / 180;
let uid = 0;   // unique ids, so many generated SVGs can share one web page
const svg = (w, h, body, defs = '') => { const k = ++uid;
  return `<svg xmlns='http://www.w3.org/2000/svg' width='${w}' height='${h}' viewBox='0 0 ${w} ${h}'><defs>${defs}</defs>${body}</svg>`
    .replace(/id='([^']+)'/g, `id='$1-${k}'`).replace(/url\(#([^)]+)\)/g, `url(#$1-${k})`); };
const dot = (x, y, r, o = 1) => `<circle cx='${f(x)}' cy='${f(y)}' r='${r}' fill='#EDEDED' fill-opacity='${o}'/>`;
function lineDots(x1, y1, x2, y2, step, r, o = 1) {
  const n = Math.max(1, Math.round(Math.hypot(x2 - x1, y2 - y1) / step)); let s = '';
  for (let i = 0; i <= n; i++) s += dot(x1 + (x2 - x1) * i / n, y1 + (y2 - y1) * i / n, r, o);
  return s;
}
function arcDots(cx, cy, rx, ry, a0, a1, step, r, o = 1) {
  const n = Math.max(2, Math.round(Math.max(rx, ry) * rad(Math.abs(a1 - a0)) / step)); let s = '';
  for (let i = 0; i <= n; i++) { const a = rad(a0 + (a1 - a0) * i / n); s += dot(cx + rx * Math.cos(a), cy + ry * Math.sin(a), r, o); }
  return s;
}
function ringDots(cx, cy, R, n, r, lit = 1, dimO = 0.16) {
  let s = '';
  for (let i = 0; i < n; i++) { const a = rad(-90 + 360 * i / n); s += dot(cx + R * Math.cos(a), cy + R * Math.sin(a), r, i < n * lit ? 1 : dimO); }
  return s;
}
const rectDots = (x, y, w, h, step, r, o = 1) => lineDots(x, y, x + w, y, step, r, o) + lineDots(x + w, y, x + w, y + h, step, r, o) + lineDots(x + w, y + h, x, y + h, step, r, o) + lineDots(x, y + h, x, y, step, r, o);
// 5x7 glyphs; add more as needed
const G = {
  0: ['01110','10001','10011','10101','11001','10001','01110'], 1: ['00100','01100','00100','00100','00100','00100','01110'],
  2: ['01110','10001','00001','00010','00100','01000','11111'], 3: ['11111','00010','00100','00010','00001','10001','01110'],
  4: ['00010','00110','01010','10010','11111','00010','00010'], 5: ['11111','10000','11110','00001','00001','10001','01110'],
  6: ['00110','01000','10000','11110','10001','10001','01110'], 7: ['11111','00001','00010','00100','01000','01000','01000'],
  8: ['01110','10001','10001','01110','10001','10001','01110'], 9: ['01110','10001','10001','01111','00001','00010','01100'],
  '%': ['11001','11010','00010','00100','01000','01011','10011'], '.': ['00000','00000','00000','00000','00000','01100','01100'],
  '+': ['00000','00100','00100','11111','00100','00100','00000'], '-': ['00000','00000','00000','11111','00000','00000','00000'],
  K: ['10001','10010','10100','11000','10100','10010','10001'], M: ['10001','11011','10101','10101','10001','10001','10001'],
  B: ['11110','10001','10001','11110','10001','10001','11110'], '$': ['00100','01111','10100','01110','00101','11110','00100'],
  '?': ['01110','10001','00001','00010','00100','00000','00100'], ' ': ['00000','00000','00000','00000','00000','00000','00000'],
};
function dotNumber(str, cell = 22) {            // returns { svg, w, h } in px
  const chars = [...String(str)], w = (chars.length * 6 - 1) * cell + cell, h = 8 * cell; let s = '';
  chars.forEach((ch, k) => (G[ch] || G[' ']).forEach((row, j) => [...row].forEach((b, i) => {
    const x = cell / 2 + (k * 6 + i) * cell, y = cell / 2 + j * cell;
    if (b === '1') s += dot(x, y, cell * 0.32); else if (ch !== ' ') s += dot(x, y, cell * 0.15, 0.07);
  })));
  return { svg: svg(w, h, s), w, h };
}
function dotBars(values, w = 760, h = 240, step = 13, r = 3.6, highlight = 4) {   // values 0..1
  const n = values.length, colW = w / n, rows = Math.floor((h - 12) / step); let s = '';
  values.forEach((v, i) => { const cx = colW * (i + 0.5), lit = Math.round(v * rows), bright = i >= n - highlight;
    for (let j = 0; j < rows; j++) s += dot(cx, h - 6 - j * step, r, j < lit ? (bright ? 1 : 0.45) : 0.06); });
  return svg(w, h, s);
}
const gauge = (size = 300, value = 0.33) => svg(size, size, ringDots(size / 2, size / 2, size * 0.44, 48, size * 0.013, value) + ringDots(size / 2, size / 2, size * 0.36, 36, size * 0.006, 0, 0.12));
const bigRing = (size = 1400, value = 0.62) => svg(size, size, ringDots(size / 2, size / 2, size * 0.47, 160, 3.4, value, 0.12) + ringDots(size / 2, size / 2, size * 0.4, 120, 2, 0, 0.1));
const halo = (size = 1200) => svg(size, size, ringDots(size / 2, size / 2, size * 0.48, 180, 2.4, 0.3, 0.18) + ringDots(size / 2, size / 2, size * 0.44, 4, 5, 1));
const glow = (size = 1000) => svg(size, size, `<circle cx='${size / 2}' cy='${size / 2}' r='${size / 2}' fill='url(#g)'/>`, `<radialGradient id='g'><stop offset='0' stop-color='#FFF' stop-opacity='.16'/><stop offset='.45' stop-color='#FFF' stop-opacity='.05'/><stop offset='1' stop-color='#FFF' stop-opacity='0'/></radialGradient>`);
function background(W, H, sx = 0.22, sy = -0.18, spot = '#2E2E34') {   // full-bleed lighting image
  const cx = sx * W, cy = sy * H, cell = Math.round(W / 30);
  return svg(W, H, `<rect width='${W}' height='${H}' fill='#050506'/><rect width='${W}' height='${H}' fill='url(#spot)'/>
<path d='M ${-W * 0.12} ${H * 0.98} Q ${W * 0.42} ${-H * 0.32} ${W * 1.12} ${H * 0.62}' fill='none' stroke='#FFF' stroke-opacity='.05' stroke-width='${W * 0.1}' filter='url(#b)'/>
<rect width='${W}' height='${H}' fill='url(#grid)' mask='url(#gm)'/><rect width='${W}' height='${H}' fill='url(#vig)'/>`,
`<radialGradient id='spot' gradientUnits='userSpaceOnUse' cx='${cx}' cy='${cy}' r='${H * 1.15}'><stop offset='0' stop-color='${spot}'/><stop offset='.32' stop-color='#16161A'/><stop offset='.7' stop-color='#08080A'/><stop offset='1' stop-color='#050506'/></radialGradient>
<pattern id='grid' width='${cell}' height='${cell}' patternUnits='userSpaceOnUse'><path d='M${cell} 0H0V${cell}' fill='none' stroke='#FFF' stroke-opacity='.085' stroke-width='${W / 1700}'/></pattern>
<radialGradient id='gmg' gradientUnits='userSpaceOnUse' cx='${cx}' cy='${cy}' r='${H}'><stop offset='0' stop-color='#FFF'/><stop offset='1' stop-color='#FFF' stop-opacity='0'/></radialGradient>
<mask id='gm'><rect width='${W}' height='${H}' fill='url(#gmg)'/></mask>
<radialGradient id='vig' gradientUnits='userSpaceOnUse' cx='${W / 2}' cy='${H / 2}' r='${Math.max(W, H) * 0.62}'><stop offset='.55' stop-color='#000' stop-opacity='0'/><stop offset='1' stop-color='#000' stop-opacity='.6'/></radialGradient>
<filter id='b' x='-50%' y='-50%' width='200%' height='200%'><feGaussianBlur stdDeviation='${W / 27}'/></filter>`);
}
// Exploded isometric stack. Returns one transparent SVG per plate (index 0 = top) plus the guide lines,
// all on the same canvas, so plates can be placed on top of each other and animated separately.
// ys = plate centre y in px; leader lines end at the right edge, so put labels right of the image at those heights.
function isoStack(n = 4, W = 1240, H = 940, hot = 1) {
  const cx = 430, a = 300, b = 150, t = 26, gap = (H - 2 * b - t - 40) / Math.max(1, n - 1), ys = [...Array(n)].map((_, i) => b + 25 + i * gap);
  const defs = `<linearGradient id='p' x1='0' y1='0' x2='1' y2='1'><stop offset='0' stop-color='#202025'/><stop offset='1' stop-color='#0B0B0E'/></linearGradient>
<linearGradient id='ph' x1='0' y1='0' x2='1' y2='1'><stop offset='0' stop-color='#3A3A42'/><stop offset='1' stop-color='#121215'/></linearGradient>
<filter id='g' x='-30%' y='-60%' width='160%' height='220%'><feGaussianBlur stdDeviation='10' result='b'/><feMerge><feMergeNode in='b'/><feMergeNode in='SourceGraphic'/></feMerge></filter>`;
  const guides = [[cx - a, 0], [cx + a, 0], [cx, b]].map(([x, dy]) => `<line x1='${x}' y1='${ys[0] + dy}' x2='${x}' y2='${ys[n - 1] + dy}' stroke='#FFF' stroke-opacity='.18' stroke-dasharray='3 7'/>`).join('');
  const plates = ys.map((y, i) => {
    const h = i === hot, so = h ? 0.95 : 0.5; let s = '';
    s += `<polygon points='${cx - a},${y} ${cx},${y + b} ${cx},${y + b + t} ${cx - a},${y + t}' fill='#0C0C0F' stroke='#FFF' stroke-opacity='${so * 0.6}' stroke-width='1.4'/>`;
    s += `<polygon points='${cx + a},${y} ${cx},${y + b} ${cx},${y + b + t} ${cx + a},${y + t}' fill='#111114' stroke='#FFF' stroke-opacity='${so * 0.6}' stroke-width='1.4'/>`;
    s += `<polygon points='${cx},${y - b} ${cx + a},${y} ${cx},${y + b} ${cx - a},${y}' fill='url(#${h ? 'ph' : 'p'})' stroke='#FFF' stroke-opacity='${so}' stroke-width='${h ? 2.4 : 1.6}' ${h ? `filter='url(#g)'` : ''}/>`;
    for (let k = 1; k < 8; k++) { const u = k / 8;
      s += `<line x1='${cx - a + a * u}' y1='${y - b * u}' x2='${cx + a * u}' y2='${y + b - b * u}' stroke='#FFF' stroke-opacity='${h ? 0.22 : 0.09}'/>`;
      s += `<line x1='${cx - a + a * u}' y1='${y + b * u}' x2='${cx + a * u}' y2='${y - b + b * u}' stroke='#FFF' stroke-opacity='${h ? 0.22 : 0.09}'/>`; }
    s += arcDots(cx, y, 60, 30, 0, 360, 9, 2.4, h ? 1 : 0.5) + dot(cx, y, 5, h ? 1 : 0.6);
    s += `<line x1='${cx + a + 14}' y1='${y}' x2='${W - 4}' y2='${y}' stroke='#FFF' stroke-opacity='${h ? 0.8 : 0.3}' ${h ? '' : `stroke-dasharray='4 6'`} stroke-width='1.4'/>` + dot(W - 6, y, 5, h ? 1 : 0.5);
    return svg(W, H, s, defs);
  });
  return { guides: svg(W, H, guides, defs), plates, ys, W, H };   // draw plates bottom-up (last index first)
}
```

Wireframe globe recipe (write it the same way): sphere circle (radial fill #26262C to #08080A, white stroke 45%); latitude ellipses at -60, -30, 0, 30, 60 degrees with centre y = c - R·sin(lat)·cos(22°), rx = R·cos(lat), ry = R·cos(lat)·sin(22°); longitude ellipses rx = R·|sin(lon)|, ry = R; project nodes with x = c + R·cos(lat)·sin(lon), y = c - R·(sin(lat)·cos(22°) - cos(lat)·cos(lon)·sin(22°)); dotted lines (lineDots) from a central node to each, thin solid lines between some neighbours, ringed node circles, a blurred white glow and ringDots around the centre node.

Dot-art icons: compose them from arcDots, lineDots, rectDots and ringDots at a 10px step and 3px dot radius (e.g. padlock = top half arc + two legs + rectDots body + small ring keyhole).

Hero image script (Python; makes black transparent, tints, feathers):

```python
from PIL import Image
import numpy as np
im = Image.open('hero.jpg').convert('L').resize((1400, 1400), Image.LANCZOS)
L = np.asarray(im).astype(np.float32) / 255
alpha = np.clip((L - 0.04) * 1.25, 0, 1)
yy, xx = np.mgrid[0:1400, 0:1400]
r = np.hypot(xx - 700, yy - 700) / 700
alpha *= np.clip((1.0 - r) / 0.12, 0, 1)
out = np.zeros((1400, 1400, 4), np.uint8); out[..., 0] = 236; out[..., 1] = 236; out[..., 2] = 240
out[..., 3] = (alpha * 255).astype(np.uint8)
Image.fromarray(out, 'RGBA').save('hero_blend.png')
```

For a non-square or non-centred subject, crop to the subject first and use a rectangular feather instead of the radial one.

Fonts for rendering in a sandbox (so previews match): Inter is often preinstalled (check with fc-list). JetBrains Mono: `npm pack @fontsource/jetbrains-mono`, extract, convert the 400 and 700 latin .woff files to .ttf with fontTools (`TTFont(path); f.flavor = None; f.save(...)`) into ~/.fonts, then `fc-cache -f`.

## 7. Building per format

### Website or landing page
- One self-contained HTML file with the CSS kit inline; generators inline in a script (or pre-rendered SVG inline).
- Sections follow the website recipe in section 4. Wrap each section in `.stage` (hero gets `.stage.hero`).
- Bento grids of `.glass` cards, one `.glass.hi`; `.hud` on diagram panels; `.chip` for status; `.ticks` for meters.
- Animate with the `.a-*` classes and a `--d` stagger of 120 to 250ms; trigger per section on scroll.
- Responsive: cards stack to one column under 720px; headline uses clamp; 16px side gutters on phones.

### Poster, flyer, social post, one-pager image
- Build as HTML at the exact pixel size with the CSS kit (render with a headless browser if available), or compose one SVG at the target size (background() + generators + text elements with font-family Inter / JetBrains Mono) and rasterise with sharp, or build as a single-slide pptx at the poster size and export to PDF.
- Follow the poster recipe in section 4. Text in SVG: use fill='url(#head)' with a vertical linearGradient for headlines.
- Export PNG for screens and PDF (or 300 dpi PNG) for print.

### PowerPoint (.pptx)
- pptxgenjs, `pres.layout = 'LAYOUT_WIDE'`. Define layouts Cover, Statement, Content, Closing; each gets background(2400, 1350, …) as its background image (hero variant: sx 0.5, sy -0.08, spot #3A3A42) and its title placeholder (positions in section 4). Content layout also gets the mono footer and slide number.
- Text boxes with margin 0. Fonts: Inter for text, JetBrains Mono for labels.
- Generated graphics as PNG images at about 200 dpi. Isometric plates as separate aligned images.
- Speaker notes on every slide: 3 to 5 conversational sentences, an everyday analogy for technical ideas, examples flagged.
- pptxgenjs cannot do gradients or animations, so build with marker colours and tagged names, then post-process the saved file with the two scripts below, then validate and render.

Marker colours (use these as solid colours while building): headline text FAFAFB, giant wordmark FAFAFC, glass fill 0B0B0D, glass border 3A3A3E, highlighted fill 0B0B0E, highlighted border 3A3A3F. Give highlighted cards a white glow shadow and glass cards a black shadow in pptxgenjs.

Animation tags: set objectName to `a_<startMs>_<effect>_<n>` (effects fade, rise, zoom, wipe; add spin or spinrev for endless rotation, e.g. zoomspin). An easy way: wrap slide.addText/addShape/addImage so everything added after `anim(450, 'rise')` gets that tag until the next `anim()` call. Never tag titles.

Script 1, gradients (python3 gradients.py deck.pptx):

```python
import re, sys, zipfile, shutil
def g(stops, ang=5400000):
    gs = ''.join(f"<a:gs pos='{p*1000}'><a:srgbClr val='{c}'/></a:gs>" for p, c in stops)
    return f"<a:gradFill rotWithShape='1'><a:gsLst>{gs}</a:gsLst><a:lin ang='{ang}' scaled='0'/></a:gradFill>"
MAP = {
    'FAFAFB': g([(0, 'FFFFFF'), (100, '7E7E86')]),
    'FAFAFC': g([(0, '5E5E66'), (65, '121215'), (100, '050506')]),
    '0B0B0D': g([(0, '1D1D22'), (100, '0B0B0E')]),
    '3A3A3E': g([(0, '82828A'), (35, '2C2C32'), (100, '18181C')]),
    '0B0B0E': g([(0, '303037'), (100, '121216')]),
    '3A3A3F': g([(0, 'E2E2E8'), (40, '5A5A62'), (100, '26262C')]),
}
PAT = re.compile(r'<a:solidFill><a:srgbClr val=.(' + '|'.join(MAP) + r').\s*/></a:solidFill>')
src = sys.argv[1]; tmp = src + '.tmp'
with zipfile.ZipFile(src) as zin, zipfile.ZipFile(tmp, 'w', zipfile.ZIP_DEFLATED) as zout:
    for item in zin.infolist():
        data = zin.read(item.filename)
        if re.match(r'ppt/(slides|slideLayouts|slideMasters)/[^/]+\.xml$', item.filename):
            data = PAT.sub(lambda m: MAP[m.group(1)], data.decode('utf-8')).encode('utf-8')
        zout.writestr(item, data)
shutil.move(tmp, src)
```

Script 2, animations and fade transitions (python3 anim.py deck.pptx), run after script 1:

```python
import re, sys, zipfile, shutil
DUR = {'fade': 500, 'rise': 650, 'zoom': 700, 'wipe': 550}
PRESET = {'fade': (10, 0), 'rise': (42, 0), 'zoom': (53, 16), 'wipe': (22, 8)}
class Ids:
    def __init__(self): self.n = 2
    def __call__(self): self.n += 1; return self.n
def tgt(s): return f"<p:tgtEl><p:spTgt spid='{s}'/></p:tgtEl>"
def entrance(ids, s, fx, delay, first):
    d = DUR[fx]
    k = (f"<p:set><p:cBhvr><p:cTn id='{ids()}' dur='1' fill='hold'><p:stCondLst><p:cond delay='0'/></p:stCondLst></p:cTn>{tgt(s)}"
         f"<p:attrNameLst><p:attrName>style.visibility</p:attrName></p:attrNameLst></p:cBhvr><p:to><p:strVal val='visible'/></p:to></p:set>")
    flt = 'wipe(left)' if fx == 'wipe' else 'fade'
    k += f"<p:animEffect transition='in' filter='{flt}'><p:cBhvr><p:cTn id='{ids()}' dur='{d}'/>{tgt(s)}</p:cBhvr></p:animEffect>"
    def mv(attr, a, b):
        return (f"<p:anim calcmode='lin' valueType='num'><p:cBhvr><p:cTn id='{ids()}' dur='{d}' decel='100000' fill='hold'/>{tgt(s)}"
                f"<p:attrNameLst><p:attrName>{attr}</p:attrName></p:attrNameLst></p:cBhvr><p:tavLst>"
                f"<p:tav tm='0'><p:val><p:strVal val='{a}'/></p:val></p:tav><p:tav tm='100000'><p:val><p:strVal val='{b}'/></p:val></p:tav></p:tavLst></p:anim>")
    if fx == 'rise': k += mv('ppt_y', '#ppt_y+0.04', '#ppt_y')
    if fx == 'zoom': k += mv('ppt_w', '#ppt_w*0.85', '#ppt_w') + mv('ppt_h', '#ppt_h*0.85', '#ppt_h')
    pid, sub = PRESET[fx]; node = 'afterEffect' if first else 'withEffect'
    return (f"<p:par><p:cTn id='{ids()}' presetID='{pid}' presetClass='entr' presetSubtype='{sub}' fill='hold' grpId='0' nodeType='{node}'>"
            f"<p:stCondLst><p:cond delay='{delay}'/></p:stCondLst><p:childTnLst>{k}</p:childTnLst></p:cTn></p:par>")
def spin(ids, s, delay, rev):
    by, ms = ('-21600000', 90000) if rev else ('21600000', 60000)
    return (f"<p:par><p:cTn id='{ids()}' presetID='8' presetClass='emph' presetSubtype='0' repeatCount='indefinite' fill='hold' grpId='1' nodeType='withEffect'>"
            f"<p:stCondLst><p:cond delay='{delay}'/></p:stCondLst><p:childTnLst><p:animRot by='{by}'><p:cBhvr><p:cTn id='{ids()}' dur='{ms}' fill='hold'/>{tgt(s)}"
            f"<p:attrNameLst><p:attrName>r</p:attrName></p:attrNameLst></p:cBhvr></p:animRot></p:childTnLst></p:cTn></p:par>")
TAG = re.compile(r'<p:cNvPr id=.(\d+). name=.a_(\d+)_([a-z]+)_\d+.')
def timing(xml):
    items = []
    for m in TAG.finditer(xml):
        is_sp = xml.rfind('<p:nvSpPr>', 0, m.start()) > xml.rfind('<p:nvPicPr>', 0, m.start())
        items.append((int(m.group(2)), m.group(1), m.group(3), is_sp))
    if not items: return ''
    items.sort(key=lambda i: i[0]); ids = Ids(); fx_xml = []; bld = []
    for n, (t, s, fx, is_sp) in enumerate(items):
        base = fx.replace('spin', '').replace('rev', '') or 'fade'
        fx_xml.append(entrance(ids, s, base, t, n == 0))
        if 'spin' in fx: fx_xml.append(spin(ids, s, t + DUR[base], 'rev' in fx))
        if is_sp: bld.append(f"<p:bldP spid='{s}' grpId='0' animBg='1'/>")
    inner = f"<p:par><p:cTn id='{ids()}' fill='hold'><p:stCondLst><p:cond delay='0'/></p:stCondLst><p:childTnLst>{''.join(fx_xml)}</p:childTnLst></p:cTn></p:par>"
    click = (f"<p:par><p:cTn id='{ids()}' fill='hold'><p:stCondLst><p:cond delay='indefinite'/><p:cond evt='onBegin' delay='0'><p:tn val='2'/></p:cond></p:stCondLst>"
             f"<p:childTnLst>{inner}</p:childTnLst></p:cTn></p:par>")
    return ("<p:timing><p:tnLst><p:par><p:cTn id='1' dur='indefinite' restart='never' nodeType='tmRoot'><p:childTnLst>"
            "<p:seq concurrent='1' nextAc='seek'><p:cTn id='2' dur='indefinite' nodeType='mainSeq'><p:childTnLst>" + click +
            "</p:childTnLst></p:cTn><p:prevCondLst><p:cond evt='onPrev' delay='0'><p:tgtEl><p:sldTgt/></p:tgtEl></p:cond></p:prevCondLst>"
            "<p:nextCondLst><p:cond evt='onNext' delay='0'><p:tgtEl><p:sldTgt/></p:tgtEl></p:cond></p:nextCondLst></p:seq>"
            "</p:childTnLst></p:cTn></p:par></p:tnLst>" + (f"<p:bldLst>{''.join(bld)}</p:bldLst>" if bld else '') + "</p:timing>")
src = sys.argv[1]; tmp = src + '.tmp'
with zipfile.ZipFile(src) as zin, zipfile.ZipFile(tmp, 'w', zipfile.ZIP_DEFLATED) as zout:
    for item in zin.infolist():
        data = zin.read(item.filename)
        if re.match(r'ppt/slides/slide\d+\.xml$', item.filename):
            xml = data.decode('utf-8')
            add = "<p:transition spd='med'><p:fade/></p:transition>" + timing(xml)
            pos = xml.find('<p:extLst>', xml.find('</p:clrMapOvr>'))
            xml = xml[:pos] + add + xml[pos:] if pos != -1 else xml.replace('</p:sld>', add + '</p:sld>')
            data = xml.encode('utf-8')
        zout.writestr(item, data)
shutil.move(tmp, src)
```

Animation choreography (decks and web alike): titles static; background visual first, then structure, then items one by one (150 to 300ms apart, a card's parts together), text block last; arrows wipe after the boxes they join; isometric plates rise bottom-up with their labels; tick meters and bar charts wipe left to right; only round things spin (hero image 60s, halo reverse 90s, big rings); everything settles within about 2.5s.

## 8. Quality check

1. Render every slide, page or poster to an image and look at it (for pptx: convert to PDF with LibreOffice, then to images; LibreOffice shows gradient text as solid and ignores animations, PowerPoint shows both).
2. Fix overflow, cut-off or overlapping text, uneven gaps, anything inside the outer margin.
3. Titles in the same position on every content slide; labels aligned with their leader lines and arrows.
4. Contrast: no dark text on dark fills, no grey icons on grey tiles.
5. One highlighted element per group; greyscale only.
6. pptx: run a validator if available and confirm it opens without a repair prompt; every slide has notes.
7. Tell the user to install Inter and JetBrains Mono (free, Google Fonts) and which numbers are examples.
