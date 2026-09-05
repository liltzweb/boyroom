# 🎟️ BOYROOM ✦ 3D Room Gift Website & Order Form Documentation

Panduan resmi dan dokumentasi terlengkap untuk website hadiah kamar 3D interaktif (**`index.html`**), formulir pemesanan otomatis (**`form.html`**), dan konfigurasi data (**`config.js`**).

---

## 🏷️ Informasi Produk

* **Nama Produk**: BOYROOM
* **Kategori**: Interactive 3D WebGL Room Experience
* **Kreator & Desainer**: `@liltz` / Catamourie
* **Harga Dasar (Base Price)**: **Rp 25.000**
* **Opsi Tambahan (Add-ons)**:
  * **Custom Color Palette (Recolor)**: +Rp 2.000
  * **Rush Processing (Selesai Kilat dlm 24 Jam)**: +Rp 4.000
* **Demo Live Website**: [https://boyroom.netlify.app](https://boyroom.netlify.app)
* **Formulir Pemesanan**: `form.html` (Siap di-host di GitHub Pages / Netlify)
* **Tujuan Pengiriman Pesanan**: Telegram **[@mirssy](https://t.me/mirssy)**

---

## 📂 Struktur Folder & Berkas Proyek

```text
BOYROOM/
├── index.html           # Website utama kamar 3D interaktif (Three.js WebGL & OrbitControls)
├── form.html            # Formulir pemesanan interaktif bergaya tiket resmi Liltzweb
├── styles.css           # Styling tampilan modern, responsif mobile, modal pop-up & animasi
├── app.js               # Mesin logika 3D, raycaster klik objek, animasi tiup lilin & kontrol sentuh
├── audio.js             # Sound engine efek suara (klik, shutter, flip) & playlist musik MP3
├── config.js            # Pusat pengaturan seluruh teks, foto, lagu, tanggal & palet warna
├── README.md            # Dokumentasi lengkap panduan pembeli & penjual
└── assets/
    ├── images/          # Tempat menyimpan 8 foto kenangan dari pembeli
    │   ├── photo1.jpg   # Foto kamera digicam 1
    │   ├── photo2.jpg   # Foto kamera digicam 2
    │   ├── polaroid1.jpg# Foto polaroid gantung dinding 1
    │   ├── polaroid2.jpg# Foto polaroid gantung dinding 2
    │   ├── timeline1.jpg# Foto milestone 1 (kelahiran/masa kecil)
    │   ├── timeline2.jpg# Foto milestone 2 (awal kenal/terhubung)
    │   ├── timeline3.jpg# Foto milestone 3 (semakin dekat/jadian)
    │   └── timeline4.jpg# Foto milestone 4 (perayaan ulang tahun/hari ini)
    └── music/           # Tempat menyimpan 3 lagu MP3 dari pembeli
        ├── song1.mp3    # Lagu MP3 track 01
        ├── song2.mp3    # Lagu MP3 track 02
        └── song3.mp3    # Lagu MP3 track 03
```

---

## 🛋️ Rincian 14 Objek Interaktif di Kamar 3D

Website **BOYROOM** dirancang sebagai kamar cowok 3D interaktif yang penuh dengan kejutan dan kenangan manis. Seluruh teks dan konten dapat diganti secara menyeluruh (*100% replace-able*):

| No | Objek 3D di Kamar | Fitur & Respons Saat Diklik | Mapping di `config.js` |
|:---:|:---|:---|:---|
| **01** | **Pintu Kamar 3D** | Pintu terbuka dengan animasi 3D + menampilkan **Sticky Note Memo** pesan sambutan. | `doorMemo` / `index.html` |
| **02** | **Laptop Workstation** | Membuka OS komputer interaktif dengan **4 Folder**: *About Profile*, *Our Archive* (statistik & log), *Sweet 17 Pass* (kartu VIP pass), dan *Love Notes* (4 catatan romantis). | `computer` |
| **03** | **Kue Ulang Tahun** | Pop-up upacara tiup lilin interaktif, tag usia, pesan permohonan (*make a wish*), dan tombol *Wish Granted*. | `cake` |
| **04** | **iPhone 16 di Nakas** | Simulasi obrolan iMessage romantis dengan 4 balon chat bertanda waktu + 3 tombol *Quick Replies* interaktif. | `phone` |
| **05** | **Kamera Digicam** | Galeri 4 foto kamera vintage dengan efek suara *shutter*, caption foto, dan tag lokasi/tahun. | `camera` |
| **06** | **Polaroid Dinding** | 2 bingkai foto polaroid gantung yang bisa dibalik (**3D Flip**) untuk membaca pesan tulisan tangan di belakangnya. | `polaroids` |
| **07** | **Timeline Perjalanan** | Modal *"The Road to 17"* berisi 4 babak milestone perjalanan cinta lengkap dengan tanggal, tag, judul, preview, dan cerita penuh. | `timeline` |
| **08** | **Surat Kasur (Bed Letter)**| Surat cinta panjang di atas kasur dengan animasi buka amplop, eyebrow, 4 paragraf mendalam, dan tanda tangan pengirim. | `bed` |
| **09** | **Laci Meja Belajar** | 3 amplop catatan rahasia di laci meja: Surat Penyemangat, Surat Saat Kangen, dan Kupon Peluk Tanpa Batas. | `drawer` |
| **10** | **Jendela Skyline** | Pop-up pesan jendela pemandangan langit (pesan langit siang, pesan bintang malam, dan subteks cinta). | `window` |
| **11** | **Pemutar Musik Vinyl** | Widget pemutar musik 3 lagu MP3 dengan visualizer, tombol Play/Pause, Next/Prev Track, dan durasi. | `music` |
| **12** | **Saklar Lampu Kamar** | Tombol pengubah suasana lampu kamar dari mode Siang (hangat cerah) ke mode Malam (estetik ambient redup). | Diatur otomatis di `app.js` |
| **13** | **Dekorasi & Balon** | Balon ulang tahun 3D, banner nama pasangan, dan poster estetika. | Mengikuti nama di `config.js` |
| **14** | **Kontrol Kamera Orbit** | Navigasi putar 360°, geser (*pan*), perbesar/perkecil (*zoom*), dan tombol reset sudut pandang kamera. | Diatur otomatis di `app.js` |

---

## 📸 Panduan Media (Foto & Lagu)

### 1. Kebutuhan Foto (Total 10 Foto)
* `photo1.jpg`, `photo2.jpg`, `photo3.jpg`, `photo4.jpg` (Kamera Digicam — 4 Foto)
* `polaroid1.jpg`, `polaroid2.jpg` (Polaroid Dinding — 2 Foto)
* `timeline1.jpg`, `timeline2.jpg`, `timeline3.jpg`, `timeline4.jpg` (Timeline 4 Milestone — 4 Foto)

> **💡 Tips Format Foto**: Format JPG/PNG dengan orientasi vertikal (portrait 4:5) atau persegi (square 1:1). Resolusi yang disarankan 1080×1080px atau 1080×1350px agar tampilan tajam dan pas di layar handphone.

### 2. Kebutuhan Lagu (3 File MP3)
* `song1.mp3` (Track 01)
* `song2.mp3` (Track 02)
* `song3.mp3` (Track 03)

---

## 📝 Panduan Mengisi Formulir untuk Pembeli (`form.html`)

Formulir `form.html` mengadopsi format tiket elegan khas Liltzweb dengan validasi cerdas:

1. **Buka `form.html`** di browser (atau buka link form yang diberikan seller).
2. **Exhibit `00` - Identitas**: Masukkan nama, username Telegram/IG, tanggal deadline, dan centang *rush fee* jika butuh kilat 24 jam.
3. **Exhibit `01` - Palet Warna**: Pilih `no` untuk warna default keren (#2B52FF / biru, #C6FF3D / lime, dll), atau pilih `yes` (+Rp 2.000) untuk memilih palet warna sendiri.
4. **Exhibit `02` - Biodata & Tanggal**: Isi nama panggilan cowok, nama cewek, tanggal lahir, usia, tahun perayaan, dan tahun awal kenal.
5. **Exhibit `03` s/d `12` - Konten Cerita**: Isi teks kustom sesuai kisah kalian, atau biarkan menggunakan teks *default* yang sudah tertata puitis dan romantis.
6. **Exhibit `13` - Judul 3 Lagu**: Tuliskan judul lagu & nama artis yang akan dikirimkan file MP3-nya.
7. **Exhibit `14` - Pilihan Link**: Masukkan judul tab web dan siapkan 2 opsi nama subdomain `.netlify.app` (contoh: `jose17` dan `room17`).
8. **Tekan Tombol `Submit`**:
   * Teks pesanan berformat rapi **`𓏲 boyroom form ♡`** akan **otomatis tersalin ke clipboard**.
   * Chat Telegram **`t.me/mirssy`** akan langsung terbuka otomatis.
   * Pembeli tinggal **Paste / Tempel** teks tersebut, lalu mengirimkan 10 foto dan 3 file lagu MP3.

---

## ⚡ Panduan Penjual: Cara Memproses Pesanan & Deploy ke Netlify

Hanya butuh waktu **3 menit** untuk mengubah pesanan pembeli menjadi website 3D yang aktif:

### Langkah 1: Isi Data ke `config.js`
1. Buka file `config.js` di text editor (VS Code, Notepad, dll).
2. Sesuaikan data `window.ROOM_CONFIG` dengan teks format yang dikirim pembeli dari Telegram:
   * Nama cowok (`boyfriendName`), nama cewek (`girlfriendName`).
   * Tanggal lahir (`birthDate`), usia (`age`), tahun perayaan (`yearCelebration`), tahun hubungan (`relationshipStartDate`).
   * Isi sticky note pintu, teks 3 folder laptop (about, archive, notes), balon chat iPhone & quick replies, caption foto digicam, tulisan polaroid, 4 milestone timeline, surat cinta kasur, catatan laci, dan pesan jendela.
   * Judul 3 lagu di array `music.playlist`.

### Langkah 2: Masukkan Aset Foto & Lagu
1. Simpan foto-foto dari pembeli ke folder `assets/images/` dengan nama:
   * `photo1.jpg`, `photo2.jpg`, `photo3.jpg`, `photo4.jpg` (Digicam).
   * `polaroid1.jpg`, `polaroid2.jpg` (Polaroid).
   * `timeline1.jpg`, `timeline2.jpg`, `timeline3.jpg`, `timeline4.jpg` (Timeline).
2. Simpan 3 lagu dari pembeli ke folder `assets/music/` dengan nama:
   * `song1.mp3`, `song2.mp3`, `song3.mp3`.

### Langkah 3: Tes di Browser Lokal
Buka file `index.html` langsung di browser Chrome/Safari/Edge untuk memastikan semua foto tampil pas, audio berputar mulus, dan teks sudah sesuai dengan pesanan pembeli.

### Langkah 4: Deploy Gratis ke Netlify (Hanya 10 Detik!)
1. Buka [app.netlify.com/drop](https://app.netlify.com/drop) (login jika diminta).
2. Tarik (*drag and drop*) seluruh folder `BOYROOM` ke kotak upload Netlify.
3. Tunggu beberapa detik sampai status menjadi **Published**.
4. Klik **Site configuration** → **Change site name** → ganti nama link sesuai opsi dari pembeli (misal: `jose17.netlify.app`).
5. Selesai! Salin link tersebut dan kirimkan ke pembeli di Telegram.

---

## 🌐 Panduan Menghosting Formulir Pemesanan (`form.html`)

Agar pembeli bisa mengisi form secara online:

* **Cara 1: Netlify Drop**: Buat folder khusus berisi file `form.html` (rename jadi `index.html`), lalu drag & drop ke [app.netlify.com/drop](https://app.netlify.com/drop) dengan nama subdomain seperti `form-boyroom.netlify.app`.
* **Cara 2: GitHub Pages**: Masukkan `form.html` ke repositori GitHub Anda, buka **Settings** → **Pages** → aktifkan branch **main**. Form Anda akan langsung live di `https://username.github.io/repositori/form.html`.

---

## 🛡️ Hak Cipta & Ketentuan Layanan

Seluruh desain 3D, konsep tiket interaktif, arsitektur kode, dan aset grafis merupakan karya cipta intelektual **`@liltz / Catamourie`**.
* Dilarang keras membagikan, menjual ulang (*resell*), atau mendistribusikan kode sumber (*source code*) mentah.
* Pembeli lisensi template diperbolehkan menggunakan kode ini untuk melayani jasa pembuatan website klien akhir.
