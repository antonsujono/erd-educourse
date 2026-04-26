# ERD EduCourse

## 📌 Deskripsi

Project ini merupakan desain **Entity Relationship Diagram (ERD)** untuk aplikasi pembelajaran online **EduCourse** yang dibuat berdasarkan analisis kebutuhan dari desain Figma.

ERD ini digunakan sebagai dasar perancangan database pada pengembangan backend aplikasi.

---

## 🛠 Tools yang Digunakan

* draw.io (diagrams.net)
* GitHub

---

## 🧩 Daftar Entitas

Berikut adalah entitas utama yang terdapat dalam ERD:

* User
* Tutor
* Kelas (Produk)
* Kategori Kelas
* Modul Kelas
* Material
* Kelas_Saya (Enrollments)
* Order
* Pembayaran
* Review
* Pretest

---

## 🔗 Relasi Antar Entitas

Beberapa relasi utama dalam sistem:

* **User → Order** (1:N)
  Satu user dapat memiliki banyak order

* **Order → Pembayaran** (1:1)
  Satu order memiliki satu pembayaran

* **Tutor → Kelas** (1:N)
  Satu tutor dapat membuat banyak kelas

* **Kelas → Modul** (1:N)
  Satu kelas memiliki banyak modul

* **Modul → Material** (1:N)
  Satu modul memiliki banyak materi

* **User → Review** (1:N)
  Satu user dapat memberikan banyak review

* **Kelas → Review** (1:N)
  Satu kelas dapat memiliki banyak review

---

## 🔄 Relasi Many-to-Many

Relasi antara **User dan Kelas** merupakan **Many-to-Many (M:N)**, yang direpresentasikan melalui tabel penghubung:

### Kelas_Saya

Relasi:

* User (1) → (N) Kelas_Saya
* Kelas (1) → (N) Kelas_Saya

Tabel ini menyimpan data user yang mengikuti kelas beserta progress pembelajaran.

---

## 🗂 Struktur Folder

```
erd-educourse/
│
├── erd.pdf
└── README.md
```

---

## 📎 Catatan

Desain ERD ini disusun dengan mempertimbangkan:

* kebutuhan sistem berdasarkan Figma
* normalisasi database
* kemudahan implementasi backend di Node.js

---

## 🚀 Author

Dibuat untuk keperluan submission Mission Backend - Harisenin Bootcamp
