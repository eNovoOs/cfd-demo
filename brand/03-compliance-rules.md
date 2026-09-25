# Advertising compliance rules

This account advertises a health service to parents of children with disabilities. It sits in the most scrutinised corner of Meta's policy surface. Breaking these gets creative rejected, and repeated breaches restrict the ad account.

## Copy rules

**Never assert or imply knowledge of a reader's health condition.**

| Never write | Write instead |
|---|---|
| "Does your child have autism?" | "A preschool built for children who need more support." |
| "Is your child struggling in preschool?" | "Families come to us when a big classroom is not working." |
| "For kids with sensory issues" | "Support for sensory, feeding and regulation needs." |
| "Has your child been diagnosed?" | "Our day programme serves children aged 3 to 6 with an autism diagnosis." |

The test: describe the programme and who it is built for. Never address a diagnosis back to the reader in the second person.

## Other hard rules

- No before-and-after framing, in image or copy, including in testimonial creative.
- No outcome guarantees and no comparative durability claims. No "proven", "guaranteed", "results in weeks", "lasts longer".
- The Playful Pathways Project is research in progress, never evidence in hand. Correct: "we are studying how relationship-based therapy changes the developing brain." Incorrect: "our therapy changes the brain."
- Never say "covered by insurance". Say "we verify your out-of-network benefits".
- Never name a specific competing business. The ABA *category* may be named, because the client already positions the day programme as "a therapeutic alternative to traditional preschool or ABA" on its own site. Name the category as a description of what CFD does, never as an attack on another provider.
- Written consent on file before any child appears in paid media.
- The landing page must match the ad. Meta reviews the destination.
- Text coverage under 20% of the canvas. Meta no longer rejects on this but delivery still degrades above it.

## Special Ad Category

Childcare and therapy are not housing, employment, credit or social issues. This account should **not** be in a Special Ad Category. If it has been flagged into one, get it out before launch or radius targeting disappears, which kills the five-mile strategy.

## Data handling

The benefits-verification form collects a child's first and last name, date of birth, autism diagnosis status, primary concerns, insurance policy number and an insurance card upload.

- None of that may enter a pixel event parameter, an ad platform, or a CRM field that syncs to one.
- That form must not fire a standard conversion event carrying any of those fields.
- Define conversion events on the booking step, not on the benefits form.

## Events to define before spend

1. **Consultation booked**. The booking confirmation step.
2. **Consultation attended**. Fired manually or by CRM status change.

Without the second event the account optimises toward bookings that never show up, which is exactly the failure already happening manually.

## Creative specification

| Element | Spec |
|---|---|
| Canvas | Build 1:1 first, extend the background for 4:5 and 9:16 |
| Safe area | 12% inset on all four edges |
| Logo | Knockout lockup top-left on dark, colour lockup on light. Width about 26% of canvas. Never the mark alone. |
| Headline | Montserrat 600, max three lines, manual line breaks |
| CTA pill | Bottom-left, 999px radius. White on dark, navy on light. Pink only for the single highest-intent unit. |
| Contrast | All text at or above 4.5:1 against the pixel behind it, checked over the photo rather than the base colour |
