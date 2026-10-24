# HomeLauncher

A tiny, fast Android TV home screen: clock, date and a grid of your apps.
No recommendations, no YouTube history, no ads, no internet access.

## Get the APK (no Android Studio needed)

1. Create a free account at github.com and a new empty repository (private is fine).
2. Upload everything from this folder into the repository, including the hidden
   `.github` folder (drag and drop the files into "Add file -> Upload files").
3. Open the **Actions** tab, wait for "Build APK" to finish (about 3-5 minutes).
4. Open the finished run and download **HomeLauncher-apk** (a zip with `app-debug.apk`).

## Install on the stick

    adb connect 192.168.1.54:5555
    adb install app-debug.apk
    adb shell am start -n app.homelauncher/.MainActivity

Press Home and choose "Home" as the default launcher when asked. If the system
does not ask, keep the stock launcher enabled and use the launcher's own entry
from the apps list. Only disable the stock launcher after this one works.

## Use

- OK on a tile opens the app. Hold OK on a tile to open its app info.
- To hide an app, add its package name to `HIDDEN` in `MainActivity.java`.
