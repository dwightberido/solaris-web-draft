# Solaris Energie Corporation

Website for Solaris Energie Ventures Corporation, a solar EPC and maintenance
company registered with the Philippine SEC in March 2022 (Reg. No. 2022030044923-87).

## What is here

    solaris-site/            the website. This folder IS the deployable site.
      index.html             every section, style and script in one file
      assets/logo.png        the logo
      assets/gen/            generated placeholder photos and the hero video loop
                             (hero, three system types, survey, maintenance, cell macro).
                             Replace with photos of Solaris crews and sites before launch.
      assets/projects/       16 real project photos cropped from the company profile
    projects.json            the 41 projects as data. Edit this to add more.
    design-package.md        design decisions and brand tokens
    mockups/                 the palette and effect mockups the owner chose from
    originals/               the source files the content came from

## Running it

No build step. The motion layer loads GSAP, ScrollTrigger and Lenis from
jsDelivr at runtime; without a connection the page still renders with
everything visible and static. Open the file directly:

    open solaris-site/index.html

Or serve it, which is only needed to view it from a phone on the same wifi:

    cd solaris-site
    python3 -m http.server 8899

## Deploying

Upload the CONTENTS of `solaris-site/` so that `index.html` sits at the top
level with `assets/` beside it.

## Adding projects

Append an object to `projects.json`, then regenerate the `PROJECTS` array
inside `index.html`. Fields: y, seg (ci|res), st (done|ongoing), kwp, kwh, mod,
role, what, where, client, when, photo, feat, cap, name, loc.

## Still to confirm with the owner

- Installed cost per kWp. The calculator currently uses a published market
  range, not Solaris pricing. This drives cost, payback and 25-year savings.
- The phone number in the footer is a placeholder.
- Payment schedule.
- Site survey fee outside Cebu (free within Cebu is confirmed; the site shows TBD).
- Whether the 5 year inverter and battery warranties are manufacturer-backed (the site shows TBD).
- Legal name: the logo reads "Corporation", the SEC record reads
  "Ventures Corporation".

The electricity rate (14.96 per kWh, Visayan Electric) and the whole project
list are real.
