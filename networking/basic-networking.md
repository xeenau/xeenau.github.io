# 🌐 Basic Networking

> essential networking concepts yang wajib dipahami.

---

## 📡 Core Concepts

sebelum masuk ke command atau konfigurasi apapun, pahami dulu konsep dasar ini — ini fondasi semua networking.

```
IP Address     # Alamat unik setiap device di jaringan
Subnet Mask    # Menentukan range jaringan (ex: 255.255.255.0)
Gateway        # Pintu keluar ke jaringan lain / internet
DNS            # Translasi domain → IP (google.com → 142.250.x.x)
DHCP           # Auto assign IP ke device
NAT            # Translate IP private → public
```

---

## 🔢 Subnetting

subnetting adalah cara membagi jaringan jadi bagian lebih kecil. ada dua cara classful dan CIDR. keduanya masih relevan dan wajib paham.

```
# Class 
Class A  # 1.0.0.0   - 126.255.255.255  /8   — skala besar
Class B  # 128.0.0.0 - 191.255.255.255  /16  — skala medium
Class C  # 192.0.0.0 - 223.255.255.255  /24  — skala kecil, paling umum

# CIDR 
192.168.1.0/24    # /24 = 254 host tersedia
192.168.1.0/16    # /16 = 65.534 host tersedia
192.168.1.0/32    # /32 = 1 host (specific IP)

# Private IP ranges (tidak bisa diakses dari internet)
10.0.0.0/8        # 10.x.x.x
172.16.0.0/12     # 172.16.x.x - 172.31.x.x
192.168.0.0/16    # 192.168.x.x

# Public IP  = bisa diakses dari internet
# Private IP = hanya bisa diakses di jaringan lokal
```

> **/24 artinya 24 bit pertama = network, sisanya = host.**
> makin besar angka prefix → makin sedikit host tersedia.

---

## 🔄 Protokol Wajib Tahu

protokol adalah aturan komunikasi antar device. tiap protokol punya tujuan dan port masing-masing — wajib hafal yang ini.

```
TCP   # Reliable, ada handshake — HTTP, SSH, FTP
UDP   # Fast, no guarantee — DNS, Video streaming, Gaming
HTTP  # Port 80  — web tidak terenkripsi
HTTPS # Port 443 — web terenkripsi (SSL/TLS)
SSH   # Port 22   — remote access terenkripsi
RDP   # Port 3389 — remote desktop Windows
FTP   # Port 21  — file transfer (tidak aman)
SFTP  # Port 22  — file transfer aman via SSH
DNS   # Port 53  — domain name system
SMTP  # Port 25  — kirim email antar server
```

---

## 🌍 DNS Records

DNS records adalah instruksi yang memberitahu internet kemana harus mengarahkan traffic untuk domain kamu.

```
A      # Domain → IPv4 (google.com → 142.250.x.x)
AAAA   # Domain → IPv6
CNAME  # Alias domain (www → domain.com)
MX     # Mail server record
TXT    # Verifikasi domain, SPF, DKIM
NS     # Name server record
PTR    # Reverse DNS (IP → domain)
```

---

## 📊 OSI Model

OSI model adalah kerangka 7 layer yang menjelaskan bagaimana data berpindah dari satu device ke device lain. pas troubleshooting network issue, ini panduan lo debug dari layer mana.

```
Layer 7 - Application   # HTTP, FTP, DNS, SSH
Layer 6 - Presentation  # SSL/TLS, enkripsi, format data
Layer 5 - Session       # Manage & maintain koneksi
Layer 4 - Transport     # TCP, UDP — port number
Layer 3 - Network       # IP address, routing
Layer 2 - Data Link     # MAC address, switch
Layer 1 - Physical      # Kabel, WiFi, sinyal
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
