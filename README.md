# Rill Habits V2 — Android project

Aplikasi Android native ringan untuk checklist harian, Daily Note, EXP/level, Workout, Workout Timer, Mood Harian, statistik, jadwal, dan pengingat lokal.

## Fitur V2
- Lima menu utama: Home, Checklist, Workout, Jadwal, Statistik.
- Daily Note disimpan lokal berdasarkan tanggal.
- Workout berulang berdasarkan hari kalender atau sesi sekali jalan berdasarkan tanggal.
- Program siap pakai: Beginner Movement, Bodyweight Basics, Walking & Jogging; dapat disesuaikan sebelum disimpan.
- Checklist per gerakan, detail set/repetisi, progres gerakan yang tersimpan, dan tombol penyelesaian sesi.
- Timer istirahat antar-gerakan dan timer bebas dengan atur durasi, mulai/jeda, lanjut, dan reset.
- Workout Streak menggunakan hari kalender: hari tanpa workout memutus streak; beberapa sesi pada hari yang sama tetap satu hari aktif. Rekor terbaik disimpan.
- Mood Harian skala 1–5 dengan catatan opsional dan kurva 7 hari/1 bulan.
- Pemicu Mood setelah seluruh item checklist harian (tugas dan workout) selesai; bisa dilewati atau diisi manual.
- Data disimpan lokal melalui SharedPreferences; tidak memerlukan akun atau internet untuk fitur utama.
- Package tetap `com.airil.rillrebirth` agar instalasi V2 dapat memperbarui V1 dan mempertahankan data lokal jika dipasang sebagai pembaruan.

## Build APK lewat GitHub Actions dari HP
1. Unggah seluruh isi folder project ini ke root repository GitHub (termasuk folder `.github/workflows`).
2. Buka tab **Actions**.
3. Pilih **Build Rill Habits V2 APK** lalu jalankan workflow, atau push perubahan ke branch `main`.
4. Setelah build sukses, buka hasil run dan unduh artifact **Rill Habits-V2-debug-APK**.
5. Ekstrak artifact dan instal `app-debug.apk` di HP. Saat memperbarui V1, jangan uninstall aplikasi lama karena data lokal dapat ikut terhapus.

## Status build
Source ini telah diperbarui, tetapi belum berhasil dikompilasi di lingkungan ini karena Android SDK dan Gradle tidak tersedia. Anggap APK belum terverifikasi sampai workflow GitHub Actions berhasil selesai. Setelah build, uji fungsi di perangkat Android 10.

## Catatan penggunaan
- Pengingat bergantung pada izin notifikasi dan pembatasan baterai Android/MIUI; alarm dapat terlambat.
- Workout yang diselesaikan memberikan 20 EXP sekali per sesi/tanggal. Mengubah status sesi tidak memberikan EXP kedua kali.
- Mood merupakan catatan refleksi, bukan diagnosis. Hari tanpa catatan dibiarkan kosong pada grafik.
- Streak bersifat ketat: diperlukan aktivitas workout pada setiap hari kalender untuk mempertahankan streak. Jangan memaksakan latihan berat saat perlu istirahat; gunakan aktivitas ringan yang sesuai kemampuan bila memilih mempertahankan streak.
- Backup/ekspor data belum tersedia. Menghapus data aplikasi atau uninstall dapat menghapus catatan lokal.
