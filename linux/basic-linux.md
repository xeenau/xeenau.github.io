# 🐧 Basic Linux Commands

> essential commands yang wajib dikuasai berikut dikelompokkan per kategori.

---

## 🌐 Networking

```bash
ping google.com              # test konektivitas internet
curl https://api.com         # test API endpoints
wget https://file.com/file   # download file
netstat -tulpn               # cek port yang sedang listening
ifconfig                     # cek IP (sistem lama)
ip a                         # cek IP (sistem modern)
ssh user@192.168.1.1         # remote connection terenkripsi
scp file user@host:/path     # copy file secara aman
```

---

## 💻 System (OS)

```bash
pwd                         # tampilkan direktori saat ini
ls                          # list file
ls -la                      # list semua file (termasuk hidden)
cd /var/log                 # pindah direktori
cd ..                       # naik satu level
cd ~                        # kembali ke home directory
top                         # monitor sistem real-time
htop                        # monitor sistem (lebih visual)
ps aux                      # tampilkan semua proses yang berjalan
ps aux | grep nginx         # cari proses spesifik
kill 1234                   # hentikan proses berdasarkan PID
killall nginx               # hentikan semua proses nginx
uname -a                    # informasi sistem
hostname                    # tampilkan hostname
whoami                      # tampilkan user saat ini
```

---

## 📂 File Operations

```bash
cp file.txt backup/         # copy file
cp -r folder backup/        # copy folder secara rekursif
mv old.txt new.txt          # rename file
mv file.txt /tmp/           # pindahkan file
rm file.txt                 # hapus file
rm -rf folder/              # hapus folder (gunakan dengan hati-hati)
mkdir newfolder             # buat direktori baru
mkdir -p path/to/folder     # buat direktori bertingkat
cat file.txt                # tampilkan isi file
less file.txt               # tampilkan file (dengan paginasi)
nano file.txt               # edit file (ramah untuk pemula)
vim file.txt                # edit file (tingkat lanjut)
touch file.txt              # buat file kosong
chmod 755 script.sh         # set permission rwxr-xr-x
chmod +x script.sh          # jadikan file executable
chown user:group file       # ubah kepemilikan file
```

---

## 🔐 Security

```bash
sudo command                # jalankan sebagai superuser
sudo su                     # beralih ke root
chmod 600 private.key       # amankan file private (rw owner only)
chmod 644 file.txt          # permission file standar (rw-r--r--)
chmod 700 ~/.ssh            # amankan direktori SSH
ssh-keygen -t rsa           # generate SSH key pair
ssh-keygen -t ed25519       # generate SSH key modern
ufw status                  # cek status firewall
ufw enable                  # aktifkan firewall
ufw allow 22                # izinkan port SSH
ufw allow 80/tcp            # izinkan HTTP
history                     # lihat riwayat command
history | grep sudo         # cari riwayat command tertentu
export HISTSIZE=0           # nonaktifkan history (untuk keamanan)
```

---

## 🔍 Troubleshooting

```bash
tail -f /var/log/syslog    # monitor log secara live
tail -n 100 error.log      # lihat 100 baris terakhir log
grep "error" log.txt       # cari teks dalam file
grep -r "TODO" .           # cari secara rekursif di semua file
find . -name "*.log"       # temukan file berdasarkan nama
find . -type f -mtime -7   # temukan file yang dimodifikasi 7 hari terakhir
df -h                      # cek penggunaan disk (human readable)
du -sh folder/             # cek ukuran folder
free -h                    # cek penggunaan memori
systemctl status nginx     # cek status service
systemctl restart nginx    # restart service
systemctl enable nginx     # aktifkan service saat boot
journalctl -xe             # lihat log sistem
journalctl -u nginx        # lihat log service tertentu
netstat -tulpn | grep :80  # cek apa yang menggunakan port 80
lsof -i :8080              # cek proses yang menggunakan port 8080
```

---

*x.com/xeenau · #keeplearning*
