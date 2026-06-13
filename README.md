# project-aol-machine-learning
# 🎓 PANDU — Prediksi Akademik & Navigasi Dini Universitas

![Python](https://img.shields.io/badge/Python-3.9%2B-blue?logo=python&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-1.x-FF4B4B?logo=streamlit&logoColor=white)
![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-ML-orange?logo=scikit-learn&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-Ready-2496ED?logo=docker&logoColor=white)
![License](https://img.shields.io/badge/License-MIT-green)

> Sistem prediksi berbasis Machine Learning untuk mendeteksi dini risiko *dropout* mahasiswa dan memprediksi kelulusan akademik.

---

## 📌 Tentang Proyek

**PANDU** adalah aplikasi web interaktif yang dibangun dengan **Streamlit** untuk memprediksi apakah seorang mahasiswa akan **Lulus (Graduate)** atau **Dropout** berdasarkan data akademik dan demografis. Proyek ini menggunakan tiga model Machine Learning yang telah dilatih pada dataset publik dari Kaggle.

Dataset yang digunakan: [Predict Students' Dropout and Academic Success](https://www.kaggle.com/datasets/thedevastator/higher-education-predictors-of-student-retention)

---

## ✨ Fitur Utama

- 🔮 **Prediksi Real-Time** — Input data mahasiswa dan dapatkan prediksi instan
- 📊 **Perbandingan Model** — Bandingkan performa tiga model ML secara langsung di dalam aplikasi
- 📋 **Riwayat Prediksi** — Simpan dan lihat kembali riwayat prediksi yang telah dilakukan
- 🧹 **Form yang Intuitif** — Input default kosong dengan validasi data

---

## 🤖 Model Machine Learning

| Model | Deskripsi |
|---|---|
| **Random Forest** | Ensemble method berbasis decision tree, performa tinggi |
| **Logistic Regression** | Model linear klasik, cepat dan interpretable |
| **Decision Tree** | Model berbasis pohon keputusan, mudah divisualisasikan |

---

## 🗂️ Struktur Repositori

```
project-ml/
│
├── code/                   # Notebook & script pelatihan model
│
├── web/                    # Aplikasi Streamlit (PANDU)
│   ├── app.py              # Entry point aplikasi
│   ├── requirements.txt    # Dependensi Python
│   ├── Dockerfile          # Konfigurasi Docker
│   ├── docker-compose.yml  # Docker Compose
│   └── models/             # Model ML yang sudah dilatih (.pkl)
│
├── Predict_Student_Dropout_and_Academic_Success[1].csv   # Dataset
└── Link_Kaggle_Predict_Students_Dropout_and_Academic_Success.txt
```

---

## 🚀 Cara Menjalankan

### ▶️ Opsi 1: Lokal (Streamlit)

1. **Clone repositori ini**
   ```bash
   git clone https://github.com/billiefernanda/project-ml.git
   cd project-ml/web
   ```

2. **Install dependensi**
   ```bash
   pip install -r requirements.txt
   ```

3. **Jalankan aplikasi**
   ```bash
   streamlit run app.py
   ```

4. Buka browser di `http://localhost:8501`

---

### 🐳 Opsi 2: Docker

1. **Build dan jalankan dengan Docker Compose**
   ```bash
   cd web
   docker-compose up --build
   ```

2. Buka browser di `http://localhost:8501`

---

### ☁️ Opsi 3: Streamlit Community Cloud

1. Fork repositori ini
2. Login ke [streamlit.io/cloud](https://streamlit.io/cloud)
3. Buat new app → pilih repositori ini
4. Set **Main file path**: `web/app.py`
5. Deploy!

---

## 📊 Dataset

Dataset bersumber dari Kaggle: **Predict Students' Dropout and Academic Success**

Dataset ini berisi informasi mahasiswa dari institusi pendidikan tinggi di Portugal, mencakup:
- Data demografis (usia, jenis kelamin, kebangsaan, dll.)
- Data akademik (nilai semester, jumlah mata kuliah, dll.)
- Data sosio-ekonomi (pekerjaan orang tua, beasiswa, dll.)
- **Target**: `Graduate`, `Dropout`, atau `Enrolled`

> Catatan: Pada aplikasi ini, target `Enrolled` tidak diikutsertakan — fokus prediksi adalah **Graduate vs Dropout**.

---

## 🛠️ Tech Stack

- **Frontend/UI**: [Streamlit](https://streamlit.io/)
- **Machine Learning**: [Scikit-Learn](https://scikit-learn.org/)
- **Data Processing**: Pandas, NumPy
- **Deployment**: Docker, Streamlit Community Cloud
- **Language**: Python 3.9+

---

## 👩‍💻 Author

**Billie Fernanda**
- GitHub: [@billiefernanda](https://github.com/billiefernanda)

---

## 📄 Lisensi

Proyek ini dibuat untuk keperluan akademis. Dataset diambil dari Kaggle dan tunduk pada lisensi masing-masing.
