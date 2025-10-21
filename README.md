# Otomasi-Jaringan_network-interface-auto-disabler
Script Python untuk manajemen interface jaringan Linux. Secara otomatis mendeteksi dan menonaktifkan interface dengan status DOWN atau UNKNOWN menggunakan perintah ip link. Kompatibel dengan sistem berbasis Linux.

# 🧠 Project: Network Interface Auto Disabler

## 📘 Deskripsi
Program Python ini digunakan untuk **mengecek status semua network interface** pada sistem Linux dan **secara otomatis menonaktifkan interface yang tidak aktif (DOWN atau UNKNOWN)**.  
Cocok digunakan untuk **administrasi jaringan**, **otomasi sistem**, atau **pemeliharaan server**.

---

## ⚙️ Fitur Utama
- Mengecek semua interface jaringan menggunakan perintah `ip -br link`.
- Menonaktifkan interface yang tidak aktif dengan `sudo ip link set <interface> down`.
- Melewati interface `lo` (loopback).
- Menampilkan status setiap interface di terminal secara interaktif.

---

## 🧩 Persyaratan Sistem
- Sistem operasi: **Linux (Ubuntu, Debian, dsb.)**
- Python 3.x
- Hak akses `sudo`

---

## 📦 Instalasi
1. Pastikan Python sudah terpasang:
   ```bash
   python3 --version
2. Simpan file dengan nama: disable_inactive_interfaces.py
3. Beri izin eksekusi: python3 disable_inactive_interfaces.py

## hasil output ##
🔍 Mengecek status network interface...

✅ Interface aktif (dibiarkan):
   - enp0s3 (UP)

⚠️  Interface yang terdeteksi tidak aktif / tidak diperlukan:
   - dummy0 (DOWN)

Apakah kamu ingin menonaktifkan interface di atas? (y/n): y

🚧 Menonaktifkan interface yang tidak diperlukan...

🔴 Interface 'dummy0' telah dinonaktifkan.

✅ Semua interface tidak diperlukan telah dinonaktifkan.
