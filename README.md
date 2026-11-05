# Personal Portfolio & Web Developer Showcase (PHP & MySQL)

A modern, responsive, and database-driven web application built for web developers and informatics students. This project dynamically retrieves personal details, academic history, technical skills, portfolio projects, and contact channels from a MySQL database.

---

## 🚀 Key Features & Architectural Overview
- **Dynamic Database Rendering:** All content rendered in `index.php`, `portfolio.php`, and `contact.php` is queried directly from MySQL via `mysqli`.
- **Modern & Balanced Aesthetics:** Crafted with a refined slate & indigo theme (`#0b0f19` and `#6366f1`), subtle glassmorphism navigation, soft cards, and zero color clashing.
- **Web Developer Focused:** Showcases web projects, UI/UX wireframes, technical skill competencies with progress indicators, and an interactive message form.
- **100% English Content:** Professional English copywriting suitable for international standards, recruiter reviews, and academic submissions.
- **Message Ingestion:** Contact inquiries submitted via `contact.php` are recorded directly into the `tbl_pesan` table in MySQL.

---

## 🗄️ Database Architecture (`db_portofolio`)

The database script is located at [`database.sql`](database.sql) with the following structure:

| Table Name | Description | Key Attributes |
| :--- | :--- | :--- |
| `tbl_data_pribadi` | Core biographical information | `nama_lengkap`, `profesi`, `ringkasan_bio`, `email`, `telepon`, `lokasi`, `foto_profil` |
| `tbl_pendidikan` | Educational chronology & milestones | `jenjang`, `nama_sekolah`, `tahun`, `status`, `deskripsi` |
| `tbl_skill` | Technical skill proficiencies & categories | `nama_skill`, `kategori`, `tingkat` (%), `level_label` |
| `tbl_portofolio` | Showcase projects & case studies | `judul`, `kategori`, `deskripsi`, `gambar`, `teknologi`, `tautan_proyek`, `tautan_github` |
| `tbl_kontak` | Verified contact & social channels | `tipe`, `label`, `nilai`, `link_url`, `icon_svg` |
| `tbl_pesan` | Inbound messages submitted via contact form | `nama_pengirim`, `email_pengirim`, `metode_komunikasi`, `pesan`, `tanggal_masuk` |

---

## 🛠️ Step-by-Step Installation & Setup in XAMPP

### 1. Start XAMPP Services
1. Open **XAMPP Control Panel**.
2. Click **Start** for both **Apache** and **MySQL**.

### 2. Import Database in phpMyAdmin
1. Open your browser and navigate to: [http://localhost/phpmyadmin](http://localhost/phpmyadmin)
2. Click **New** on the left sidebar to create a database.
3. Enter database name: `db_portofolio` (Collation: `utf8mb4_unicode_ci`) and click **Create** (or simply use the Import tab directly).
4. Select the `db_portofolio` database, then click the **Import** tab at the top.
5. Choose the [`database.sql`](database.sql) file located in `C:\xampp\htdocs\ngoding\database.sql`.
6. Scroll down and click **Import** (or **Go**). All 6 tables with sample data will be created instantly.

### 3. Run the Web Application
Open your browser and navigate to:
- **Homepage:** [http://localhost/ngoding/index.php](http://localhost/ngoding/index.php)
- **Portfolio Showcase:** [http://localhost/ngoding/portfolio.php](http://localhost/ngoding/portfolio.php)
- **Contact & Inquiries:** [http://localhost/ngoding/contact.php](http://localhost/ngoding/contact.php)

---

## 📸 Checklist Lampiran Tugas Edlink

Untuk mengumpulkan tugas di Edlink, siapkan 4 tangkapan layar (screenshot) berikut:

1. **Screenshot Database di phpMyAdmin:**
   - Buka `http://localhost/phpmyadmin`
   - Pilih database `db_portofolio` di sidebar kiri hingga terlihat struktur tabel: `tbl_data_pribadi`, `tbl_pendidikan`, `tbl_portofolio`, `tbl_skill`, `tbl_kontak`, dan `tbl_pesan`.
2. **Screenshot `koneksi.php`:**
   - Buka file [`koneksi.php`](koneksi.php) di VS Code / Antigravity dan ambil screenshot kodenya.
3. **Screenshot Script PHP Penampil Data:**
   - Buka file [`index.php`](index.php) atau [`portfolio.php`](portfolio.php) yang menampilkan syntax query database (`mysqli_query`, `mysqli_fetch_assoc`) dan perulangan `foreach` untuk merender HTML.
4. **Screenshot Tampilan Web di Browser:**
   - Buka `http://localhost/ngoding/index.php` di browser Anda (Chrome / Edge / Firefox) dan screenshot halaman webnya yang elegan.

---

## 🐙 Push ke GitHub

Jalankan perintah berikut di terminal / PowerShell:

```bash
git add .
git commit -m "feat: migrate web developer portfolio to dynamic PHP and MySQL with modern UI"
git branch -M main
git remote add origin https://github.com/<username-anda>/<nama-repo-anda>.git
git push -u origin main
```

