# Creation to Revelation

An interactive timeline of the whole Bible: patriarchs, judges, the kings of Israel and Judah, the prophets, Jesus and the apostles, the books of the Bible, and the empires around them, from creation to about AD 100.

Live: https://gvannoorden.github.io/creation-to-revelation/

## What it does

- **Three levels of detail.** Overview (eras, empires, kingdoms, writing prophets), Standard (every patriarch, judge, king, prophet, apostle, and book), and Detailed (coregencies, every prophet, Paul's journeys, rulers, and emperors).
- **Gantt-style lanes** you can reorder and hide from the Lanes pop-out. Order and visibility are remembered in the browser.
- **Tap any bar** for dates, Scripture's verdict on each king, ESV links, the books it appears in, and everyone who overlapped it. Tap empty space to see everyone on the scene in a given year.
- **Book focus.** Pick a book and the chart filters and zooms to what it covers.
- **Color by** kingdom, verdict, or dynasty. Light and dark modes, with a manual toggle.

## Dates

Kings follow Thiele's chronology as refined by Rodger C. Young (JETS 48/2, 2005). Abraham through the judges are anchored on 1 Kings 6:1 and Exodus 12:40 (exodus 1446 BC; Merrill's *Kingdom of Priests*). Genesis 1–11 is drawn without a scale. Debated dates (Obadiah, Joel, the crucifixion, Revelation) can be shown with their main alternatives. The in-app **About** panel explains every choice.

## Tech

One self-contained `index.html`. No build step, no dependencies; only Google Fonts load from outside. Hosted on GitHub Pages from `main`.
