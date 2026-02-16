# xeenau - Website Portfolio IT

Website portfolio dan blog untuk konten pengetahuan IT, tips & trik, sejarah teknologi, implementasi, dan tutorial.

## 🚀 Cara Deploy ke GitHub Pages

### 1. Buat Repository Baru
1. Login ke GitHub: https://github.com
2. Klik tombol `+` di pojok kanan atas, pilih "New repository"
3. Nama repository: `xeenau.github.io` (atau nama lain, misal: `it-knowledge`)
4. Centang "Public"
5. Klik "Create repository"

### 2. Upload File
Ada 2 cara upload file:

#### Cara A: Lewat Web (Mudah)
1. Di repository yang baru dibuat, klik "uploading an existing file"
2. Drag & drop file `index.html` ke area upload
3. Scroll ke bawah, klik "Commit changes"

#### Cara B: Lewat Git (Untuk yang sudah familiar)
```bash
git clone https://github.com/USERNAME/xeenau.github.io.git
cd xeenau.github.io
# Copy file index.html ke folder ini
git add .
git commit -m "Initial commit - xeenau website"
git push origin main
```

### 3. Aktifkan GitHub Pages
1. Di repository Anda, klik tab "Settings"
2. Scroll ke bagian "Pages" (di sidebar kiri)
3. Di bagian "Source", pilih branch `main` dan folder `/ (root)`
4. Klik "Save"
5. Tunggu 1-2 menit, refresh halaman
6. Website Anda akan live di: `https://USERNAME.github.io/xeenau.github.io/`

### 4. (Opsional) Custom Domain
Jika punya domain sendiri:
1. Tambahkan CNAME record di DNS provider Anda:
   ```
   Type: CNAME
   Name: www
   Value: USERNAME.github.io
   ```
2. Di GitHub Settings > Pages, masukkan domain Anda di "Custom domain"
3. Centang "Enforce HTTPS"

## 📝 Cara Update Konten

### Update Manual
1. Edit file `index.html` dengan text editor (VS Code, Notepad++, dll)
2. Cari section yang ingin diubah (misalnya "Latest Posts")
3. Ubah teks, tambah card baru, dll
4. Upload file yang sudah diedit ke GitHub (replace yang lama)

### Menambah Post Baru
Cari section dengan class `latest-posts` dan tambahkan card baru:

```html
<div class="post-card">
    <div class="post-meta">
        <span class="post-tag">Tutorial</span>
        <span>5 min read</span>
    </div>
    <h4>Judul Post Anda</h4>
    <p>Deskripsi singkat post Anda di sini...</p>
</div>
```

### Mengubah Kategori
Cari section dengan class `categories` dan edit:
- Icon: ubah emoji di `<div class="category-icon">`
- Judul: ubah di `<h4>`
- Deskripsi: ubah di `<p>`
- Count: ubah teks di `<span class="count">`

## 🎨 Kustomisasi

### Mengubah Warna
Edit bagian `:root` di CSS (awal file):
```css
:root {
    --primary: #00ff88;      /* Warna utama (hijau terang) */
    --secondary: #0066ff;    /* Warna sekunder (biru) */
    --accent: #ff0066;       /* Warna aksen (pink) */
    /* ... dst */
}
```

### Mengubah Font
Font yang digunakan: Sora (body text) dan JetBrains Mono (code/logo)
Untuk mengganti, ubah link Google Fonts di `<head>` dan CSS

### Menambah Link Social Media
Di bagian footer, tambahkan link baru:
```html
<a href="URL_ANDA" target="_blank" title="Platform">Icon/Text</a>
```

## 🛠️ Fitur Website

- ✅ Desain modern dengan animasi halus
- ✅ Responsive (mobile-friendly)
- ✅ Grid background animasi
- ✅ Parallax effect pada cursor
- ✅ Glow effects dan gradients
- ✅ Category cards dengan hover effects
- ✅ Clean typography
- ✅ Fast loading (single HTML file)
- ✅ SEO-friendly

## 📱 Preview

Website ini sudah responsive dan akan terlihat bagus di:
- Desktop (1920px+)
- Laptop (1366px)
- Tablet (768px)
- Mobile (375px+)

## 🔄 Next Steps

Setelah website live, Anda bisa:
1. Mulai mengisi konten dengan artikel/tutorial pertama
2. Hapus badge "Coming Soon" dari post cards
3. Update jumlah post di category cards
4. Tambahkan Google Analytics untuk tracking pengunjung
5. Pertimbangkan menggunakan CMS seperti Jekyll atau Hugo untuk manajemen konten yang lebih mudah

## 📞 Support

Jika ada pertanyaan atau butuh bantuan:
- Twitter/X: @xeenau
- Buat issue di repository ini

---

**#keeplearning #xeenau** 🚀
Teknologi bukan hanya untuk yang "sudah ahli"
