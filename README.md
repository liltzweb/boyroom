# 🎟️ BOYROOM ✦ Order Form & 3D Website Documentation

Dokumentasi lengkap untuk formulir pemesanan web (**`form.html`**) dan website hadiah kamar 3D interaktif (**`index.html`**).

---

## 🏷️ Informasi Produk

* **Nama Produk**: BOYROOM
* **Desain & Kode**: `@liltz` / Catamourie
* **Harga Dasar**: **Rp 25.000**
* **Live Demo Website**: [https://boyroom.netlify.app](https://boyroom.netlify.app)
* **Formulir Pemesanan**: `form.html` (Dapat dibuka di browser lokal atau di-hosting di GitHub Pages / Netlify)

---

## 📂 Struktur File

```text
BOYROOM/
├── index.html           # Website utama kamar 3D interaktif (Three.js WebGL)
├── form.html            # Formulir pemesanan & kustomisasi bergaya tiket Liltzweb
├── styles.css           # Styling tampilan modern & responsif kamar 3D
├── app.js               # Mesin logika 3D, raycasting & kontrol sentuh mobile
├── audio.js             # Sound engine efek suara & pemutar musik MP3
├── config.js            # Pusat pengaturan data & teks cerita website
├── README.md            # Panduan & dokumentasi resmi
└── assets/
    ├── images/          # Tempat menyimpan 10 foto kenangan dari pembeli
    │   ├── photo1.jpg   # Foto kamera digicam 1
    │   ├── photo2.jpg   # Foto kamera digicam 2
    │   ├── photo3.jpg   # Foto kamera digicam 3
    │   ├── photo4.jpg   # Foto kamera digicam 4
    │   ├── polaroid1.jpg# Foto polaroid dinding 1
    │   ├── polaroid2.jpg# Foto polaroid dinding 2
    │   ├── timeline1.jpg# Foto milestone 1 (kelahiran/masa kecil)
    │   ├── timeline2.jpg# Foto milestone 2 (awal kenal)
    │   ├── timeline3.jpg# Foto milestone 3 (momen pacaran)
    │   └── timeline4.jpg# Foto milestone 4 (sweet 17 / ulang tahun)
    └── music/           # Tempat menyimpan 3 lagu MP3 dari pembeli
        ├── song1.mp3    # Lagu MP3 track 1
        ├── song2.mp3    # Lagu MP3 track 2
        └── song3.mp3    # Lagu MP3 track 3
```

---

## 📋 Rincian Formulir Pemesanan (`form.html`)

Formulir `form.html` mengadopsi estetika tiket (*ticket aesthetic*) khas Liltzweb dengan fitur lengkap:

### 1. Sistem Kalkulasi Harga Otomatis
* **Harga Dasar**: Rp 25.000
* **Custom Color Palette (Recolor)**: +Rp 2.000
* **Rush Processing (Selesai 24 Jam)**: +Rp 4.000

### 2. Exhibit Data yang Diisi Pembeli
1. **`00` Customer Identity**: Nama pembeli, username Telegram/IG, deadline, dan opsi *rush fee*.
2. **`01` Custom Color Palette**: Pilihan ganti palet warna (lengkap dengan *color picker* & input kode HEX).
3. **`02` Birthday & Identity Record**: Nama panggilan cowok, nama cewek, tanggal lahir, usia perayaan, tahun perayaan, tahun awal kenal.
4. **`03` Sticky Note Pintu Masuk 3D**: Pesan memo di daun pintu & tanda tangan pengirim.
5. **`04` Computer Workstation (OS Profile)**: Hal favorit tentang cowok, kekuatan rahasia, dan kebiasaan berdua.
6. **`05` Chat Simulasi iPhone 16 (iMessage)**: 4 baris balon obrolan teks.
7. **`06` Kamera Digicam (4 Foto)**: Caption & lokasi momen untuk 4 foto digicam.
8. **`07` Polaroid Dinding (2 Foto)**: Tulisan depan & pesan tulisan tangan di belakang polaroid.
9. **`08` Timeline Perjalanan (Road to 17 / 4 Foto)**: 4 cerita milestone perjalanan hidup & cinta.
10. **`09` Surat Cinta Kasur (Bed Letter)**: Judul surat, 4 paragraf surat cinta panjang, dan salam penutup.
11. **`10` Catatan Rahasia di Laci Meja**: 3 amplop catatan rahasia (penyemangat, kangen, dan kupon peluk).
12. **`11` Songs Needed (3 Lagu MP3)**: 3 judul lagu & artis (semua lagu wajib dari pembeli).
13. **`12` Link Netlify**: Judul halaman web & 2 opsi subdomain kustom `.netlify.app`.

### 3. Validasi & Pengiriman Otomatis
* Form memvalidasi seluruh kolom yang wajib diisi. Kolom kosong akan ditandai dengan warna *pink* (`.invalid`) dan layar akan otomatis bergeser (*smooth scroll*) ke kolom tersebut.
* Saat tombol **`submit`** ditekan:
  * Format teks pesanan **`𓏲 boyroom form ♡`** otomatis tersalin ke clipboard pembeli.
  * Chat Telegram (**`t.me/mirssy`**) langsung terbuka otomatis, pembeli tinggal *paste* dan melampirkan 10 foto serta 3 file lagu MP3.

---

## 🚀 Cara Menghosting Web Form (`form.html`)

### Pilihan A: GitHub Pages (Direkomendasikan)
1. Buat repositori baru di GitHub (misal: `boyroom` atau `order-form`).
2. Unggah file `form.html` (bisa di-rename menjadi `index.html` jika ingin URL langsung tanpa akhiran `/form.html`).
3. Masuk ke **Settings** → **Pages** → pilih branch **main** → simpan.
4. Web form Anda akan aktif di URL seperti: `https://username.github.io/boyroom/`.

### Pilihan B: Netlify
1. Buka [Netlify Drop](https://app.netlify.com/drop).
2. Seret (*drag and drop*) folder yang berisi file form Anda.
3. Ubah nama domain Netlify menjadi yang Anda inginkan (misal: `form-boyroom.netlify.app`).

---

## 🛠️ Cara Memproses Pesanan Masuk Menjadi Website Jadi

Setelah menerima teks pesanan dari pembeli via Telegram / WhatsApp:

1. **Buka file `config.js`**:
   * Salin data dari teks pesanan pembeli ke dalam variabel `window.ROOM_CONFIG` di file `config.js`.
2. **Simpan File Foto & Lagu**:
   * Simpan 10 foto dari pembeli ke folder `assets/images/` dengan penamaan:
     * `photo1.jpg` s/d `photo4.jpg` (kamera digicam)
     * `polaroid1.jpg` & `polaroid2.jpg` (polaroid dinding)
     * `timeline1.jpg` s/d `timeline4.jpg` (timeline perjalanan)
   * Simpan 3 file lagu dari pembeli ke folder `assets/music/` dengan penamaan:
     * `song1.mp3`, `song2.mp3`, `song3.mp3`
3. **Deploy Website Pembeli ke Netlify**:
   * Buka [Netlify Drop](https://app.netlify.com/drop).
   * Seret folder proyek `BOYROOM` yang sudah terisi data pembeli.
   * Masuk ke **Site configuration** → **Change site name** → ganti sesuai opsi link dari pembeli (misal: `jose17.netlify.app`).
   * Kirimkan link aktif website ke pembeli!

---

## ⚖️ Hak Cipta & Ketentuan
Semua desain, kode, dan aset merupakan karya cipta **`@liltz / Catamourie`**. Dilarang mendistribusikan ulang, menjual ulang kode mentah, atau mengklaim kepemilikan desain tanpa izin.
