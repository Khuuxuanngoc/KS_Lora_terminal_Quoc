# Arduino_Project_Template# ESP32-S3 Dev Kit LoRa – Hshop MKE-M23 & MKE-M24

## 📌 Giới thiệu

Repo này được xây dựng để sử dụng **ESP32-S3 Dev Kit** với các module LoRa của Hshop:

* **MKE-M23** – Ai-Thinker **Ra-02 Breakout Board**
* **MKE-M24** – Ai-Thinker **Ra-01SH Breakout Board**

Repo sử dụng thư viện **RadioLib** để điều khiển và giao tiếp với các module LoRa.

---

## 📦 Phần cứng

### ESP32-S3 Dev Kit

### MKE-M23 – Ai-Thinker Ra-02

Module LoRa sử dụng chip **SX1278**.

### MKE-M24 – Ai-Thinker Ra-01SH

Module LoRa sử dụng chip **SX1262**.

---

## 🔌 Kết nối ESP32-S3 với MKE-M23

| MKE-M23 (Ra-02) | ESP32-S3 Dev Kit |
| --------------- | ---------------- |
| NSS             | GPIO10           |
| MOSI            | GPIO11           |
| SCK             | GPIO12           |
| MISO            | GPIO13           |
| DIO0            | GPIO16           |
| RST             | GPIO17           |
| DIO1            | GPIO15           |

### Sơ đồ kết nối

```text
ESP32-S3 Dev Kit          MKE-M23 (Ra-02)
─────────────────         ───────────────
GPIO10  ───────────────── NSS
GPIO11  ───────────────── MOSI
GPIO12  ───────────────── SCK
GPIO13  ───────────────── MISO
GPIO16  ───────────────── DIO0
GPIO17  ───────────────── RST
GPIO15  ───────────────── DIO1
GND     ───────────────── GND
3.3V    ───────────────── VCC
```

---

## 🔌 Kết nối ESP32-S3 với MKE-M24

| MKE-M24 (Ra-01SH) | ESP32-S3 Dev Kit |
| ----------------- | ---------------- |
| NSS               | GPIO10           |
| MOSI              | GPIO11           |
| SCK               | GPIO12           |
| MISO              | GPIO13           |
| BUSY              | GPIO15           |
| NRST              | GPIO17           |
| DIO1              | GPIO16           |

### Sơ đồ kết nối

```text
ESP32-S3 Dev Kit          MKE-M24 (Ra-01SH)
─────────────────         ─────────────────
GPIO10  ───────────────── NSS
GPIO11  ───────────────── MOSI
GPIO12  ───────────────── SCK
GPIO13  ───────────────── MISO
GPIO15  ───────────────── BUSY
GPIO17  ───────────────── NRST
GPIO16  ───────────────── DIO1
GND     ───────────────── GND
3.3V    ───────────────── VCC
```

---

## 📚 Thư viện

Repo sử dụng thư viện **RadioLib** để điều khiển module LoRa.

RadioLib hỗ trợ nhiều dòng chip LoRa khác nhau, trong đó có các dòng chip được sử dụng trên MKE-M23 và MKE-M24.

---

## 🚀 Mục đích Repo

Repo cung cấp các code mẫu để:

* Kết nối ESP32-S3 với module LoRa MKE-M23.
* Kết nối ESP32-S3 với module LoRa MKE-M24.
* Gửi dữ liệu qua LoRa.
* Nhận dữ liệu qua LoRa.
* Kiểm tra kết nối và cấu hình module LoRa.
* Làm nền tảng cho các dự án giao tiếp LoRa sử dụng ESP32-S3.

---

## 📁 Cấu trúc Repo

```text
.
├── MKE-M23/
│   ├── LoRa_Transmit/
│   └── LoRa_Receive/
│
├── MKE-M24/
│   ├── LoRa_Transmit/
│   └── LoRa_Receive/
│
└── README.md
```

---

## ⚠️ Lưu ý

* ESP32-S3 và các module LoRa sử dụng mức logic **3.3V**.
* Kiểm tra đúng nguồn cấp cho module trước khi sử dụng.
* MKE-M23 và MKE-M24 sử dụng các chân điều khiển khác nhau, vì vậy cần sử dụng đúng wiring tương ứng với từng module.
* Khi sử dụng RadioLib, cần cấu hình đúng loại module và đúng GPIO theo phần kết nối ở trên.

---

## 🛠️ Hardware

**MCU:** ESP32-S3 Dev Kit
**LoRa Module 1:** Hshop MKE-M23 – Ai-Thinker Ra-02 Breakout Board
**LoRa Module 2:** Hshop MKE-M24 – Ai-Thinker Ra-01SH Breakout Board
**LoRa Library:** RadioLib
