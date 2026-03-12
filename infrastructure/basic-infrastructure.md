# 🏗️ Basic Infrastructure

> infrastructure itu bukan cuma urusan tim IT infra — developer juga wajib paham dasarnya sebelum bisa deploy app ke production.

---

## 🖥️ On-premise vs VPS vs Cloud

sebelum deploy, tentukan dulu tempat app lo jalan.

| | On-premise | VPS | Cloud |
|---|---|---|---|
| Server | fisik di datacenter sendiri | virtual, sewa sebagian | di-manage provider |
| Control | full | medium | tergantung provider |
| Biaya | mahal (infra sendiri) | terjangkau | pay-as-you-go |
| Cocok untuk | data sensitif, regulated | belajar, app kecil-medium | startup, scale cepat |

> **rule of thumb:**
> - data sensitif & compliance ketat → on-premise
> - belajar & app kecil → VPS
> - butuh scale cepat & fleksibel → cloud

---

## 🐧 Operating System (OS)

OS adalah lapisan pertama yang jalan di atas server — fondasi sebelum app lo bisa diinstall.

```
# pilihan utama
Linux    # paling umum di server — ringan, stable, gratis
Windows  # butuh lisensi — cocok untuk ekosistem .NET atau Active Directory
Unix     # enterprise level — AIX, Solaris
```

distro Linux yang paling sering dipakai di production:

```
Ubuntu      # paling populer, komunitas besar ← rekomendasi untuk pemula
AlmaLinux   # pengganti CentOS, gratis, enterprise-grade
Rocky Linux # pengganti CentOS, dibuat founder CentOS asli
RHEL        # Red Hat Enterprise Linux — berbayar, support resmi
Debian      # sangat stable, ringan
```

> **rekomendasi:** mulai dengan Ubuntu Server 22.04 LTS — dokumentasi paling lengkap.

---

## 📊 Spec Server

sebelum request server ke tim infra atau order di cloud — lo harus tau spesifikasi yang dibutuhkan app lo.

```
CPU     # jumlah core untuk proses — makin banyak makin cepat
RAM     # memori saat app berjalan — minimal 2GB untuk app sederhana
Storage # tempat nyimpan data & OS
        # SSD → lebih cepat, harga lebih mahal
        # HDD → lebih murah, lebih lambat
Network # kecepatan transfer data & jenis IP (public/private)
```

contoh request yang jelas dan benar:

```
2 vCPU | 4GB RAM | 100GB SSD
OS      : Ubuntu 22.04 LTS
Network : 100Mbps, public IP
```

> spec terlalu kecil = app lambat atau crash.
> spec terlalu besar = buang budget.
> sesuaikan dengan kebutuhan — bisa di-upgrade nanti.

---

## 🐳 Container (Docker)

masalah klasik yang sering terjadi:

> *"di laptop gue jalan, di server kok gak jalan?"*

penyebabnya — environment berbeda. solusinya: **Docker**.

```
Image      # blueprint aplikasi lo (berisi OS, dependency, config)
Container  # instance yang jalan dari sebuah image
Volume     # tempat nyimpan data yang persisten
Port       # jembatan antara container dan dunia luar
```

workflow dasar:

```bash
docker build -t myapp .     # build image dari Dockerfile
docker run -p 8080:80 myapp # jalankan container
```

> dengan Docker — environment di laptop, VPS, dan cloud akan selalu sama.
> tidak ada lagi "jalan di sini tapi tidak di sana."

---

## 🗄️ Database

setiap app butuh tempat nyimpan data. ada dua kategori utama:

**SQL (Relational)** — data terstruktur dengan relasi antar tabel:
```
MySQL       # paling populer, ringan, mudah dipelajari
PostgreSQL  # powerful, cocok untuk data kompleks dan analitik
MSSQL       # Microsoft SQL Server — cocok untuk ekosistem Windows
```

**NoSQL (Non-relational)** — data fleksibel tanpa schema ketat:
```
MongoDB    # document-based, struktur data fleksibel
Cassandra  # distributed, dirancang untuk data skala sangat besar
```

> pilih SQL kalau data lo terstruktur dan butuh relasi antar tabel.
> pilih NoSQL kalau data lo fleksibel, butuh speed tinggi, atau skala besar.

---

## 🌐 API

API adalah jembatan komunikasi antara app lo dengan service lain — atau antara frontend dan backend.

```
REST API   # standar paling umum — berbasis HTTP request/response
Endpoint   # URL spesifik yang bisa dipanggil
JSON       # format data yang paling sering dipakai
```

contoh endpoint dengan method CRUD (Create, Read, Update, Delete):

```
GET    /users        # ambil semua data user
GET    /users/1      # ambil data user dengan id 1
POST   /users        # buat user baru
PUT    /users/1      # update data user dengan id 1
DELETE /users/1      # hapus user dengan id 1
```

---

## 🔥 Firewall & Network

setelah server siap dan app berjalan — pastikan akses dari luar sudah dikonfigurasi dengan benar.

```
# on-premise → request ke tim infra untuk buka port
# cloud → konfigurasi di security group / firewall rules
```

port yang umum perlu dibuka:

```
22    # SSH  — remote akses ke server
80    # HTTP — web tidak terenkripsi
443   # HTTPS — web terenkripsi
```

port yang **tidak boleh** dibuka ke public:

```
3306  # MySQL
5432  # PostgreSQL
27017 # MongoDB
6379  # Redis
```

> **rule of thumb:** buka port sesedikit mungkin.
> port database harus selalu tertutup dari public internet.

---

## 📋 Recap

```
🖥️ Server      — tentukan: on-premise, VPS, atau cloud
🐧 OS          — fondasi server, rekomendasi Ubuntu Server
📊 Spec        — CPU, RAM, Storage, Network sesuai kebutuhan
🐳 Container   — Docker untuk environment yang konsisten
🗄️ Database    — SQL atau NoSQL sesuai struktur data
🌐 API         — jembatan komunikasi antar service
🔥 Firewall    — kontrol akses, tutup port yang tidak perlu
```

---

*x.com/xeenau · #keeplearning*
