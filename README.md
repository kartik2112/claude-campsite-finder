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

## Notes
- One check sends about 75 requests (4 at a time). Results are cached in your browser for 15 minutes per date.
- Your date, filters and Interested / Not interested choices are saved in localStorage until you press Reset.
- These APIs are unofficial. If one changes its format, those cards show "Check failed".
