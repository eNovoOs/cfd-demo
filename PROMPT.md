# The prompt

Open a terminal in this folder, run `claude`, and paste everything between the lines below.

---

Read CLAUDE.md, then read dir-floortime.html in full, then read brand/01-brand-facts.md,
brand/02-messaging-bank.md and brand/03-compliance-rules.md.

dir-floortime.html is the approved design and is already finished. Do not modify it. Reuse its
CSS, its components and its spacing for everything you build.

Build four new pages in this folder, in this order, telling me when each one is done:

1. harbor-academy.html
   The Harbor Academy program page. Accent colour is Meadow Green instead of the Floortime pink.
   Sections: header with nav; hero with the headline "More support. Still preschool." and the
   support line about a small play-based classroom founded by an occupational therapist; a key
   facts strip; a "What a day looks like" section; a "Who it is for" section aimed at a parent
   whose child needs more support than a large classroom gives, with or without a diagnosis; the
   founder section; tuition stated openly at $2,950 a month, $3,700 with extended hours, private
   pay with no insurance approval to wait on; an FAQ; and the booking form block. Do not mention
   the 1:3 ratio anywhere.

2. therapies.html
   Individual therapies, birth to 21, any diagnosis. Accent colour is Sky. Cover occupational
   therapy, DIR/Floortime sessions, feeding therapy and aquatic therapy, each with a short plain
   description, plus the two-week and one-month intensives and remote parent training. Payment is
   out-of-network, superbill or single case agreement. This page sells to families already in the
   practice and to people outside the area, so it is calmer and less urgent than the program pages.

3. index.html
   The home page. Its only job is to route three different parents to the right place: a parent
   with no diagnosis to Harbor Academy, a parent with an autism diagnosis to the DIR/Floortime day
   program, and a family with a specific need to individual therapies. Sections: short hero, three
   program cards using each program's accent colour, a short section on what makes this practice
   different, the founder, a trust strip, footer. No booking form on the home page, only links.

4. thank-you.html
   Short confirmation page. The consultation is booked, what happens next in three steps, the
   address and phone, and one line on what to expect at the visit. Same design system, no nav
   pressure, no second offer.

Then wire the site together: the header nav and the footer must be identical across all five
pages and every link must resolve. Every form submit button links to thank-you.html.

Finally, run a check over all five pages and report back:
- every internal link resolves to a file that exists
- the colour logo is used on light backgrounds and the white one on dark
- no page has more than one pink button
- no copy breaks the rules in brand/03-compliance-rules.md
- no invented numbers, prices, ratios or claims
- every page works at 390px wide

List anything you marked TBC and anything you had to decide on your own.

---

## To view it

```bash
npx serve .
```

Then open the address it prints. `python3 -m http.server 8000` works too if you prefer no
dependencies.

## If you want to keep going after the demo

Ask for `fairfield.html` (waitlist page, no opening date because there is none yet),
`playful-pathways.html` (the research project, with donation traffic kept separate from
enrolment traffic), `about.html` and `contact.html`.
