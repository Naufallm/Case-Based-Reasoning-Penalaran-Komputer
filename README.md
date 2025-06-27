
# Klasifikasi Putusan Hakim Menggunakan Case-Based Reasoning

Repositori ini berisi kode dan data untuk penelitian yang bertujuan mengklasifikasikan putusan hakim terkait kasus pencurian menggunakan pendekatan *Case-Based Reasoning* (CBR). Penelitian ini secara spesifik membandingkan performa dua metode representasi teks—**TF-IDF** (statistik) dan **IndoBERT** (*deep learning*)—dalam mengkategorikan 100 putusan dari Pengadilan Negeri Medan ke dalam kelas "Berat," "Ringan," dan "Tidak Ditemukan."

## Deskripsi
Tantangan utama dalam analisis dokumen hukum adalah merepresentasikan teks yang padat akan terminologi spesifik ke dalam format yang dapat dipahami mesin. Penelitian ini mengimplementasikan sistem klasifikasi otomatis dengan membandingkan efektivitas metode klasik berbasis frekuensi kata (TF-IDF) dengan metode modern berbasis makna kontekstual (IndoBERT). Tujuannya adalah untuk menentukan pendekatan mana yang lebih andal dan akurat untuk domain hukum berbahasa Indonesia dengan volume data yang terbatas.

## Fitur Utama
- **Pra-pemrosesan Teks Hukum:** Membersihkan dan menstandarkan teks dari dokumen putusan.
- **Ekstraksi Fitur:** Mengimplementasikan dua pipeline paralel untuk representasi teks:
  1. Representasi vektor menggunakan **TF-IDF**.
  2. *Embeddings* kontekstual menggunakan **IndoBERT**.
- **Pelatihan Model:** Melatih klasifikator **Support Vector Machine (SVM)** untuk setiap jenis representasi teks.
- **Evaluasi Komparatif:** Menganalisis dan membandingkan kinerja kedua model menggunakan metrik akurasi, presisi, *recall*, dan F1-score.

Generated code
## Memulai

### 1. Prasyarat
- Python 3.8 atau versi lebih baru
- `pip` dan `virtualenv`

### 2. Instalasi
Untuk menyiapkan lingkungan dan menginstal semua dependensi yang diperlukan, ikuti langkah-langkah berikut:

1.  **Klon Repositori**
    ```bash
    git clone https://github.com/your-username/Case-Based-Reasoning-Penalaran-Komputer.git
    cd Case-Based-Reasoning-Penalaran-Komputer
    ```

2.  **Buat dan Aktifkan Lingkungan Virtual (Direkomendasikan)**
    ```bash
    # Untuk macOS/Linux
    python3 -m venv venv
    source venv/bin/activate

    # Untuk Windows
    python -m venv venv
    .\venv\Scripts\activate
    ```

3.  **Instal Dependensi**
    Instal semua pustaka Python yang dibutuhkan dari file `requirements.txt`.
    ```bash
    pip install -r requirements.txt
    ```

## ⚙Cara Menjalankan Pipeline End-to-End
Seluruh pipeline penelitian, mulai dari pemrosesan data hingga evaluasi model, dijalankan melalui notebook Jupyter.

### Menjalankan Notebook
Cara utama untuk menjalankan pipeline ini adalah dengan membuka dan menjalankan sel-sel kode di dalam notebook `case-based-reasoning.ipynb`.

1.  **Luncurkan Jupyter Notebook**
    Dari direktori utama proyek, jalankan perintah berikut di terminal Anda:
    ```bash
    jupyter notebook
    ```

2.  **Buka dan Jalankan Notebook**
    *   Di browser Anda, navigasikan ke direktori `notebooks/`.
    *   Buka file `case-based-reasoning.ipynb`.
    *   Jalankan setiap sel kode secara berurutan (dari atas ke bawah) untuk mereplikasi seluruh alur kerja

### Contoh Perintah
Untuk memulai, pastikan Anda berada di direktori utama repositori dan lingkungan virtual Anda aktif. Kemudian jalankan:
```bash
jupyter notebook notebooks/case-based-reasoning.ipynb

Selanjutnya, ikuti instruksi di dalam notebook untuk menjalankan pipeline.
