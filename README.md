# BladiFix — projet APK (Capacitor)

Contenu : `www/` (index.html, style.css, app.js, assets/) + `capacitor.config.json` + `package.json`.
Test navigateur : ouvrir `www/index.html` (ou `npx serve www`).

## Générer l'APK
Prérequis : Node.js 18+, Android Studio (SDK + JDK 17).
1. `npm install`
2. `npx cap add android`
3. `npx cap sync android`
4. Ajouter dans `android/app/src/main/AndroidManifest.xml` (avant `<application>`) :
   `<uses-permission android:name="android.permission.CAMERA"/>`
   `<uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>`
   `<uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION"/>`
5. `npx cap open android` puis Android Studio : Build > Build Bundle(s)/APK(s) > Build APK(s).
   L'APK est dans `android/app/build/outputs/apk/debug/app-debug.apk`.

## Sans Android Studio
Zipper le dossier `www/` et l'envoyer sur https://www.pwabuilder.com ou un convertisseur web-vers-APK.
