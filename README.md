# Tsukihime -A piece of blue glass moon- Script (HuneX Engine Parser)

Repositori ini berisi skrip hasil parser dari aset asli **Tsukihime -A piece of blue glass moon- (TsukiRe)**. Data ini diekstrak dari kontainer **HuneX File Archive (.hfa)** menggunakan metode dekompresi dan decoding yang spesifik untuk format engine HuneX.

---

## Spesifikasi Teknis Engine (HuneX)
Skrip dalam repositori ini diproses berdasarkan pemahaman struktur internal HuneX:

* **Archive Utama:** `.hfa` (HuneX File Archive) - Kontainer tanpa kompresi pada level arsip, namun berisi file internal yang terkompresi.
* **Format Skrip:** `.ctd` (Script Text) - Berisi instruksi bytecode dan string dialog.
* **Algoritma Kompresi:** **LenZu** (Variasi LZ77 + Huffman, LSB-first). Data skrip dalam repositori ini adalah hasil dekompresi dari format ini sehingga menjadi teks yang dapat dibaca.

---

## Konten Repositori
Hasil parser ini mencakup:
* **Dialog & Narasi:** String teks yang sudah didecode dari bytecode `.ctd`.
* **Identifikasi Tag:** Tag instruksi engine (seperti ruby, voice, dan sinkronisasi teks) yang sudah dipetakan secara jelas.
* **Metadata Offset:** Informasi alamat memori asli untuk mendukung proses injeksi kembali ke format `.ctd` yang terkompresi.

---

## Informasi Format Aset Lainnya
Sebagai referensi modding lebih lanjut, engine ini menggunakan format:
* **.cbg** (Background/UI): Menggunakan filter Huffman + zero-alternate + delta.
* **.mzp** (Sprite/CG): Menggunakan metode MZX tiles (RLE + LZ + Huffman).

---

## Cara Penggunaan
Bagi modder yang ingin melakukan lokalisasi:
1. Gunakan teks dalam repositori ini sebagai sumber referensi utama.
2. Proses translasi dilakukan pada bagian string dialog.
3. Untuk mengembalikan ke dalam game, teks harus dikompresi kembali menggunakan algoritma **LenZu** dan dimasukkan ke dalam struktur `.ctd`, kemudian dipack ulang ke dalam `.hfa`.

---

## Credits
* **Data Source:** Tsukihimates (Original English Localization Team).
* **Technical Research:** HuneX Engine reverse-engineering.
* **Maintenance:** [Jannabie](https://github.com/Jannabie).

**Disclaimer:** *Repositori ini hanya bertujuan untuk riset teknis dan edukasi. Seluruh hak cipta konten asli dimiliki oleh TYPE-MOON / ANIPLEX / HuneX.*
