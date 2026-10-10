# Head Arrow Shot – Android project

A native Android shell (Kotlin + WebView) that runs the game offline from
`app/src/main/assets/index.html`. No ads, no internet permission.

## Run it
1. Open this folder in **Android Studio** (Koala or newer) and let Gradle sync.
2. Plug in a phone (USB debugging on) or start an emulator, then press **Run**.

## Publish it
- **Build > Generate Signed Bundle / APK > Android App Bundle** for Google Play.
- Keep your keystore file and passwords safe; you need them for every update.

## Customise
- Game code, levels and sounds: edit `app/src/main/assets/index.html`.
- App name: `res/values/strings.xml`. Package name: `app/build.gradle.kts`
  (`applicationId` and `namespace`) plus the folder/`package` line in `MainActivity.kt`.
- Icon: replace `android:icon` in `AndroidManifest.xml` with your own
  (Studio: right-click `res` > New > Image Asset).
- Version: bump `versionCode` / `versionName` in `app/build.gradle.kts` for each release.
