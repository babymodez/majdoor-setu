# Majdoor Setu - Android App

Ye ek Android app hai jo Majdoor Setu website ko andar se chalata hai. Website (`app/src/main/assets/index.html`) app ke saath bundle hai, isliye internet hosting ki zarurat nahi.

## Option 1: GitHub se APK (sabse aasan, bina Android Studio ke)

1. GitHub par free account banayein (github.com).
2. Ek naya repository banayein (jaise `majdoor-setu`) aur is folder ki saari files upload karein.
3. Repository mein **Actions** tab kholein. "Build Majdoor Setu APK" workflow apne aap chalega (ya **Run workflow** dabayein).
4. Lagbhag 5 minute baad workflow complete hoga. Uske andar **Artifacts** mein `majdoor-setu-apk` milega. Use download karein, usme `app-debug.apk` hogi.
5. Ye APK file WhatsApp, email ya Google Drive se kisi ko bhi bhej sakte hain.

## Option 2: Android Studio se APK

1. Android Studio install karein (developer.android.com/studio).
2. **Open** dabayein aur is folder ko chunein. Sync hone dein.
3. **Build → Build Bundle(s) / APK(s) → Build APK(s)** chunein.
4. APK `app/build/outputs/apk/debug/app-debug.apk` mein banegi.

## Phone par install kaise karein

1. APK file phone par download karein.
2. File par tap karein. Pehli baar phone poochega "Unknown apps se install allow karein" — **Allow** karein.
3. **Install** dabayein. Ho gaya.

## Dhyan dein

- Ye debug APK hai. Google Play Store ke liye signed AAB chahiye (Android Studio → Generate Signed Bundle).
- Kuch phones par "Play Protect" warning aa sakti hai, kyunki app Play Store se nahi hai. "Install anyway" chunein.
- Data abhi phone ke andar (localStorage) save hota hai, server par nahi. Doosre users ke saath data share karne ke liye backend (Firebase / Supabase) chahiye.
- Location ke liye app pehli baar permission maangegi.
