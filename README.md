# Tsukihime -A piece of blue glass moon- Script (Tsukihimates Parser)

Kumpulan skrip hasil parser dari proyek lokalisasi **Tsukihimates** untuk game **Tsukihime -A piece of blue glass moon- (TsukiRe)**. Repositori ini berisi data teks dan instruksi game yang telah dikonversi ke format yang lebih mudah dibaca untuk kebutuhan modding, riset, atau fan-translation ke bahasa lain.

---

## Tentang Proyek
Data yang ada di sini merupakan hasil ekstraksi dan parsing teknis dari aset asli game menggunakan toolset yang dikembangkan oleh tim **Tsukihimates**. Proyek ini bertujuan untuk menyediakan referensi skrip yang terstruktur bagi komunitas.

---

## Struktur Data
Skrip dalam repositori ini telah diproses sehingga memiliki struktur sebagai berikut:
* **Format:** File teks terstruktur (JSON/YAML/TXT) hasil parsing bytecode asli.
* **Konten:** Mencakup dialog narasi, pilihan rute (choices), dan tag instruksi engine.
* **Encoding:** Menggunakan standar UTF-8 untuk mendukung karakter khusus dan kanji Jepang secara akurat.

---

## Catatan Teknis
Harap diperhatikan bahwa skrip ini adalah hasil **Parser**:
1. **Bukan Plain Text Mentah:** Skrip ini sudah melalui tahap interpretasi bytecode agar tag-tag seperti `[ruby]`, `[voice]`, dan `[wait]` dapat diidentifikasi dengan jelas.
2. **Sinkronisasi Offset:** Beberapa file mungkin menyertakan alamat memori atau offset asli untuk memudahkan proses injeksi kembali (re-injection) ke dalam file `.crypt` atau `.dat` game.
3. **Kompatibilitas:** Struktur ini mengikuti format yang digunakan oleh tim Tsukihimates dalam patch bahasa Inggris mereka.

---

## Cara Penggunaan
Bagi modder yang ingin melakukan lokalisasi (misal: Bahasa Indonesia):
* Gunakan file-file ini sebagai referensi sumber teks.
* Lakukan proses terjemahan pada bagian dialog tanpa mengubah tag instruksi (seperti `@name`, `@voice`).
* Gunakan tool re-packer yang kompatibel untuk mengembalikan skrip ke format binari game.

---

## Credits
* **Parser Tool & Data:** [Tsukihimates Team](https://tsukihimates.com/) (Original Parser).
* **Maintenance:** [Jannabie](https://github.com/Jannabie) (Repository maintainer).

**Disclaimer:** *Repositori ini hanya bertujuan untuk riset dan edukasi. Hak cipta konten asli tetap dimiliki oleh TYPE-MOON / ANIPLEX.*
