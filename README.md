# Aplikasi Manajemen Data Mahasiswa

Aplikasi ini adalah sistem manajemen data mahasiswa berbasis Java Swing dengan koneksi ke database MySQL. Aplikasi ini memungkinkan pengguna untuk melakukan operasi CRUD (Create, Read, Update, Delete) pada data mahasiswa.

## Fitur Utama

- **Tambah Data Mahasiswa**: Menambahkan data mahasiswa baru ke sistem
- **Lihat Data Mahasiswa**: Menampilkan daftar mahasiswa dalam bentuk tabel
- **Update Data Mahasiswa**: Memperbarui data mahasiswa yang sudah ada
- **Hapus Data Mahasiswa**: Menghapus data mahasiswa dari sistem
- **Validasi Input**: Memastikan data yang dimasukkan valid dan lengkap

## Struktur Proyek

```
DataMahasiswa/
├── src/
│   ├── Database.java       # Kelas untuk koneksi database
│   ├── Mahasiswa.java      # Model data mahasiswa
│   └── Menu.java           # GUI dan logika aplikasi
└── lib/                    # Direktori untuk library tambahan
```

## Prasyarat

1. Java Development Kit (JDK) 8 atau lebih baru
2. MySQL Server
3. MySQL Connector/J (termasuk dalam proyek)
4. IDE Java (IntelliJ IDEA, Eclipse, dll)

## Instalasi dan Konfigurasi

1. **Setup Database**:
   - Buat database dengan nama `db_mahasiswa`
   - Jalankan query berikut untuk membuat tabel:

   ```sql
   CREATE TABLE mahasiswa (
       id INT AUTO_INCREMENT PRIMARY KEY,
       nim VARCHAR(20) NOT NULL UNIQUE,
       nama VARCHAR(100) NOT NULL,
       jenis_kelamin ENUM('Laki-laki', 'Perempuan') NOT NULL
   );
   ```

2. **Konfigurasi Koneksi Database**:
   - Buka file `Database.java`
   - Sesuaikan parameter koneksi jika diperlukan:
     ```java
     connection = DriverManager.getConnection(
         "jdbc:mysql://localhost:3306/db_mahasiswa", 
         "root", 
         "");
     ```

3. **Menjalankan Aplikasi**:
   - Compile dan run file `Menu.java`
   - Aplikasi akan muncul dengan antarmuka GUI

## Panduan Penggunaan

1. **Menambahkan Data Baru**:
   - Isi field NIM, Nama, dan pilih Jenis Kelamin
   - Klik tombol "Add"

2. **Mengupdate Data**:
   - Pilih baris yang ingin diupdate dari tabel
   - Ubah data di form
   - Klik tombol "Update"

3. **Menghapus Data**:
   - Pilih baris yang ingin dihapus dari tabel
   - Klik tombol "Delete"

4. **Membatalkan Operasi**:
   - Klik tombol "Cancel" untuk mengosongkan form

## Screenshot Aplikasi

![image](https://github.com/user-attachments/assets/b8eb6d03-6692-44dc-a363-eb0e82efe923)
![image](https://github.com/user-attachments/assets/3ebb69d9-8143-4fb4-becb-98305672f4b3)
![image](https://github.com/user-attachments/assets/0b9b3015-9225-4941-86d5-44d7405fc924)

## Troubleshooting

1. **Koneksi Database Gagal**:
   - Pastikan MySQL server berjalan
   - Periksa username dan password database
   - Pastikan MySQL Connector/J ada di classpath

2. **Error Input Data**:
   - Pastikan semua field terisi sebelum submit
   - NIM harus unik (tidak boleh duplikat)

3. **Error Tampilan GUI**:
   - Pastikan JDK versi kompatibel terinstall
   - Periksa dependensi library Swing

## Kontribusi

Kontribusi untuk proyek ini diterima. Silakan buka issue atau pull request untuk:
- Melaporkan bug
- Menambahkan fitur baru
- Meningkatkan dokumentasi

## Lisensi

Proyek ini dilisensikan di bawah [MIT License](LICENSE).

---

Dibuat dengan ❤️ oleh [Nama Anda] - 2023
