# Timeshifter: jet lag planner

A single-page jet lag planner. Add your flights and it builds a day-by-day plan
for sleep, light, caffeine and melatonin, from a few days before you fly until
you're adjusted.

- **New trip**: add screenshots of your booking and Claude reads the flights,
  or type them in. Add your usual bedtime and wake-up time, and say whether you
  take melatonin.
- **Right now** card: what to do at this moment and what's coming up, updated live.
- Switch the times between your home city and your destination.
- Trips are saved, so you can use it for every trip.

Reading screenshots needs Claude, so it only works when the page is opened as a
Claude artifact. On GitHub Pages you can type flights in by hand, and trips are
saved in that browser.

## How the plan is made

The planner estimates where your body clock's low point is each night (about
2 hours before you'd naturally wake). It then places light before or after that
point to move your clock the right way, by about 1–1.5 hours a day. It starts a
day or two before you fly and continues at your destination. Eastward trips of
10+ hours are shifted the other way round, because that's quicker.

- Caffeine is fine until about 7 hours before each main sleep.
- Melatonin, for shifts of 3+ hours:
  - Moving the clock earlier: take it before the shifted bedtimes.
  - Moving the clock later: take it only if you wake in the night and can't
    get back to sleep.

The built-in KL → London trip (23 Sep 2026) follows the Timeshifter app's own plan.

This is general guidance, not medical advice.

## Publishing on GitHub Pages

Settings → Pages → Build and deployment → Source: GitHub Actions (or deploy from
the `main` branch). Every push to `main` then updates the site.
