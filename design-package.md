# Solaris Energie Corporation — Design Package
Built for: a concept mockup a business can agree on. No backend, no database, no AI generation.

## 1. The brand premise

One word from the subject's own world: **sun-hour**. A sun-hour is one hour of full-strength
sunlight on one square metre. Most of the Philippines gets 4.5 to 5.5 a day. That number, times
the size of the array, is the electricity. Everything else is arithmetic. So the whole site sells
one idea: solar is not a leap of faith, it is a calculation, and Solaris is the company that shows
its working. Every claim on the page sits on a ruled line with its unit next to it. The pricing is
a range, not a promise. The payment schedule ties the last instalment to the net metering
certificate actually existing. Sun-hours in, pesos out.

## 2. Palette (sampled from the supplied photographs)

Sampled by downsampling each photo and bucketing by hue and lightness. Panel indigo #465a80 and
#4b6587 dominate three of the five shots; deep panel shadow #06041d and #0c192d are the darkest
three percent; golden hour peaks at #f09a00; foliage sits at #465a23.

```css
:root{
  --canvas:#080D1A;        /* deep panel shadow, tinted indigo. never pure black */
  --canvas-2:#0B1120;      /* alternating section wash */
  --panel:#111B2E;         /* cards and raised surfaces */
  --panel-2:#16223A;
  --line:#22314C;          /* the ledger hairline */
  --line-strong:#40567F;   /* interactive borders, 3:1 on canvas */
  --blue:#8CACE0;          /* panel indigo lifted. the structural voice */
  --blue-deep:#3F5C8F;
  --sun:#F7A423;           /* THE accent. CTA, money, rare emphasis */
  --sun-hi:#FFC65E;
  --leaf:#84D06E;          /* confirm ticks only */
  --text-primary:#E9EEF7;
  --text-secondary:#A6B6CF;
  --text-tertiary:#7C8FAE;
}
```

Three voices, not one, which is what keeps this off the stock "near-black plus amber" template:
indigo carries the structure, gold carries only money and the call to action, green only confirms.

## 3. Type trio

- **Display: Archivo**, variable, run at width 112 and weights 600/700. Industrial signage
  grotesque. Not Inter, not Roboto, and not a high-contrast serif.
- **Body: IBM Plex Sans** 400/500. Quiet, engineered, made by an engineering company.
- **Mono: IBM Plex Mono** 400/500. This is the ledger voice and it does real work here.

## 4. The hero

No generated film exists, so the journey is five real photographs moved by one continuous camera
in the browser. The camera only ever pushes in and descends, at a steady rate, across all five, so
the handoffs read as one travelling shot rather than a slideshow. Every handoff lands inside
motion and inside the gap between two beats, never under settled text (the seam law).

Journey: horizon, then site, then hands, then wiring, then the glass itself. Scrolling down reads
as descending and arriving. The final photograph is full-bleed texture, so nothing crops badly on
any screen, and the camera decelerates to a genuine stop at progress 1.

Hero height 900vh, so the scroll range is 800vh.

| Band | Range | Photo and camera | Copy (verbatim) | Entrance |
|---|---|---|---|---|
| 1 | 0.000–0.150 | hero-1, golden farm, slow push toward the sun | kicker `01 / IRRADIANCE` · "The sun over your roof is already free." · "Solaris builds the machine that catches it." | approach-from-depth |
| 2 | 0.175–0.325 | hero-2, hillside array, push continues, drifts down | `02 / SITE` · "Every roof gets measured before anything gets sold." · "Shade, pitch, azimuth, and your last twelve bills. The array is designed after that, not before." | grid snap-align |
| 3 | 0.350–0.500 | hero-3, three installers lifting a panel | `03 / BUILD` · "Installed by people whose names are on the permit." · "Licensed electricians. Registered business. Official receipt. Ask for any of it." | word-punch with overshoot |
| 4 | 0.525–0.675 | hero-4, overhead, wiring the inverter | `04 / THE PART NOBODY PHOTOGRAPHS` · "Panels almost never fail. Wiring does." · "Correct cable sizing, real breakers, surge protection, and a DC isolator you can actually reach." | weave |
| 5 | 0.700–0.845 | hero-5, water across the glass | `05 / AFTER` · "We come back. That is the whole difference." · "A wash, an inspection and a performance report twice a year, for as long as the array runs." | blur-to-sharp |
| 6 | 0.875–1.000 | hero-5 at rest, text lower left | `SOLARIS ENERGIE CORPORATION` · "Sun-hours in. Pesos out." · "Grid-tied, hybrid and off-grid solar for Philippine homes, resorts and businesses. Designed on your real bills. Built for your real weather." · buttons: Get a quote / See what it costs | word-by-word rise, staged settle |

Photo windows, with each crossfade centred in a gap between beats:
hero-1 0.000–0.185 · hero-2 0.140–0.360 · hero-3 0.315–0.535 · hero-4 0.490–0.710 · hero-5 0.665–1.000

## 5. The static hero (phones, portrait, coarse pointer, reduced motion)

Composed on hero-5, the resting frame, with the ledger rule and the settle copy.
Headline "Sun-hours in. Pesos out." Subline "Solar designed on your real bills and your real roof.
Philippine homes, resorts and businesses." CTA "Get a quote". Nothing else downloads.

## 6. Below-fold outline (funnels to one CTA: Get a quote)

1. **The bill.** "Nobody calls a solar company because they love solar." Three ledger stats.
2. **The unit.** The sun-hour explained, and **the one interactive moment**: hold the sun, run one
   day across a 5 kWp roof, watch sun-hours become kWh become pesos. Release early and it eases
   back. Complete it and the ledger lights up in sequence and reveals the payback line.
3. **Systems.** A ledger comparison of on-grid, hybrid and off-grid, including the honest row that
   an on-grid system shuts off during a brownout.
4. **Process.** Six steps on a self-drawing line, ending on the payment schedule 40/45/15 where the
   last fifteen percent is not due until the net metering certificate is in the owner's hand.
5. **Recent work.** The five photographs as an asymmetric grid with specs on ruled lines.
6. **Pricing.** 3, 5 and 10 kWp with real 2026 Philippine ranges, monthly saving and payback.
7. **FAQ.** The eight objections found in research, answered in the buyers' own words, including
   "magkano ba talaga", typhoons, brownouts, rainy season, net metering time, and what happens if
   the company closes.
8. **The form.** Name, mobile, city, property type, current monthly bill, message.
   Button "Get my quote". Success state names the person and the number back to them.
   **Handling: JS-only success state.** Nothing is sent anywhere. This is a mockup and the footer
   says so.
9. **Footer.** Contact, nav, and the disclosure that this is a concept mockup with placeholder
   figures and photographs.

## 7. The vector layer

All drawn by hand as inline SVG: the Solaris mark (sun rays over a panelled globe) used in the nav
and as the favicon, the irradiance arc that draws itself along the process timeline, the roof and
array diagram inside the interactive moment, ledger rules with tick marks, and whisper-level golden
motes in the fixed background environment layer. Everything honours reduced motion by showing its
final drawn state with the drives stopped.

## 8. The engineering list

dt-normalised lerp in a rAF loop that rests, delta-gated DOM writes, band pacing validated by the
flick test, the four-layer legibility system with a worst-frame audit at 3.5:1, the five
static-hero gates matched character for character in CSS and JS and kept live with change
listeners, complete-and-beautiful if the photographs never load, the whole-site-animated standard,
and the quality floor. There is no video, so the Blob loader and the loading ring are replaced by a
gated image preload on the same code path.

## 9. The copy gate

Every viewer-facing line above ships verbatim. The built page must pass the grep gate with zero em
dashes and zero stock words, plus the sweep for AI tells, before anyone sees it. The designed
devices here are craft and stay: "Sun-hours in. Pesos out." and "40 / 45 / 15."
