# Product Management System

Aplikasi ini adalah sistem manajemen produk yang dibangun dengan menggunakan **Spring Boot** dan **Java**. Sistem ini menyediakan API untuk mengelola data produk dengan operasi dasar seperti menambahkan, memperbarui, dan menghapus produk.

## Struktur Proyek

- **DemoApplication.java**: File utama untuk menjalankan aplikasi Spring Boot.
- **Product.java**: Entitas untuk mendefinisikan objek produk.
- **ProductController.java**: Kontroller untuk menangani permintaan HTTP terkait produk (menambah, memperbarui, menghapus, dan menampilkan produk).
- **ProductService.java**: Kelas yang berisi logika bisnis untuk mengelola produk.
- **ProductRepository.java**: Repositori untuk mengakses dan menyimpan data produk ke dalam database.

## Prerequisites

Pastikan untuk menginstal dan mengonfigurasi perangkat lunak berikut sebelum menjalankan aplikasi ini:
- **Java 11** atau lebih baru
- **Maven** untuk build proyek
- **Spring Boot** (Secara otomatis dikelola melalui Maven)
- **Database** (MySQL atau database lain yang kompatibel)

### Instalasi Dependensi

Jika kamu menggunakan **Maven**, pastikan untuk menginstal dependensi yang diperlukan menggunakan perintah berikut:
```bash
mvn clean install
Cara Menjalankan Aplikasi
Klon repositori ini ke mesin lokal kamu:

bash
git clone https://github.com/username/repository.git
Konfigurasi database:
Pastikan untuk mengonfigurasi koneksi database di application.properties (atau application.yml jika menggunakan YAML). Sesuaikan pengaturan dengan kredensial database yang kamu gunakan.

Jalankan Aplikasi:
Setelah semua dependensi diinstal dan database dikonfigurasi, jalankan aplikasi dengan perintah:

bash
mvn spring-boot:run
Aplikasi akan berjalan di localhost:8080 dan siap menerima permintaan API untuk mengelola produk.

API Endpoints
1. Menambahkan Produk
URL: /api/products

Metode: POST

Body Request:

json
{
  "name": "Product Name",
  "description": "Product Description",
  "price": 100
}
2. Mendapatkan Semua Produk
URL: /api/products

Metode: GET

Response:

json
[
  {
    "id": 1,
    "name": "Product Name",
    "description": "Product Description",
    "price": 100
  }
]
3. Mendapatkan Produk Berdasarkan ID
URL: /api/products/{id}

Metode: GET

Response:

json
{
  "id": 1,
  "name": "Product Name",
  "description": "Product Description",
  "price": 100
}
4. Memperbarui Produk
URL: /api/products/{id}

Metode: PUT

Body Request:

json
{
  "name": "Updated Product Name",
  "description": "Updated Product Description",
  "price": 150
}
5. Menghapus Produk
URL: /api/products/{id}

Metode: DELETE

Evaluasi dan Pengujian
Aplikasi ini dilengkapi dengan pengujian unit dan integrasi untuk memastikan fungsionalitas API. Kamu dapat menjalankan pengujian dengan perintah berikut:

bash
mvn test
Lisensi
Proyek ini dilisensikan di bawah MIT License.
