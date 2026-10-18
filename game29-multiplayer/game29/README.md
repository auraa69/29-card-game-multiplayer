# 29 Card Game - Android guide

The game is a web app, so it already runs in any phone browser. Three ways to get it on Android:

## 1. Deploy the server (needed for multiplayer, do this first)
1. Put this folder on GitHub.
2. render.com -> New -> Web Service -> pick the repo. Build command: npm install. Start command: npm start.
3. You get an https link like https://my-29.onrender.com . Free plan sleeps when idle; the first open can take ~30 s.

## 2. Install like an app (easiest, no APK)
Open the link in Chrome on Android -> menu (three dots) -> Install app / Add to Home screen.
It opens full screen with its own icon. Everyone in the family does the same and joins the same room code.

## 3. Real APK (optional)
Option A - PWABuilder: go to pwabuilder.com, paste your https link, choose Android, download the package, sign and install it.
Option B - Capacitor (needs Android Studio):
    npm i -D @capacitor/cli @capacitor/core @capacitor/android
    set SERVER_URL in public/config.js to your https link
    npx cap init "29 Card Game" com.yourname.game29 --web-dir public
    npx cap add android
    npx cap sync
    npx cap open android      (then Build > Build APK in Android Studio)

## Run on your PC for testing
    npm install
    npm start        # http://localhost:3000
