# 🌐 Basic Networking

> essential networking concepts yang wajib dipahami sebelum masuk ke konfigurasi apapun.

---

## 📡 Core Concepts

sebelum masuk ke command atau konfigurasi, pahami terlebih dahulu konsep dasar, berikut ini adalah fondasi dari seluruh networking.

```
IP Address     # alamat unik setiap device di jaringan
Subnet Mask    # menentukan range jaringan (ex: 255.255.255.0)
Gateway        # pintu keluar ke jaringan lain / internet
DNS            # translasi domain → IP (google.com → 142.250.x.x)
DHCP           # auto assign IP ke device
NAT            # translate IP private → public
```

---

## 🔢 Subnetting

subnetting adalah cara membagi jaringan menjadi bagian yang lebih kecil. ada dua pendekatan yaitu classful dan CIDR. keduanya masih relevan dan wajib dipahami.

```
# Class
Class A  # 1.0.0.0   - 126.255.255.255  /8   — skala besar
Class B  # 128.0.0.0 - 191.255.255.255  /16  — skala medium
Class C  # 192.0.0.0 - 223.255.255.255  /24  — skala kecil, paling umum

# CIDR
192.168.1.0/24    # /24 = 254 host tersedia
192.168.1.0/16    # /16 = 65.534 host tersedia
192.168.1.0/32    # /32 = 1 host (specific IP)

# Private IP ranges (tidak dapat diakses dari internet)
10.0.0.0/8        # 10.x.x.x
172.16.0.0/12     # 172.16.x.x - 172.31.x.x
192.168.0.0/16    # 192.168.x.x

# Public IP  = dapat diakses dari internet
# Private IP = hanya dapat diakses di jaringan lokal
```

> **/24 artinya 24 bit pertama = network, sisanya = host.**
> semakin besar angka prefix → semakin sedikit host yang tersedia.

---

## 🔄 Protokol Wajib Tahu

protokol adalah aturan komunikasi antar device. setiap protokol memiliki tujuan dan port masing-masing wajib dipahami.

```
TCP   # reliable, ada handshake — HTTP, SSH, FTP
UDP   # fast, no guarantee — DNS, video streaming, gaming
HTTP  # port 80  — web tidak terenkripsi
HTTPS # port 443 — web terenkripsi (SSL/TLS)
SSH   # port 22  — remote access terenkripsi
RDP   # port 3389 — remote desktop Windows
FTP   # port 21  — file transfer (tidak aman)
SFTP  # port 22  — file transfer aman via SSH
DNS   # port 53  — domain name system
SMTP  # port 25  — kirim email antar server
```

---

## 🌍 DNS Records

DNS records adalah instruksi yang memberitahu internet ke mana traffic harus diarahkan untuk sebuah domain.

```
A      # domain → IPv4 (google.com → 142.250.x.x)
AAAA   # domain → IPv6
CNAME  # alias domain (www → domain.com)
MX     # mail server record
TXT    # verifikasi domain, SPF, DKIM
NS     # name server record
PTR    # reverse DNS (IP → domain)
```

---

## 📊 OSI Model

OSI model adalah kerangka 7 layer yang menjelaskan bagaimana data berpindah dari satu device ke device lain. saat troubleshooting network issue, ini adalah panduan untuk menentukan di layer mana masalah terjadi.

```
Layer 7 - Application   # HTTP, FTP, DNS, SSH
Layer 6 - Presentation  # SSL/TLS, enkripsi, format data
Layer 5 - Session       # manage & maintain koneksi
Layer 4 - Transport     # TCP, UDP — port number
Layer 3 - Network       # IP address, routing
Layer 2 - Data Link     # MAC address, switch
Layer 1 - Physical      # kabel, WiFi, sinyal
```

> tips hafal dari layer 7 ke 1: **"All People Seem To Need Data Processing"**
>
> setiap huruf pertama = nama layer:
> - **A**ll → Application
> - **P**eople → Presentation
> - **S**eem → Session
> - **T**o → Transport
> - **N**eed → Network
> - **D**ata → Data Link
> - **P**rocessing → Physical

---

*x.com/xeenau · #keeplearning*
