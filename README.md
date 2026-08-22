# Solaris Energie Corporation

Website for Solaris Energie Ventures Corporation, a solar EPC and maintenance
company registered with the Philippine SEC in March 2022 (Reg. No. 2022030044923-87).

## What is here

    solaris-site/            the website. This folder IS the deployable site.
      index.html             every section, style and script in one file
      assets/                logo, hero photo
      assets/projects/       17 project photos cropped from the company profile
    projects.json            the 42 projects as data. Edit this to add more.
    design-package.md        design decisions and brand tokens

## Running it

No build step and no dependencies. Open the file directly:

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
- Payment schedule and warranty terms.
- Legal name: the logo reads "Corporation", the SEC record reads
  "Ventures Corporation".

The electricity rate (14.96 per kWh, Visayan Electric) and the whole project
list are real.
