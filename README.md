# Pit Wall for Android

Formula 1 timing, telemetry, track maps and tyre strategy, using live data from the free OpenF1 API (2023 season onwards). The app wraps the Pit Wall web page (`app/src/main/assets/index.html`) in a full-screen WebView. It needs an internet connection.

## Option A: build in Android Studio

1. Unzip this folder and open it in Android Studio (File > Open, then pick the `pitwall-android` folder).
2. Let Gradle sync finish. The first sync downloads the Android build tools, so it can take a few minutes.
3. Plug in your phone with USB debugging on, then press Run. Or use Build > Build APK(s) and copy the APK to your phone.

## Option B: let GitHub build the APK

1. Create a new GitHub repository and upload the contents of this folder, including the hidden `.github` folder.
2. Open the repository's **Actions** tab. The "Build Pit Wall APK" run starts by itself on every push.
3. When it finishes, download **PitWall-apk** from the run's page. Unzip it, copy `app-release.apk` to your phone and open it. Android asks you to allow installs from that source the first time.

## Updating the app

Edit `app/src/main/assets/index.html` (the same file as the website) and rebuild.

## Before publishing to Google Play

The release build is signed with the debug key so it installs right away. For Google Play, create your own keystore (Build > Generate Signed App Bundle) and build an `.aab` file instead.
