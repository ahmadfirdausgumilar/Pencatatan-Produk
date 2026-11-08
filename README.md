# Pencatatan Produk Toko (JavaFX)

Aplikasi desktop sederhana untuk mencatat produk toko, dibuat dengan **JavaFX + FXML (Scene Builder)** dan **Maven** di NetBeans. Proyek ini adalah hasil modifikasi dari aplikasi praktikum *TiketAppAdvanced* menjadi aplikasi daftar produk (Tugas Individu).

## Fitur

- **Tambah produk** lewat form (nama, kategori, harga). Kode produk dibuat otomatis (`PR001`, `PR002`, ...).
- **Tabel produk** yang menampilkan kode, nama, kategori, dan harga.
- **Pencarian berdasarkan nama produk** lewat tombol **Cari** (tidak membedakan huruf besar/kecil; kolom kosong menampilkan semua produk).
- **Lihat Detail** untuk membuka halaman detail produk yang dipilih di tabel.
- **Hapus produk** dengan dialog konfirmasi (fitur tambahan).

## Validasi

- Nama produk tidak boleh kosong.
- Harga harus berupa angka bulat dan lebih dari nol.
- Kategori hanya **Makanan** atau **Minuman**.

Data disimpan di memori selama aplikasi berjalan (tanpa database).

## Struktur proyek

```
src/main/java/kelas/
    MainApp.java            # titik masuk aplikasi
    Navigator.java          # berpindah halaman & mengirim objek ke controller
    model/Produk.java       # atribut private, constructor + validasi, getter
    data/DataProduk.java    # daftar produk sementara di memori
    controller/
        FormController.java     # halaman tambah produk
        DaftarController.java   # tabel, pencarian, detail, hapus
        DetailController.java   # halaman detail (menerima objek Produk)
src/main/resources/kelas/
    form.fxml, daftar.fxml, detail.fxml
    styles/app.css
```

## Cara menjalankan di NetBeans

### Kebutuhan

- **JDK 17 atau lebih baru** (NetBeans sudah membawa JDK sendiri).
- **Apache NetBeans** (dengan dukungan Maven, sudah termasuk secara bawaan).
- **Git** ([git-scm.com](https://git-scm.com/download/win)) untuk mengunduh repository.
- Koneksi internet saat pertama kali, supaya Maven mengunduh JavaFX.

### Langkah 1: Unduh (clone) repository

**Lewat NetBeans:**

1. Menu **Team > Git > Clone...**
   (Jika tidak ada menu *Team*, coba **Window > Team** atau gunakan cara Command Prompt di bawah.)
2. Isi **Repository URL**:
   ```
   https://github.com/ahmadfirdausgumilar/Pencatatan-Produk.git
   ```
3. Klik **Next**, pilih branch **main**, lalu **Next**.
4. Pada **Parent Directory**, pilih folder sederhana, misalnya `D:\java`, lalu klik **Finish**.
5. Saat muncul pertanyaan *"Open Project?"*, pilih **Open Project**.

**Atau lewat Command Prompt:**

```bat
cd /d D:\java
git clone https://github.com/ahmadfirdausgumilar/Pencatatan-Produk.git
```

Lalu di NetBeans: **File > Open Project**, pilih folder `Pencatatan-Produk`, dan klik **Open Project**.

> Tanpa Git: di halaman GitHub klik **Code > Download ZIP**, ekstrak ke folder sederhana, lalu buka dengan **File > Open Project**.

### Langkah 2: Jalankan

1. Tunggu NetBeans selesai memuat dependensi Maven (lihat indikator di pojok kanan bawah).
2. Klik kanan nama proyek > **Clean and Build**.
3. Klik kanan nama proyek > **Run** (atau tekan **F6**).

Jendela aplikasi akan terbuka di halaman form **Pencatatan Produk Toko**.

### Alternatif: lewat terminal

```bat
cd /d D:\java\Pencatatan-Produk
mvn clean javafx:run
```

## Cara memakai

1. Isi **Nama produk**, pilih **Kategori**, isi **Harga**, lalu klik **Simpan Produk**.
2. Ulangi untuk beberapa produk.
3. Klik **Lihat Daftar** untuk melihat tabel.
4. Ketik nama di kolom pencarian lalu klik **Cari** untuk memfilter.
5. Klik satu baris, lalu **Lihat Detail** untuk membuka halaman detail.
6. Pilih satu baris lalu **Hapus** untuk menghapus produk (ada konfirmasi).


Tampilan awal yang harus diisi
<img width="1366" height="768" alt="2026-11-08" src="https://github.com/user-attachments/assets/c9edc7b8-6346-4180-8117-6e9dcd536ee1" />

Tampilan Hasil Produk 
<img width="1366" height="768" alt="2026-11-08 (4)" src="https://github.com/user-attachments/assets/7a30de82-dbfb-4942-9181-0a3854b73bfd" />

Detail Produk
<img width="1366" height="768" alt="2026-11-08 (4)" src="https://github.com/user-attachments/assets/77abc42a-feff-4a98-8ed7-13f7913211c0" />

Hapus Produk
<img width="1366" height="768" alt="2026-11-08 (7)" src="https://github.com/user-attachments/assets/531af108-e5b5-468d-a3e3-fe7cc07c7dc9" />





## Teknologi

Java 17+, JavaFX 21, FXML & Scene Builder, Maven, CSS JavaFX.
