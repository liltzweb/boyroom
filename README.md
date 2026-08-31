# 𓏲 phonist ‧ order form & website ♡

> **PHONIST** adalah katalog website interaktif bertema *"i stole your phone & exposed you"* karya [@liltz](https://t.me/mirssy) / **catamourie**. Repositori ini memuat source code website utama serta halaman **Order Form** resmi yang siap dideploy ke GitHub Pages / Netlify.

---

## 📌 Demo & Live Links

- **Form Pemesanan**: `https://<username>.github.io/phonist/form.html` (atau rename ke `index.html` jika repo khusus form)
- **Website Utama**: `https://<username>.github.io/phonist/`
- **Official Telegram**: [@mirssy](https://t.me/mirssy)

---

## 💸 Struktur Harga (Pricing)

- **Harga Dasar (Base Website)**: `Rp24.000`
- **Recolor Custom Color Palette**: `+Rp2.000`
- **Rush Fee (Deadline <24 Jam)**: `+Rp4.000`
- **Metode Pembayaran**: QRIS (No Rate Fee)

---

## 🎨 Color Palette Default (Electric Blue)

| Warna | Hex Code | Deskripsi |
| :--- | :--- | :--- |
| **Off White** | `#F5F5F2` | Background utama |
| **Black** | `#111214` | Teks dan elemen kontras |
| **Electric Blue** | `#356BFF` | Warna aksen utama / thread |
| **Muted Blue** | `#7895D8` | Border dan fokus outline |
| **Ice Blue** | `#DCE6FF` | Background badge / pill aktif |
| **Gray** | `#C9CACD` | Garis pembatas & teks sekunder |

---

## ✨ Fitur Order Form (`form.html`)

1. **Ticket Stub Header**:
   - Tampilan tiket estetik dengan perforasi garis putus-putus.
   - Total harga terkalkulasi secara otomatis dan real-time.

2. **Validasi & Color Picker Dinamis**:
   - Pilihan recolor interaktif dengan 6 color picker terhubung ke input kode HEX.
   - Validasi format HEX regex otomatis (`#RRGGBB`).

3. **17 Bagian Form Terstruktur**:
   - `00` ୵ **Customer Identity** (Nama, Username, QRIS, Tanggal Deadline, Checkbox Rush Fee).
   - `01` ୵ **Custom Color Palette** (Pilihan no/yes + color picker).
   - `02` ୵ **Core Identity** (Nama Penerima, Nama Pengirim, Umur, Tanggal Ulang Tahun, Kode Perangkat, Tahun Pertemanan, Inisial Avatar Chat).
   - `03` ୵ **Step 0 — Opening** (Hero greeting, subtitle, pesan status terminal, tombol pembuka).
   - `04` ୵ **Step 1 — Intro** (Badge label, judul headline, body prose, tombol lanjut).
   - `05` ୵ **Step 2 — Home Bento Hub** (Judul section, notifikasi bento, subteks card).
   - `06` ୵ **Step 3 — Messages & Memo** (5 pesan chat, judul memo rahasia, whisper & isi paragraf tulus).
   - `07` ୵ **Step 4 — Camera Roll** (Judul locked archive folder & 6 caption foto publik).
   - `08` ୵ **Step 5 — Notes App** (4 catatan unik: perkataan khas, hal yang dihutang, pengingat, rasa syukur).
   - `09` ୵ **Step 6 — Music Player** (4 judul lagu, nama musisi & vibe tags).
   - `10` ୵ **Step 7 — Memories Lore** (6 timeline tonggak pertemanan, tanggal, quote & cerita).
   - `11` ୵ **Step 8 — Memory Quiz** (4 soal kuis tebak-tebakan, 3 opsi jawaban, kunci, feedback benar/salah).
   - `12` ୵ **Step 9 — Secret Tribute Screen** (Heading & surat rahasia tulus).
   - `13` ୵ **Step 10 — Birthday Mode Profile** (Nama profil, umur, 3 pill status badge, survival rate meter).
   - `14` ୵ **Step 11 — Final Letter & Response** (Surat penutup, tanda tangan, opsi balasan penerima, username telegram pembeli).
   - `15` ୵ **Lampiran Foto** (Catatan instruksi kirim foto via Telegram).
   - `16` ୵ **Lampiran Lagu MP3** (Catatan instruksi kirim 4 lagu via Telegram).
   - `17` ୵ **Link Website** (Judul tab, 2 pilihan custom subdomain `.netlify.app`).

4. **Satu Klik Salin & Buka Telegram**:
   - Validasi input wajib.
   - Merangkum form ke dalam teks rapi dengan simbol unicode (`𓏲 phonist form ♡`).
   - Teks otomatis tersalin ke clipboard pengguna.
   - Membuka link `https://t.me/mirssy?text=...` dengan teks pesanan terisi otomatis.

---

## 📁 Struktur File

```text
PHONIST/
├── index.html          # Website interaktif utama PHONIST (14 Screen)
├── form.html           # Halaman Form Pemesanan PHONIST (Harga 24k)
├── order.html          # Salinan form.html (opsi routing alternatif)
├── style.css           # Styling CSS lengkap & responsif mobile/desktop
├── script.js           # Konfigurasi data konten, audio player 4 lagu, animasi
├── README.md           # Dokumentasi repositori
└── assets/             # Direktori aset
    ├── audio/          # File lagu format .mp3
    └── images/         # Foto memori, kuis, secret, dan galeri
```

---

## 🚀 Cara Upload & Hosting ke GitHub Pages

### Opsi A: Menggabungkan Website & Form dalam Satu Repositori
1. Push semua file repositori ini ke GitHub (`main` branch).
2. Buka repository di GitHub -> Masuk ke tab **Settings** -> **Pages**.
3. Pada bagian **Build and deployment**, pilih:
   - **Source**: `Deploy from a branch`
   - **Branch**: `main` / `/ (root)`
4. Klik **Save**.
5. Website kamu akan aktif di:
   - Website Utama: `https://<username>.github.io/<repo-name>/`
   - Form Pemesanan: `https://<username>.github.io/<repo-name>/form.html`

### Opsi B: Khusus Halaman Form Saja (seperti `liltzweb.github.io/phonist/`)
1. Jika repositori ini ditujukan **khusus** untuk form pemesanan:
   - Rename `form.html` menjadi `index.html`.
2. Push ke GitHub dan aktifkan GitHub Pages.
3. Form akan langsung terbuka di `https://<username>.github.io/<repo-name>/`.

---

## 📜 Terms & Conditions

1. Seluruh desain, kode, dan konten adalah hak cipta **catamourie** / [@liltz](https://t.me/mirssy).
2. Dilarang mendistribusikan ulang, menjual ulang kode mentah, atau mengklaim kepemilikan desain tanpa izin.
3. Pemesanan resmi hanya melalui Telegram: [@mirssy](https://t.me/mirssy).

---

<div align="center">
  <sub>crafted with care by @liltz ‧ thank you for trusting phonist ♡</sub>
</div>
