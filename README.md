Nama: Florencia sim
Kelas: 3A Pagi
Matkul: Machine Learning
Dosen Pengajar: Dr. DWI WAHYU PRABOWO, S.Si., M.Eng., Dody Erlangga, S.Kom

Klasifikasi Status Kelulusan Mahasiswa Menggunakan SVM
1. Deskripsi Dataset
Dataset berisi informasi akademik dan demografis mahasiswa sebanyak 379 data dengan 15 kolom, antara lain:
NAMA
JENIS KELAMIN
STATUS MAHASISWA
UMUR
STATUS NIKAH
IPS 1 – IPS 8
IPK
STATUS KELULUSAN (Label: Lulus / Tidak Lulus)
Beberapa kolom mengandung missing values (contoh IPK dan IPS 8), dan dilakukan proses pembersihan data serta encoding label.

2. Langkah Pengerjaan
Berikut tahapan yang dilakukan di dalam notebook:
a. Import library & load dataset
Notebook memuat dataset dari folder /data dan menampilkan:
5 data teratas
Info dataset
Jumlah missing value
Statistik deskriptif

b. Data Cleaning
Menghapus kolom yang tidak relevan (contoh: nama)
Mengisi missing value pada IPK dan IPS 8 menggunakan median
Melakukan encoding pada kolom kategorikal:
LabelEncoder pada STATUS KELULUSAN
One-hot encoding pada fitur kategorikal lain

c. Split Data
Data dibagi menjadi train dan test dengan rasio tertentu (dari notebook tampak menggunakan default sekitar 80:20).

d. Normalisasi / Standarisasi
StandardScaler digunakan untuk menormalkan fitur numerik sebelum masuk ke model SVM.

e. Training Model
Menggunakan:
SVM (Support Vector Machine) dengan kernel linear

f. Evaluasi Model
Notebook menampilkan:
Accuracy
Classification report
Confusion matrix

3. Hasil Evaluasi Model
Berdasarkan output notebook:
Akurasi model SVM ≈ 0.84 (84%)
Model cukup baik dalam membedakan mahasiswa Lulus dan Tidak Lulus.
Nilai precision, recall, dan f1-score per kelas ditampilkan di classification report.

4. Cara Menjalankan Notebook
Pastikan struktur folder:
/data
   └── dataset.csv  (nama sesuai file aslinya)
SVM_kelulusan.ipynb
README.md

Install dependencies:
pip install numpy pandas scikit-learn matplotlib
Jalankan notebook:
jupyter notebook SVM_kelulusan.ipynb
Eksekusi tiap cell secara berurutan.
