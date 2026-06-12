# Fitur Kamera - SahabatPetani AI

## 📸 Fitur Baru

### 1. Tombol "Buka Kamera"
- Tombol hijau dengan ikon kamera di upload card
- Tersedia selama belum ada gambar yang dipilih
- Akan bersembunyi saat ada gambar preview

### 2. Modal Kamera Real-time
- Akses kamera webcam langsung dari browser
- Preview live video stream
- Tombol "Ambil Foto" untuk capture gambar
- Tombol "Tutup Kamera" untuk menutup modal

### 3. Capture & Preview
- Foto yang diambil otomatis akan menampilkan preview
- File info (nama & ukuran) ditampilkan
- Tersedia tombol "Hapus" dan "Kirim ke AI"

## 🎨 Responsif Design

### Desktop (900px+)
- Layout 2 kolom (hero text + upload card)
- Feature cards 3 kolom
- Modal kamera dengan max-width 520px
- Tombol ukuran normal

### Tablet (640px - 900px)
- Layout single kolom
- Feature cards 2 kolom
- Modal sesuaikan ukuran layar
- Tombol lebih besar untuk touch-friendly

### Mobile (480px - 640px)
- Layout full-width responsive
- Feature cards single kolom
- Modal full screen dengan padding
- Tombol full-width untuk kemudahan tap
- Video stream max-height 300px

### Mobile Kecil (<480px)
- Padding minimal
- Font size lebih kecil
- Spacing optimal untuk layar kecil

## 🔧 Implementasi Teknis

### Camera API
- Menggunakan `navigator.mediaDevices.getUserMedia()`
- Constraint: `facingMode: 'environment'` (kamera belakang pada mobile)
- Support untuk audio: false

### Canvas Capture
- Menangkap frame video menggunakan `canvas.getContext('2d')`
- Konversi ke blob JPEG dengan kualitas 0.95
- Mengirim sebagai File object ke file input

### Modal Management
- Fixed positioning dengan semi-transparent overlay
- Flexbox untuk center alignment
- Z-index 1000 untuk layer di atas konten lain
- Close button dengan hover effect

## 🚀 Cara Menggunakan

### Desktop
1. Buka http://localhost:8000 di browser
2. Klik tombol hijau "Buka Kamera"
3. Izinkan akses kamera ketika diminta browser
4. Lihat preview video live
5. Klik "Ambil Foto" untuk capture
6. Foto akan menampilkan di preview
7. Klik "Kirim ke AI" untuk simulasi upload

### Mobile
1. Akses dari smartphone: http://[IP-ADDRESS]:8000
2. Klik "Buka Kamera" 
3. Izinkan akses kamera
4. Ambil foto dengan tap "Ambil Foto"
5. Lihat preview dan kirim

### Alternatif Input
- Klik "Unggah Foto" untuk pilih dari galeri
- Drag & drop gambar ke upload card
- Click drop zone untuk file picker

## 📱 Browser Support

✅ Chrome/Chromium  
✅ Firefox  
✅ Safari (iOS 14.5+)  
✅ Edge  

⚠️ Requires HTTPS untuk production (atau localhost)

## ⚙️ File yang Diubah

- `index.html` - Tombol kamera + modal HTML
- `css/styles.css` - Modal styling + responsive breakpoints
- `js/script.js` - Camera API + capture logic

## 🎯 Fitur Responsif

| Elemen | Desktop | Tablet | Mobile |
|--------|---------|--------|--------|
| Hero Layout | 2 kolom | 1 kolom | 1 kolom |
| Feature Cards | 3 kolom | 2 kolom | 1 kolom |
| Modal Width | 520px | 100% | 100% |
| Button Width | auto | 100% | 100% |
| Video Height | 400px | 350px | 300px |

## 🔐 Privacy & Security

- Semua processing dilakukan di browser (client-side)
- Tidak ada upload ke server (demo mode)
- Stream kamera dihentikan saat modal ditutup
- File dibuat secara lokal menggunakan Blob API

---
Versi: 1.0 | Update: Juni 2026
