# 💡 Logic & Coding

> sebelum mikirin bahasa programming — pahami dulu cara komputer berpikir.

---

## 🤖 Apa itu Programming?

komputer itu bodoh. dia gak bisa mikir sendiri.
dia cuma bisa ngikutin perintah — satu per satu.

tugas lo sebagai programmer? ngasih perintah yang jelas.

contoh paling simple di dunia coding:

```python
print("Hello, World!")
```

lo tulis itu → komputer baca → keluar tulisan. sesimpel itu.

> coding = bahasa buat ngomong ke komputer.
> makin lo paham bahasanya, makin kompleks yang bisa lo suruh dia kerjain.

---

## 🧠 3 Logic Dasar

komputer kerja secara sequential — satu perintah selesai, baru lanjut ke berikutnya.
tapi logic dasarnya cuma 3:

```
1. sequence   # jalankan satu per satu
2. condition  # kalau ini → lakukan itu
3. loop       # ulangi sampai selesai
```

> semua program di dunia — sebesar apapun — dibangun dari 3 hal ini.

---

## 📦 Konsep Dasar

3 logic tadi butuh "wadah" buat jalan. ini konsep dasar yang wajib lo tau:

```python
# variable — tempat nyimpan data
nama = "xeenau"    # string (teks)
umur = 20          # integer (angka)
tinggi = 170.5     # float (desimal)
aktif = True       # boolean (true/false)

# condition — if this → do that
if umur >= 17:
    print("boleh masuk")
elif umur >= 13:
    print("remaja")
else:
    print("belum cukup umur")

# loop — ulangi sampai kondisi terpenuhi
for i in range(3):
    print("halo!")    # diulang 3x

# function — kumpulan perintah yang bisa dipanggil ulang
def sapa(nama):
    return "halo, " + nama + "!"

print(sapa("xeenau"))
```

---

## 🔢 Data Type

tiap variable punya tipe data — Python bisa cek pakai `type()`:

```python
nama   = "xeenau"   # str   — teks
umur   = 20         # int   — angka bulat
tinggi = 170.5      # float — angka desimal
aktif  = True       # bool  — True atau False

print(type(nama).__name__)    # str
print(type(umur).__name__)    # int
print(type(tinggi).__name__)  # float
print(type(aktif).__name__)   # bool
```

---

## 🛠️ Mulai dari Mana?

install Python di [python.org](https://python.org), buka VSCode, buat file `main.py`, tulis code, run:

```bash
python main.py
```

atau langsung practice di browser tanpa install apapun:
🔗 [xeenau.github.io/lab/python](https://xeenau.github.io/lab/python)

---

## 🔁 Tips Practice

ini baru logic dasarnya — belum masuk ke bahasa programming spesifik, belum web, belum backend, belum AI.

tapi ini fondasi lo. semua bahasa pakai logic yang sama.

sekarang coba sendiri:
- ganti variabel, ganti angka, ganti kondisi
- lihat outputnya berubah
- ulang-ulang dengan use case yang berbeda — sampai lo ngerti, bukan cuma hafal

> logic ini yang akan lo pakai seumur hidup sebagai programmer.

---

*x.com/xeenau · #keeplearning*
