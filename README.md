# Math Arcade
A self-contained, kid-friendly math arcade for Johnny. No dependencies, accounts, trackers, paid assets, or build step.

## Open
Open `index.html` directly to play, or serve this folder:

    cd /workspace/math-arcade
    python3 -m http.server 8080

Visit http://localhost:8080. For a normal public website link, upload this folder to any static HTTPS host. No deployment or GitHub push has been performed.

## Install / offline
Settings contains install instructions and a browser install button when supported. Android/desktop: Install app from browser menu. iPad/iPhone: Safari > Share > Add to Home Screen. PWA/offline requires HTTPS (or localhost), not file://. Visit once online to cache the shell. PNG icons, manifest, and service worker are included. All gameplay and music are self-contained and run offline afterward.

## Play
- Pick your display name. Click Music to start procedural chiptune audio (browsers require a gesture). It is muted by default.
- Math: select long multiplication/division and 2–5 digits. Main operand/dividend has the selected length. Multipliers are two digits; divisors are one/two digits, with exact integer results. Correct answers earn 100 XP and 10 coins. Retry without penalty. Hints explain the long-form method.
- Spend 1,000 available XP on any arcade unlock. Lifetime XP and spent XP remain separately tracked. Unlocks never expire.
- Target Master: tap or drag/release to shoot the moving lime bullseye. Keyboard arrows aim, Space shoots. Five consecutive center hits wins; miss ends the round. Restart anytime.
- Bumper Smash: choose a car color. Hold arrows or on-screen direction buttons; swipes also move. Fast rams damage three rivals more than they hurt you; staying still is dangerous. Clear all rivals before your 100 life runs out.
- Neon Skate: survive 30 seconds. Left/right changes lanes; up jumps orange crates, down ducks blue gates. Swipes and buttons work. Fire board costs 200 coins and clears your lane using Space/Fire, with a three-second recharge. Basic board can win without purchases.
- Every arcade win gives 20 arcade points and 25 coins, once per round. Restart to earn again.
- Top 10 is local to this browser, ranked by arcade points. Settings changes display name for another local player; XP, unlocks and wallet remain shared. No online/global scores or cloud sync. Clearing site data resets progress.

## Files
index.html, style.css, app.js, manifest.webmanifest, sw.js, icon-192.png, icon-512.png, README.md.

## Verification performed
- JavaScript and service-worker syntax checks passed.
- Headless Chromium: completed 10 real math answers, verified 1,000 XP / 100 coins, spent XP on unlocks, opened/restarted all three games, reloaded persisted progress, and opened leaderboard/settings. No uncaught page errors.
- Verified 390px mobile viewport has no horizontal overflow; inspected the full hub screenshot.
- Automated five-bullseye streak earned 20 points. Purchased/equipped Fire board and completed a 30-second skate challenge for another 20 points.
- Exercised Bumper Smash steering, collisions, enemy eliminations, HP loss, and loss/restart path. Bumper victory branch is implemented but was not independently completed by the automated steering bot.
- Verified offline service-worker cache and manifest/icon files. Actual device home-screen installation and physical touch/audio listening still need on-device acceptance testing.
