# BotSpot

Project Android WebView siap di-build menjadi APK.

## Kenapa bukan file .apk langsung?
APK yang bisa diinstall harus dikompilasi (Java -> DEX) dan ditandatangani (signing)
dengan Android SDK. Itu tidak bisa dilakukan di dalam browser. File .apk "palsu"
hasil rename ZIP selalu ditolak Android dengan pesan "Tidak dapat mengurai paket".

## Cara 1 - Android Studio (paling mudah)
1. Ekstrak ZIP ini
2. Android Studio > Open > pilih folder hasil ekstrak
3. Tunggu Gradle sync selesai
4. Build > Build Bundle(s)/APK(s) > Build APK(s)
5. APK ada di: app/build/outputs/apk/debug/app-debug.apk

## Cara 2 - Tanpa install apa pun (GitHub Actions)
1. Upload isi folder ini ke repository GitHub baru
2. Buka tab Actions, jalankan workflow "Build APK"
3. Setelah selesai, download artifact APK-nya

## Cara 3 - Command line
gradle assembleDebug

## Info aplikasi
- Nama: BotSpot
- Package: com.app.botspot
- Versi: 1.0.0
- Orientasi: portrait
- Warna tema: #6366f1

## Install di HP
Aktifkan "Install dari sumber tidak dikenal", lalu buka file APK hasil build.
