# 🔒 Basic Security

> infrastruktur security yang sudah mature bukan jaminan keamanan... tidak ada sistem yang benar-benar aman... selalu ada celah yang belum disadari.

---

## 🧱 CIA Triad

sebelum membahas tools, teknik, atau strategi pertahanan ada tiga prinsip dasar yang menjadi fondasi dari seluruh konsep security.

```
Confidentiality  # data hanya dapat diakses oleh pihak yang berwenang
Integrity        # data tidak boleh diubah tanpa otorisasi
Availability     # sistem harus dapat diakses kapanpun dibutuhkan
```

ketiga prinsip ini dikenal sebagai **CIA triad** dan seluruh framework security yang ada, mulai dari ISO 27001 hingga NIST, merujuk kembali ke sini.

CIA triad bukan sebuah checklist yang cukup dicentang satu kali. ini adalah **kerangka berpikir**  setiap keputusan teknis yang dibuat seharusnya selalu kembali ke tiga pertanyaan berikut:

```
# sebelum deploy sesuatu, pertanyakan:
C → siapa yang dapat mengakses data ini? apakah sudah dibatasi dengan benar?
I → jika ada yang mengubah data ini tanpa izin, apakah bisa terdeteksi?
A → jika sistem ini mengalami gangguan, apa dampaknya? apakah ada contingency plan?
```

---

## ⚠️ Threat Landscape

asumsi umum yang beredar adalah bahwa ancaman siber selalu datang dari luar, hacker canggih, exploit zero-day, atau malware sophisticated. kenyataannya, sebagian besar breach justru bermula dari hal-hal yang jauh lebih sederhana.

| Yang Sering Diasumsikan | Yang Sebenarnya Terjadi |
|---|---|
| hacker canggih dari luar | misconfiguration oleh tim internal |
| exploit zero-day | karyawan yang menjadi korban phishing |
| malware sophisticated | password lemah yang digunakan di semua akun |

> the biggest threat is closer than you think.

ketika sebuah ancaman berhasil menembus sistem selalu ada satu dari tiga prinsip CIA yang gagal dipertahankan. berikut adalah contoh nyata yang pernah terjadi:

```
# Confidentiality gagal
data pelanggan bocor karena S3 bucket misconfigured
tanpa enkripsi, tanpa access control yang memadai

# Integrity gagal
attacker berhasil memodifikasi transaction log
untuk menutupi transfer fraud yang dilakukan

# Availability gagal
serangan DDoS menyebabkan layanan down berjam-jam
operasional bisnis terhenti sepenuhnya
```

> CIA triad bukan sekadar teori — ini yang terjadi di dunia nyata.

---

## 🧠 Security Mindset

security bukan tentang seberapa canggih tools yang digunakan. tools dapat di-update, sistem dapat di-patch tetapi tanpa pemahaman yang mendasar, semua itu hanya akan menjadi lapisan permukaan.

yang perlu dipahami lebih dalam adalah:

```
what you're protecting  # aset apa yang perlu dijaga?
from who                # siapa yang berpotensi menjadi ancaman?
and why                 # mengapa aset tersebut penting untuk dilindungi?
```

dengan menjawab ketiga pertanyaan ini, prioritas pertahanan menjadi jauh lebih jelas dan celah yang selama ini luput dari perhatian akan lebih mudah ditemukan.

---

## 🚫 Zero Trust

zero trust adalah prinsip yang lahir dari satu kesadaran sederhana: ancaman dapat datang dari mana saja, termasuk dari dalam organisasi itu sendiri.

konsepnya:

> jangan otomatis mempercayai siapapun. verifikasi terlebih dahulu.

prinsip ini berlaku untuk semua entitas dalam sistem:

```
# semua harus diverifikasi:
user             # siapa mereka? apakah benar mereka yang mengklaim?
sistem           # dari mana request ini berasal?
traffic internal # apa tujuannya? apakah pola ini wajar?
```

zero trust bukan paranoia — ini adalah pendekatan yang realistis. di dunia digital, kepercayaan bukan sesuatu yang diberikan secara otomatis. harus dibuktikan, setiap saat, di setiap lapisan.

```
# zero trust diterapkan di semua layer:
network layer       # verifikasi setiap koneksi yang masuk
application layer   # verifikasi setiap request yang diterima
identity layer      # verifikasi setiap user dan device
```

---

## 📋 Recap

```
🧱 CIA Triad    — Confidentiality, Integrity, Availability — fondasi semua security
⚠️ Threat       — ancaman terbesar sering datang dari dalam, bukan dari luar
🧠 Mindset      — pahami apa yang diprotect, dari siapa, dan mengapa
🚫 Zero Trust   — never trust, always verify — diterapkan di semua layer
```

---

*x.com/xeenau · #keeplearning #security #infosec*
