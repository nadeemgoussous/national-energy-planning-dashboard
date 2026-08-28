# National Energy Transition Planning Dashboard — preview

A live preview of a single self-contained web dashboard cataloguing national
long-term energy planning documents (LTES / LT-LEDS) and the modelling tools used
to produce them.

**▶ [Open the dashboard](https://nadeemgoussous.github.io/national-energy-planning-dashboard/)**

Catalogue built 2026-08-13: **269 documents** across **142 countries**, citing
**154 modelling tools**, 149 of which have a register entry.

## What this repository is

A hosting stub, nothing more. It carries the dashboard —
`webdash/dist/national-energy-planning-dashboard.html` — and the three CSV files it
reads, so that it can be opened and reviewed in a browser without downloading
anything. `index.html` only redirects to it, forwarding the URL hash so deep links
keep working.

Those files are **generated**, and the things that generate them are not in this
repository: the build script, the page source, and the Excel workbook the data comes
from all live in IRENA's internal project folder. Editing the HTML here would be
overwritten on the next build.

The page reads its catalogue from `Documents.csv`, `Doc_Tools.csv` and `MT_Key.csv`
in its own folder, which is how the data can be refreshed without rebuilding the
page. It also carries a full copy of that data inlined as a fallback, along with the
world geometry, styles and scripts — so opened from a file share, a USB stick or
offline, where those files cannot be read, it still works and says so in its footer.
It makes no requests to any other origin.

## Status

This is a **working preview, not an official IRENA publication.** It is intended to
replace the Power BI embed on
[the public IRENA page](https://www.irena.org/Energy-Transition/Planning/Long-term-energy-planning-support/National-Energy-Transition-Planning-Dashboard),
but has not been through IRENA sign-off, and the URL above is a personal GitHub Pages
site rather than an IRENA one. Treat figures as provisional.

## Map boundaries

The map is drawn from a generic [Natural Earth](https://www.naturalearthdata.com/)
110m Admin-0 derivative (public domain), **not** from an official UN boundary layer.
It is a shape source, not a statement about which countries exist or where their
borders run.

> The designations employed and the presentation of materials herein do not imply the
> expression of any opinion on the part of IRENA concerning the legal status of any
> region, country, territory, city or area or of its authorities, or concerning the
> delimitation of frontiers or boundaries.

## Data

The catalogue is IRENA's. It is published here for review only; all rights in the
underlying data remain with IRENA. Each of the three tables can be exported as CSV
from the dashboard itself, filtered exactly as shown on screen.
