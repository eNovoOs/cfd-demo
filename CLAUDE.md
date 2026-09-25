# CFD demo site

Static HTML demo of a new website for Child & Family Development, a pediatric therapy practice
in Oakland, New Jersey that also runs a preschool. Not the other way around.

This is shown to the client in a meeting. No build step, no framework, no npm, no bundler.
Each page is one self-contained .html file with its CSS in a `<style>` block, exactly like
`dir-floortime.html`.

All client-facing copy is US English.

## Design source, read this first

`dir-floortime.html` is the approved design and it is already built. Read it before writing
anything. Copy its CSS, its components, its spacing and its section rhythm into every new page.
Do not invent new visual patterns, do not restyle it, do not "improve" it. If a new page needs a
component that does not exist there, build it in the same language and tell me what you added.

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

## Scope of this demo

- All internal links must resolve to a file that exists in this folder.
- Forms do not submit anywhere. The submit button is a link to `thank-you.html`.
- No analytics, no pixel, no tracking script, no API calls, no external requests except the
  Google Fonts stylesheet already used in `dir-floortime.html`.
- Photo placeholders stay as placeholders. Never use stock photography or AI generated images of
  children. The placeholder itself says what photo goes there.
- Responsive matters: these parents read on a phone. Every page must work at 390px wide.

## Workflow

Plan before writing code. Build one page per step and tell me when each is done. Do not refactor
`dir-floortime.html` as a side effect of building another page.
