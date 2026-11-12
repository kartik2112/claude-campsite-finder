# Bay Area Campsite Finder

Static page that checks live campsite availability in your browser.

## Publish on GitHub Pages
1. Create a new repository (for example `campsite-finder`) and push all the files in this folder.
2. In the repository, open **Settings → Pages**. Set **Source** to "Deploy from a branch", branch `main`, folder `/ (root)`. Click **Save**.
3. Open `https://<your-user>.github.io/campsite-finder/` after about 1 minute.

## Live sources (called from your browser)
- Recreation.gov availability API: 14 campgrounds
- ReserveCalifornia (Tyler RDR) API: 27 campgrounds
- Campflare page for Del Valle (East Bay Parks): 1 campground

7 campgrounds have no live check (Doran: CAPTCHA; Ventana, Big Sur Campground & Cabins, Riverside, Fernwood: private booking systems; Veterans Memorial Park, Laguna Seca: city/county).

## Features
- Check-in / check-out dates: a site counts as open only if it is free on every night of the stay and the stay meets its minimum-night rule.
- Grid view: open sites per campground per day. Filter start days (Saturdays, Fridays, Fri+Sat, Sun–Thu) and nights (1–4). Scroll right to load later dates.
- Availability is stored in this browser with no expiry. "Fetch latest availability" refetches only data older than 15 minutes.
- Minimum stay: ReserveCalifornia per-night MinStay, Recreation.gov weekend / holiday rules.

## Notes
- Data is fetched one calendar month at a time per campground (Recreation.gov: 1 request; ReserveCalifornia: 2 per facility; Campflare: 1), 4 requests at a time.
- Your date, filters and Interested / Not interested choices are saved in localStorage until you press Reset.
- These APIs are unofficial. If one changes its format, those cards show "Check failed".
