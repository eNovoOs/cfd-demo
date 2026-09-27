# CFD demo site

Static HTML demo of a new website for Child & Family Development, a pediatric therapy practice
in Oakland, New Jersey that also runs a preschool. Not the other way around.

This is shown to the client in a meeting. No build step, no framework, no npm, no bundler.
Each page is one self-contained .html file with its CSS in a `<style>` block, exactly like
`dir-floortime.html`.

All client-facing copy is US English.

It is deployed. Repo `eNovoOs/cfd-demo` (public), live at https://cfd-demo.vercel.app on the
Vercel team `media-1872's projects`. Every push to `main` redeploys automatically. Her Wix site
at childfam-dev.com is still live and untouched.

## Design source, read this first

`dir-floortime.html` is the approved design and it is already built. Read it before writing
anything. Copy its CSS, its components, its spacing and its section rhythm into every new page.
Do not invent new visual patterns, do not restyle it, do not "improve" it. If a new page needs a
component that does not exist there, build it in the same language and tell me what you added.

`dir-floortime.html` has since been edited twice, both times deliberately: once to wire its nav,
footer and button links, and once to add the responsive rules it never had. Its copy, its
components and its desktop rendering are unchanged.

## Design tokens

```
navy      #2B3A7A   primary, all headings and most buttons
ink       #1C2340   long-form body text
slate     #556B8D   secondary text, captions
mist      #D5DAE3   rules, dividers, borders
cloud     #F4F6FA   section backgrounds
pink      #E2879B   DIR/Floortime accent
green     #96C079   Harbor Academy accent
sky       #89BFCA   individual therapies accent
sunshine  #EEC72C   research and donation material only
```

Surface split: 60% neutral (white, cloud or navy), 30% navy, 10% everything else combined.

Only navy, ink and slate may carry text. Pink, green, sky and sunshine are decoration only:
they tint a rule, a dot, an eyebrow or a bar. They never set body copy.

Only one pink button per page, on the single highest-intent action. Every other button is navy
on light, white on dark.

## Typography

Montserrat for everything, Forum for display lines only (pull quotes, a large statement).
Both load from Google Fonts, already linked in `dir-floortime.html`.

- Body never below 16px. Line length 60 to 75 characters.
- Sentence case headlines, with manual line breaks. Never let a short headline wrap on its own.
- No all caps beyond the small eyebrow label.

## Logo

- `assets/logo-color.png` on white, cloud or any light field.
- `assets/logo-white.png` on navy, on a gradient, or on any dark field.
- Minimum width 180px. Never recolour, stretch, rotate or add effects.
- Never use the mark without the wordmark on a page.

## Copy rules, non negotiable

Read `brand/03-compliance-rules.md` before writing any copy, and `brand/02-messaging-bank.md`
for approved lines. These are not style preferences: breaking them gets ad accounts restricted
and damages a clinical practice.

- Never assert or imply knowledge of the reader's health condition. No "Does your child have
  autism?", no "Is your child struggling?". Describe the program and who it is built for, in the
  third person.
- Never claim or imply a clinical outcome. Banned: cure, fix, normal, high functioning, low
  functioning, suffers from, afflicted, miracle, guaranteed, proven to, breakthrough, transform
  your child, special needs preschool.
- Never write "covered by insurance". The practice has no in-network contracts. The correct
  phrasing is "we verify your out-of-network benefits".
- Never name a competing business. The ABA category may be named once, as the practice's own
  positioning, never as an attack.
- Never use em dashes or en dashes in any copy. Use clean punctuation instead.
- Never invent a number, a price, a schedule, a ratio, a statistic or a claim. Everything factual
  comes from `brand/01-brand-facts.md`. If a fact is missing, write `TBC` in the page and list it
  for me at the end.

Two specific traps:

- Do not publish the 1:3 Harbor Academy ratio. The client states it, the live site does not, so it
  stays out until they publish it.
- The Playful Pathways Project is research in progress, never evidence in hand. Correct: "we are
  studying how relationship-based therapy changes the developing brain." Incorrect: "our therapy
  changes the brain."

## Data handling

Forms in this demo collect parent name, phone, email, program and location only. Never a child's
name, a date of birth, a diagnosis or insurance information. Add the line "Please do not include
medical or insurance details here" under any form.

Nothing a visitor types may reach an analytics or ad platform. Every `.form` block carries
`data-clarity-mask="true"` so Clarity session recordings do not capture it, and pixel events
carry only static labels, never field values. Keep both properties on any new form.

## Scope of this demo

- All internal links must resolve to a file that exists in this folder.
- Forms do not submit anywhere. The submit button is a link to `thank-you.html`.
- Analytics and the Meta pixel are installed, see "Analytics and tracking" below. Beyond those,
  Google Fonts and the pixel endpoints, make no other external request. No new third-party script
  without asking.
- Photos are real now, see "Photography and consent" below. Never stock photography and never AI
  generated images of children.
- Responsive matters: these parents read on a phone, and most ad traffic will arrive there. Every
  page must work at 390px wide.

## Pages

| File | What it is |
|---|---|
| `index.html` | Home. Routes three parents to the right program. No booking form. |
| `harbor-academy.html` | Harbor Academy program page. Meadow Green accent. |
| `dir-floortime.html` | The approved design, and the DIR/Floortime program page. Coral Pink accent. |
| `therapies.html` | Individual therapies, birth to 21. Sky accent. |
| `team.html` | The team, with staff bios. Navy, no program accent. |
| `thank-you.html` | Booking confirmation. Fires the `Lead` event. |
| `lp-harbor-academy.html` | Meta ads landing page. Not part of the site. |
| `lp-dir-floortime.html` | Meta ads landing page. Not part of the site. |

The header nav and footer are byte-identical across the six site pages. Change one, change all six.

The two `lp-` pages are deliberately different: logo only, no nav links, one conversion goal, and
`noindex` so they do not compete with the site in organic search. Paid traffic leaks through every
nav link you give it. Do not "fix" them to match the site.

## Components added

Built in the same visual language as `dir-floortime.html`, since it had none of these:

- `.pic` wraps a real photo where `.ph` was a placeholder. Same radius and dimensions.
- `.people` the team card grid on `team.html`. Uses `aspect-ratio:4/5` so portraits hold framing.
- `.cards` a `.ladder` box without the stagger, in 2 and 3 column grids.
- `.mt` / `.mb` a CSS-only hamburger. No JavaScript. Header drops from about 240px to 123px on a
  phone, which matters because the logo lockup is nearly square and sets the floor.
- `.sticky` bottom call to action, `lp-` pages only, under 760px. Gentle lift every 5 seconds,
  guarded by `prefers-reduced-motion`.
- `.trust` and `.price` on the `lp-` pages.

## Photography and consent

Real photos from the client's marketing folder are in `assets/photos/`. Originals live outside the
repo in `../Images/`.

**Only frames without identifiable children are published.** Every photo the client supplied shows
children at the practice, and written consent per family is not confirmed. A photo of an
identifiable minor on a therapy practice's public site also implies health information about that
child. Two crops were redone for exactly this reason. Until the client confirms written consent,
use back-of-head, hands-only or room-only frames.

Do not use the "Oliver - Pre-Post 1 year of DIR-Floortime Therapy" material. Before-and-after
framing is banned outright by `brand/03-compliance-rules.md`.

Exported photos carry no EXIF or GPS. Strip it on anything new; the source HEICs geotag the center.

Staff bio photos are fine to publish. Bios come from the questionnaires in
`../Images/EduCare - Marketing Folder/Team Photos and Bios/`, never invented.

Two things in those questionnaires are deliberately left out of `team.html`: a staff member's named
child and his developmental status, and another member's disclosure about herself and her children.
Both are health details about private individuals, one a minor. Publishing them is the client's
call, not ours.

## Analytics and tracking

| What | Where | Detail |
|---|---|---|
| Microsoft Clarity | All 8 pages | Project `yoqzhupcqt`. Session recording and heatmaps. |
| Meta pixel | All 8 pages | `1161526882203012`. `PageView` on load. |
| `ViewContent` | All 8 pages | Delegated listener on `.btn, button`. Sends the button label and page title only. |
| `Lead` | `thank-you.html` | The booking confirmation step, as the compliance rules require. `sessionStorage` guard stops a refresh double-counting. |

`ViewContent` is the Meta API name. Events Manager displays it as "View Content".

Still missing before any spend: **Consultation attended**, fired manually or by CRM status change.
Without it the account optimises toward bookings that never show up. It cannot be done from the
site; it needs the Conversions API.

Never define a conversion event on the benefits form. Booking step only.

## Known gotchas

- **CSS source order.** These files have one long stylesheet with `@media(max-width:760px)` near
  the end. A rule appended after that block silently overrides the mobile rule at equal
  specificity. This has bitten twice: the team grid stayed 3 columns on a phone, and the sticky CTA
  never appeared. Put new base rules *before* the media query.
- **Local preview.** `python3 -m http.server` dies when the session ends. A broken image on
  `127.0.0.1` usually means a dead server, not a broken page. Verify on the Vercel URL.
- **Credential accuracy.** `brand/01-brand-facts.md` lists Alicia Bergen as an "Occupational
  Therapist". She is a COTA/L, a certified occupational therapy assistant. `team.html` uses her own
  wording. The brand facts file still needs correcting.
- **Multilingual gap.** The Wix site serves English, Spanish, Russian and Ukrainian on `en.` `es.`
  `ru.` and `uk.` subdomains. This demo is English only.

## Workflow

Plan before writing code. Build one page per step and tell me when each is done. Do not refactor
`dir-floortime.html` as a side effect of building another page.

Verify in a browser at 390px before saying a page is done. Checking that the CSS is present is not
the same as checking that it applies. Then commit and push; Vercel deploys on its own.
