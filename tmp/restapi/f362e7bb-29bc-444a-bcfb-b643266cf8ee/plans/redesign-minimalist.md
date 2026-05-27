# Redesign Minimalis LxREST

## 🎯 Objective
Mendesain ulang `index.html` dengan pendekatan **Minimalis Ekstrem, Konsisten, dan Semantik**. Fokus pada pengurangan elemen visual yang tidak perlu, penggunaan *whitespace* yang optimal, tipografi yang jelas, serta penerapan palet warna yang **semantik** (merah untuk error, hijau untuk sukses, dll) dan konsisten di seluruh aplikasi (mendukung Light/Dark mode). Tata letak mempertahankan struktur Atas (Request) - Bawah (Response).

## 🗂 Key Files & Context
- `index.html` (Satu-satunya file yang akan dimodifikasi).

## 🛠 Implementation Steps

### 1. Palet Semantik & Tipografi Minimalis (CSS)
- **Tema Warna (Light & Dark) & Semantic Colors:** 
  - Menggunakan warna monokrom bersih sebagai dasar.
  - Menerapkan **semantic colors** secara konsisten: `Success` (Hijau/22C55E), `Error` (Merah/EF4444), `Warning` (Kuning/FACC15), dan `Info/Primary` (Biru-Ungu/6C63FF). Warna ini akan digunakan untuk HTTP methods (GET=hijau, POST=biru, DELETE=merah) dan status HTTP (200=hijau, 400/500=merah).
- **Tipografi & Konsistensi:** Menggunakan font sistem (Inter/System-UI). Menekankan hierarki melalui `font-weight` dan warna teks (primary, secondary, muted), bukan elemen kotak/border.
- **Penghapusan Ornamen:** Menghilangkan `box-shadow` tebal dan *border* yang tidak esensial. Desain UI akan sepenuhnya konsisten di seluruh panel (padding sama, border-radius seragam tapi halus).

### 2. Restrukturisasi Tata Letak & Elemen UI
- **Sidebar Tersembunyi (Drawer):** Sidebar (History, Collections, Env) disembunyikan secara *default* dan muncul sebagai *drawer* dari samping.
- **Request Bar Terpadu:** Menggabungkan pemilih Metode, input URL, dan tombol Send menjadi satu baris mulus tanpa *border* pemisah yang mencolok.
- **Tabs Halus:** Tampilan tab minimalis, hanya teks yang berubah ketebalan/warna saat aktif.

### 3. Pembersihan Kode & Interaksi
- **Clean Code CSS & JS:** Mengelompokkan variabel CSS dan logika JS agar lebih mudah dikelola.
- Mengurangi penggunaan *border* pada input, menggunakan *background* halus yang merespon *hover* atau *focus*.
- Menambahkan logika untuk *drawer* Sidebar dan *Theme Toggle* (Light/Dark).

## ✅ Verification & Testing
- Memeriksa konsistensi palet semantik pada status code, HTTP methods, dan notifikasi.
- Memeriksa tampilan di mode Light dan Dark untuk memastikan rasio kontras.
- Menguji kelancaran UI (drawer Sidebar, Tabs, Theme Toggle).
- Memastikan fungsionalitas inti (mengirim request, melihat respons) berjalan normal.
