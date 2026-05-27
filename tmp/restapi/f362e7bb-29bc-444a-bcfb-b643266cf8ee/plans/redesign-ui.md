# Redesign & Modernisasi LxREST

## 🎯 Objective
Merombak desain UI/UX LxREST (`index.html`) agar lebih modern, responsif di berbagai perangkat, memiliki struktur kode yang bersih (clean code), dan mendukung Light/Dark mode, dengan tetap mempertahankan tata letak atas-bawah untuk Request dan Response.

## 🗂 Key Files & Context
- `index.html` (Satu-satunya file yang akan dimodifikasi, mempertahankan prinsip "single-file app").

## 🛠 Implementation Steps

### 1. Refactoring CSS & Dukungan Tema (Light/Dark Mode)
- **CSS Variables:** Mendefinisikan ulang variabel CSS untuk warna, bayangan, dan tipografi agar mendukung dua tema.
- **Theme Toggle:** Menambahkan tombol di UI untuk mengganti tema (Light/Dark) yang statusnya disimpan di `localStorage`.
- **Clean CSS:** Mengelompokkan CSS berdasarkan komponen (Layout, Sidebar, Main, Panels, Controls, Utilities) agar lebih mudah dibaca dan dipelihara.

### 2. Modernisasi Tata Letak (Modern & Responsive)
- **App Layout:** Menggunakan CSS Grid yang lebih tangguh untuk `app-container`.
- **Sidebar (Mobile Responsive):** Membuat sidebar dapat disembunyikan/dimunculkan dengan mulus di perangkat mobile (menggunakan hamburger menu atau tombol toggle).
- **Header & Request Bar:** Merombak bilah alamat URL dan pemilih metode HTTP agar terlihat seperti satu kesatuan (pill/input group) yang lebih bersih.
- **Sistem Tab:** Memperbarui desain tab dengan indikator aktif yang lebih modern dan animasi transisi yang halus.
- **Response Panel:** Merapikan informasi meta respons (Status, Waktu, Ukuran) dengan desain badge yang lebih elegan.

### 3. Refactoring JavaScript
- Menambahkan logika untuk mengelola *Theme Toggle*.
- Menambahkan logika untuk membuka/menutup Sidebar di layar kecil.
- Mengoptimalkan interaksi UI agar terasa lebih responsif.

## ✅ Verification & Testing
- Membuka `index.html` di browser desktop dan memastikan tampilan baru berfungsi dengan baik.
- Menguji fungsi perpindahan tema (Light ke Dark dan sebaliknya).
- Mensimulasikan tampilan mobile/tablet di browser untuk memastikan sidebar dan elemen lainnya beradaptasi dengan benar (responsif).
- Mengirimkan *request* uji coba untuk memastikan semua fungsi inti (Params, Headers, Body, Auth, Response) tetap berjalan normal setelah perubahan UI.
