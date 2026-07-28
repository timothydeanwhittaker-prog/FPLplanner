Dugout — FPL Helper

A single-file, no-build Fantasy Premier League companion app. Open dugout.html on your phone or desktop and it just works — no server, no install, no account beyond your own FPL Team ID.

What it does
Dashboard — your starting XI on a pitch view, bench strip, captain/vice badges, next-fixture difficulty per player, team value, bank, and overall rank.
Transfers — a gameweek-by-gameweek captaincy log (your captain, your points, the overall average, the gap between them), a rolling "captaincy leak %" so you can catch a bad pattern early, and a searchable watchlist for players you're tracking.
DC Tracker — defensive contribution per 90 minutes for defenders, mids, and forwards, filterable by price, with a toggle to hide players already in your squad. Works even without a team loaded.
Planner — a mock transfer board. Swap any squad player for anyone in the full player pool, see your budget update live, and check a 6-gameweek fixture ticker for the hypothetical XI. Nothing here touches your real FPL team — it's a sandbox. Reset it back to your actual squad any time.
Getting started
Download dugout.html from this repo.
Open it directly in a browser — double-click it, or on mobile, open it from your Files app / add it to your home screen for an app-like feel.
Tap the ⚙ icon and either:
Enter your FPL Team ID (find it in the URL when you view your team on the official FPL site — fantasy.premierleague.com/entry/{YOUR_ID}/event/1) and tap Load my team, or
Tap Enter squad manually instead and paste your 15 players as name, position, price (one per line) if the live pull doesn't work in your browser.
Data & privacy

Everything the app stores — your Team ID, manual squad entries, watchlist, and any draft plan from the Planner — lives only in your browser's local storage. Nothing is sent anywhere except read-only calls to the public Fantasy Premier League API (fantasy.premierleague.com/api/). There's no backend, no analytics, no login.

A note on CORS

The FPL API isn't always reachable directly from a browser opening a local HTML file — some browsers block the request (CORS). If that happens:

The app automatically retries through a public CORS proxy (corsproxy.io).
If that also fails, use the manual squad entry fallback in Settings — the rest of the app (fixtures, DC tracker, planner) still works from there once the player pool has loaded.
Known limitations
The captaincy log currently pulls your last 6 completed gameweeks — older history isn't shown.
The Planner's fixture ticker shows all 15 squad players' next 6 fixtures, not just your starting XI specifically.
No live in-play score tracking or predictive points modelling — this is a planning and review tool, not a prediction engine.
Tech

Plain HTML, CSS, and vanilla JavaScript — no build step, no dependencies beyond two Google Fonts. Should run in any modern mobile or desktop browser.
