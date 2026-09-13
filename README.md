# 🎥 Interactive Camera Filter with Hand Gesture

Aplikasi filter kamera interaktif menggunakan **Hand Tracking** dengan **MediaPipe** dan **OpenCV**.

Aplikasi ini memungkinkan pengguna membuat sebuah **"Portal" menggunakan gesture tangan** di depan webcam. Area di dalam portal akan menampilkan berbagai efek filter secara real-time.

## ✨ Fitur

Tersedia berbagai filter menarik yang dapat digunakan:

* ⚫ **Mono**
* 🎨 **Dual-Tone**
* 🟪 **Pixelate**
* 🔄 **Invert**
* 🟤 **Sepia**
* 🌫️ **Blur**
* 🌡️ **Thermal**
* ✏️ **Sketch**
* ⚡ **Glitch**
* 💡 **Neon**
* 🌌 **Galaxy**

## 🖥️ Persyaratan Sistem

Sebelum menjalankan aplikasi, pastikan komputer memenuhi persyaratan berikut:

* **Python 3.7 atau lebih baru**
* **Webcam / Kamera**
* Sistem operasi Windows, macOS, atau Linux
* Pencahayaan ruangan yang cukup

---

# 🚀 Cara Install dan Menjalankan

## 1. Clone Repository

Clone repository GitHub ke komputer Anda:

```bash
git clone <URL_GITHUB_ANDA>
```

Masuk ke folder repository:

```bash
cd <NAMA_FOLDER_REPO>
```

> Ganti `<URL_GITHUB_ANDA>` dengan URL repository GitHub Anda dan `<NAMA_FOLDER_REPO>` dengan nama folder project.

---

## 2. Buat Virtual Environment

Virtual environment **opsional tetapi sangat disarankan** agar library project tidak bentrok dengan project Python lainnya.

### Windows

```bash
python -m venv venv
```

Aktifkan virtual environment:

```bash
venv\Scripts\activate
```

Jika berhasil, biasanya akan muncul tulisan `(venv)` di awal terminal.

### macOS / Linux

```bash
python3 -m venv venv
```

Aktifkan:

```bash
source venv/bin/activate
```

---

## 3. Install Dependencies

Jika repository sudah memiliki file `requirements.txt`, jalankan:

```bash
pip install -r requirements.txt
```

### Install Manual

Jika belum tersedia `requirements.txt`, install library berikut:

```bash
pip install opencv-python mediapipe numpy
```

Library yang digunakan:

| Library         | Fungsi                                |
| --------------- | ------------------------------------- |
| `opencv-python` | Mengakses webcam dan memproses gambar |
| `mediapipe`     | Hand Tracking / deteksi tangan        |
| `numpy`         | Pengolahan data dan gambar            |

---

## 4. Pastikan Model MediaPipe Tersedia

Aplikasi membutuhkan beberapa file model MediaPipe.

Pastikan file berikut tersedia di dalam project:

```text
hand_landmarker.task
selfie_segmenter.tflite
```

Struktur folder yang disarankan:

```text
project/
│
├── main.py
├── requirements.txt
├── hand_landmarker.task
├── selfie_segmenter.tflite
└── venv/
```

### Fungsi Model

**`hand_landmarker.task`**

Digunakan untuk mendeteksi titik-titik atau **landmark pada tangan**.

**`selfie_segmenter.tflite`**

Digunakan untuk proses **segmentasi background**, terutama pada filter **Galaxy**.

> Pastikan kedua file model berada pada lokasi yang sesuai dengan path yang digunakan di dalam kode `main.py`.

---

# ▶️ 5. Menjalankan Aplikasi

Setelah semua dependency dan model tersedia, jalankan:

```bash
python main.py
```

Untuk macOS/Linux:

```bash
python3 main.py
```

Jika berhasil, webcam akan terbuka dan aplikasi mulai mendeteksi gesture tangan secara real-time.

---

# 🖐️ Cara Menggunakan

## Membuka Portal

Gunakan **dua tangan** di depan kamera.

Gunakan:

* 👍 Jempol tangan kiri
* ☝️ Telunjuk tangan kiri
* 👍 Jempol tangan kanan
* ☝️ Telunjuk tangan kanan

Aplikasi akan mendeteksi keempat titik tersebut dan membentuk sebuah **portal berbentuk persegi empat**.

Filter akan diterapkan pada area **di dalam portal**.

---

## 🔄 Mengganti Filter

Filter dapat diganti menggunakan gesture tangan.

### Cara 1 — Jempol dan Kelingking

Dekatkan atau sentuhkan:

**ujung jempol → ujung jari kelingking**

Ketika gesture terdeteksi, filter akan berpindah ke filter berikutnya.

### Cara 2 — Dua Telunjuk

Dekatkan:

**ujung telunjuk tangan kiri → ujung telunjuk tangan kanan**

Gesture tersebut juga dapat digunakan untuk mengganti filter.

---

# 🎨 Daftar Filter

Aplikasi menyediakan beberapa efek visual:

| Filter        | Deskripsi                           |
| ------------- | ----------------------------------- |
| **Mono**      | Efek hitam putih                    |
| **Dual-Tone** | Efek dua warna                      |
| **Pixelate**  | Membuat gambar menjadi piksel       |
| **Invert**    | Membalik warna gambar               |
| **Sepia**     | Efek foto klasik kecokelatan        |
| **Blur**      | Memberikan efek blur                |
| **Thermal**   | Efek seperti kamera thermal         |
| **Sketch**    | Mengubah gambar menjadi efek sketsa |
| **Glitch**    | Efek digital glitch                 |
| **Neon**      | Efek garis bercahaya                |
| **Galaxy**    | Efek luar angkasa / galaksi         |

---

# ❌ Menutup Aplikasi

Untuk keluar dari aplikasi:

1. Pastikan jendela kamera **aktif/diklik**.
2. Tekan tombol:

```text
Q
```

Aplikasi kemudian akan berhenti dan jendela kamera ditutup.

---

# 💡 Tips Penggunaan

Agar Hand Tracking dapat bekerja dengan optimal:

* Gunakan ruangan dengan **pencahayaan yang cukup**.
* Pastikan tangan terlihat jelas oleh webcam.
* Hindari background yang terlalu ramai.
* Jangan terlalu dekat atau terlalu jauh dari kamera.
* Pastikan jari tidak tertutup benda lain.
* Gunakan webcam dengan posisi yang stabil.

---

# 📁 Struktur Project

Contoh struktur project:

```text
hand-gesture-filter/
│
├── main.py
├── requirements.txt
├── hand_landmarker.task
├── selfie_segmenter.tflite
├── README.md
└── venv/
```

---

# 🛠️ Teknologi yang Digunakan

Project ini dibuat menggunakan:

* **Python**
* **OpenCV**
* **MediaPipe**
* **NumPy**
* **Webcam**

---

# 📜 Lisensi

Project ini dibuat untuk **pembelajaran, eksperimen, dan pengembangan aplikasi computer vision berbasis gesture tangan**.

Silakan dikembangkan dan dimodifikasi sesuai kebutuhan.
