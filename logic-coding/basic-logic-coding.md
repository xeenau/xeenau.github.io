# 💡 Logic & Coding

> sebelum memikirkan bahasa pemrograman alangkah baiknya pahami terlebih dahulu cara komputer berpikir.

---

## 🤖 Apa itu Programming?

komputer tidak dapat berpikir sendiri. komputer hanya dapat mengikuti perintah satu per satu, secara berurutan.

tugas seorang programmer adalah memberikan perintah yang jelas dan terstruktur.

contoh paling sederhana:

```python
print("Hello, World!")
```

kode ditulis → komputer membaca → output muncul. sesederhana itu.

> coding adalah bahasa untuk berkomunikasi dengan komputer.
> semakin dalam pemahamannya, semakin kompleks instruksi yang dapat diberikan.

---

## 🧠 3 Logic Dasar

komputer bekerja secara sequential yaitu satu perintah selesai, baru lanjut ke berikutnya.
namun logic dasarnya hanya ada 3:

```
1. sequence   # jalankan satu per satu
2. condition  # kalau ini → lakukan itu
3. loop       # ulangi sampai selesai
```

> semua program di dunia, sebesar apapun, dibangun dari 3 hal ini.

---

## 📦 Konsep Dasar

ketiga logic tersebut membutuhkan "wadah" untuk berjalan. berikut konsep dasar yang wajib dipahami:

```python
# variable — tempat menyimpan data
nama   = "xeenau"  # string (teks)
umur   = 20        # integer (angka)
tinggi = 170.5     # float (desimal)
aktif  = True      # boolean (true/false)

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

# function — kumpulan perintah yang dapat dipanggil ulang
def sapa(nama):
    return "halo, " + nama + "!"

print(sapa("xeenau"))
```

---

## 🔢 Data Type

setiap variable memiliki tipe data, Python dapat mengeceknya menggunakan `type()`:

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

install Python di [python.org](https://python.org), buka VSCode, buat file `main.py`, tulis kode, jalankan:

```bash
python main.py
```

atau langsung practice di browser tanpa instalasi apapun:
🔗 [xeenau.github.io/lab/python](https://xeenau.github.io/lab/python)

---

## 🔁 Tips Practice

ini baru logic dasarnya, belum masuk ke bahasa pemrograman spesifik, belum web, belum backend, belum AI.

namun ini adalah fondasi dari segalanya. semua bahasa pemrograman menggunakan logic yang sama.

coba secara mandiri:
- ganti variabel, ganti angka, ganti kondisi
- perhatikan bagaimana output berubah
- ulangi dengan use case yang berbeda sampai benar-benar paham, bukan sekadar hafal

> logic ini yang akan digunakan seumur hidup sebagai programmer.

---

*x.com/xeenau · #keeplearning*
