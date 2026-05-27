# esp-minecraft

Halo sobat digital!!

ini adalah versi **bareiron yang udah disiapin biar tinggal upload di PlatformIO** 😭🔥

jadi tujuan repo ini simpel:

> clone → buka di VSCode → upload ke ESP32-C3 → jalan

project ini adalah port / versi siap pakai dari bareiron Minecraft server, jadi kamu gak perlu ribet setup manual yang aneh-aneh.

---

# ⚠️ DISCLAIMER

project ini adalah:

MAKSA BIKIN SERVER MINECRAFT DI BENDA YANG LEBIH KECIL DARI KOREK GAS YANG SERING ILANG DI WARUNG ITU!!!

---

# 🎯 TUJUAN PROJECT

- bikin bareiron versi yang gampang dipakai
- target ESP32-C3
- langsung jalan di PlatformIO
- gak perlu setup build manual yang ribet
- fokus ke konsep **plug and play flash & run**

---

# 🧠 BASE PROJECT

project ini berdasarkan:

https://github.com/p2r3/bareiron

bareiron = Minecraft server minimal untuk device embedded low memory

---

# 🚀 CARA INSTALL

## 1. Install PlatformIO

install VSCode + extension PlatformIO:

https://platformio.org/install/ide?install=vscode

---

## 2. Clone Repository

```bash
git clone https://github.com/ngulikom/esp-minecraft
cd esp-minecraft
```

---

## 3. Buka di VSCode

- buka folder project
- tunggu PlatformIO indexing selesai

---

## 4. Pastikan Board ESP32-C3

cek file:

```ini
platformio.ini
```

isi minimal:

```ini
[env:esp32-c3]
platform = espressif32
board = esp32-c3-devkitm-1
framework = espidf
monitor_speed = 115200
```

---

## 5. Setup WiFi

edit file:

```c
include/globals.h
```

isi:

```c
#define WIFI_SSID "nama_wifi_kamu"
#define WIFI_PASS "password_wifi_kamu"
```

---

## 6. Upload ke ESP32

klik di PlatformIO:

- `Upload`

atau via terminal:

```bash
pio run -t upload
```

---

## 7. Monitor Serial (optional)

```bash
pio device monitor
```

---

# 🎮 CARA KERJA

ESP32-C3 akan:

- connect ke WiFi
- menjalankan Minecraft server minimal
- menerima koneksi client Minecraft
- menjalankan logic server sederhana

flow:

```text
Minecraft Client → ESP32-C3 Server
```

---

# ⚙️ FITUR

- ESP32-C3 support
- PlatformIO build system
- WiFi configurable
- Minecraft server minimal implementation
- simple embedded networking stack

---

# 🔥 LIMITASI

karena ESP32:

- RAM sangat terbatas
- chunk generation sangat minimal
- player count kecil
- fitur vanilla tidak lengkap
- eksperimen saja, bukan server production

---

# 💡 CATATAN PENTING

kalau error:

- cek WiFi credential
- pastikan board ESP32-C3 benar
- jangan paksa multiplayer terlalu banyak
- monitor serial buat debug

---

# 🧠 KONSEP BESAR

project ini ngebuktiin:

> Minecraft server bisa jalan di chip ESP32 😭🔥

---

# 🎬 CLOSING

kalau ini jalan…

berarti kita sudah masuk era:

> "Minecraft server di hardware receh"

---

Fork base: https://github.com/p2r3/bareiron  
Port by: Ngulikom
