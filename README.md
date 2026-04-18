# Tsukihime -A piece of blue glass moon- Script (HuneX Engine Parser)

Repositori ini berisi skrip hasil parser dari aset asli **Tsukihime -A piece of blue glass moon- (TsukiRe)** versi Switch. Data ini merupakan hasil ekstraksi dan dekompresi dari file utama yang dikemas dalam format **.nsp (Nintendo Submission Package)**.

---

## Spesifikasi Teknis Engine (HuneX Switch)
Skrip dalam repositori ini diproses berdasarkan pemahaman struktur internal engine HuneX untuk platform konsol:

* **Archive Utama:** `.nsp` (Nintendo Submission Package) - Kontainer distribusi aplikasi Nintendo Switch yang berisi file aset game.
* **Format Skrip:** `.mrg` (Script Text) - Berisi instruksi bytecode dan string dialog asli game.
* **Algoritma Kompresi:** **LenZu** (Variasi LZ77 + Huffman, LSB-first). Data skrip dalam repositori ini adalah hasil dekompresi dari format `.mrg` asli sehingga menjadi teks yang dapat dibaca manusia (human-readable).

---

## Konten Repositori
Hasil parser ini mencakup:
* **Dialog & Narasi:** String teks yang telah diekstrak dari bytecode `.mrg`.
* **Interpretasi Tag:** Pemetaan instruksi engine (seperti ruby teks, voice cue, dan efek transisi) yang tertanam di dalam skrip.
* **Struktur Bytecode:** Representasi urutan perintah engine yang memudahkan proses analisis alur cerita (rute).

---

## Informasi Format Aset Lainnya
Selain skrip, engine HuneX pada platform ini umumnya menggunakan:
* **.cbg** (Background/UI): Huffman + zero-alternate + delta filter.
* **.mzp** (Sprite/CG): MZX tiles (RLE + LZ + Huffman).

---

## Panduan Modding & Lokalisasi
Bagi modder yang ingin melakukan lokalisasi:
1. **Referensi Teks:** Gunakan teks dalam repositori ini sebagai basis terjemahan.
2. **Kompilasi Kembali:** Untuk mengembalikan teks ke dalam game, hasil terjemahan harus dikonversi kembali ke bytecode, dikompresi dengan algoritma **LenZu**, dan dimasukkan kembali ke dalam struktur kontainer `.mrg`.
3. **Injeksi:** File `.mrg` baru kemudian dipack kembali ke dalam struktur romfs untuk digunakan pada konsol yang sudah dimodifikasi atau emulator.

---

## Credits
* **Original Data:** Hasil parser dari proyek lokalisasi tim Tsukihimates.
* **Technical Research:** Reverse-engineering format HuneX (.mrg & LenZu).
* **Maintenance:** [Jannabie](https://github.com/Jannabie).

**Disclaimer:** *Repositori ini hanya bertujuan untuk riset teknis dan edukasi. Seluruh hak cipta konten asli dimiliki oleh TYPE-MOON / ANIPLEX / HuneX.*
