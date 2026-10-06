# Skyglass (Android)

## Option A: no Android Studio (GitHub builds the APK)
1. Create a free GitHub account and a new repository.
2. Upload this whole folder to it (branch: main).
3. Open the Actions tab, wait for "Build APK" to finish (3-5 min).
4. Open the finished run, download the artifact "skyglass-apk", unzip it.
5. Send app-debug.apk to your phone and install it (allow "install unknown apps").

## Option B: Android Studio
Requires Node 18+, JDK 17 and Android Studio.
    npm install
    npx cap add android
    npx cap sync android
    npx cap open android
Then Build > Build APK(s).

## Changing the game
Edit www/index.html, then run `npx cap sync android` and rebuild.

## Play Store
The debug APK is for personal installs. For the Play Store build a signed
release AAB (Build > Generate Signed Bundle) and add your own app icon.
