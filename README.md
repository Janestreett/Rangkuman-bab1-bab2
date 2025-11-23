RANGKUMAN MODUL PRAKTIKUM BASIS DATA - BAB 1 & 2

BAB 1: REVIEW KONVERSI ENTITY RELATIONSHIP (ER) DIAGRAM KE SKEMA RELASI

A. TUJUAN PEMBELAJARAN:

· Memahami cara mengubah diagram ER menjadi skema relasi dan tabel
· Memudahkan transformasi dari desain konseptual ke implementasi fisik database

B. MATERI POKOK:

1. Konversi ER Diagram ke Diagram Relationship
2. Studi kasus sistem pembayaran apotik

C. ATURAN KONVERSI PENTING:

1. ENTITAS KUAT → menjadi 1 tabel
   · Atribut simple menjadi kolom
   · Primary key tetap sebagai primary key
2. ATRIBUT KOMPOSIT → dipecah menjadi beberapa kolom
   · Contoh: alamat → jalan, kota, provinsi, kode_pos
3. ATRIBUT MULTINILAI → harus dibuat tabel terpisah
4. RELASI ONE-TO-MANY (1:N)
   · Tabel di sisi 'many' menambahkan foreign key
   · Foreign key merujuk ke primary key tabel di sisi 'one'
5. RELASI MANY-TO-MANY (N:N)
   · Harus dibuat tabel junction/penghubung
   · Tabel junction berisi foreign key dari kedua tabel
6. ENTITAS LEMAH → menjadi tabel + foreign key
   · Foreign key merujuk ke entitas kuat

D. EVALUASI:

· Test awal: identifikasi komponen ERD dan konversi sederhana
· Test akhir: konversi ERD kompleks menjadi kumpulan tabel

---

BAB 2: PENGANTAR BASIS DATA - DDL

A. TUJUAN PEMBELAJARAN:

· Mengenal MySQL dan aplikasi pendukungnya
· Dapat mengakses MySQL dan memahami tipe data
· Menguasai perintah DDL dasar

B. PENGENALAN MYSQL:

· MySQL adalah DBMS (Database Management System) open source
· Kelebihan: cepat, reliable, multiplatform, mendukung multitasking
· Direkomendasikan instalasi via XAMPP

C. AKSES MYSQL:

# Login ke MySQL
mysql -u root -p

# Lokasi database
Windows: C:\xampp\mysql\data
Linux: /opt/lampp/var/mysql/

D. TIPE DATA MYSQL:

· INT: angka bulat (-2 milyar sampai +2 milyar)
· FLOAT: angka desimal
· DATE: format YYYY-MM-DD
· DATETIME: format YYYY-MM-DD HH:MM:SS
· VARCHAR(n): string 1-255 karakter
· CHAR(n): string fixed length

E. PERINTAH DDL DASAR:

1. Membuat database:
   ```sql
   CREATE DATABASE praktikum;
   ```
2. Melihat database:
   ```sql
   SHOW DATABASES;
   ```
3. Menggunakan database:
   ```sql
   USE praktikum;
   ```
4. Menghapus database:
   ```sql
   DROP DATABASE praktikum;
   ```
