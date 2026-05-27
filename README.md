# esp-minecraft
# bareiron-esp32 (PlatformIO Ready Port)

Halo sobat digital!!

ini adalah versi **PlatformIO-ready port** dari project bareiron Minecraft server 😭🔥

jadi tujuan repo ini simpel:

> ESP32-C3 langsung jalan sebagai Minecraft server tanpa setup ribet

---

# ⚠️ DISCLAIMER

project ini:

- experimental Minecraft server implementation
- tidak 100% vanilla compliant
- performa tergantung ESP32 (RAM & WiFi)
- cocok untuk riset, eksperimen, dan konten Ngulikom

---

# 🎯 TUJUAN PROJECT

- bikin bareiron bisa langsung dipakai di PlatformIO
- target ESP32-C3
- hapus proses build manual yang ribet
- fokus ke "plug and play flash & run"

---

# 🧠 BASE PROJECT

project ini berdasarkan:

https://github.com/p2r3/bareiron

bareiron = Minecraft server minimal untuk device embedded low memory

---

# 🚀 CARA INSTALL

## 1. Install PlatformIO

Install VSCode + extension PlatformIO:

https://platformio.org/install/ide?install=vscode

## 2. Clone Repository

```bash
git clone https://github.com/your-repo/bareiron-esp32
cd bareiron-esp32
```

## 3. Buka di VSCode

- buka folder project
- tunggu PlatformIO indexing selesai

## 4. Pastikan Board ESP32-C3

cek file:

`platformio.ini`

isi minimal:

```ini
[env:esp32-c3]
platform = espressif32
board = esp32-c3-devkitm-1
framework = espidf
monitor_speed = 115200
```

## 5. Setup WiFi

edit file:

`include/globals.h`

isi:

```c
#define WIFI_SSID "nama_wifi_kamu"
#define WIFI_PASS "password_wifi_kamu"
```

## 6. Upload ke ESP32

klik di PlatformIO:

- Upload

atau via terminal:

```bash
pio run -t upload
```

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

Minecraft Client → ESP32-C3 Server

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
- jangan paksa multi player terlalu banyak
- monitor serial untuk debug

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
