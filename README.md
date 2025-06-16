# keterlambatan_kriptografi

Nama : Raditya Hardian Santoso
NRP : 5027231033

Dokumentasi ini merupakan rangkuman dari pertemuan kelompok mata kuliah kriptografi, dengan topik utama **Kriptografi**, yang dipresentasikan oleh Kelompok 7. Materi disampaikan secara visual, teknis, dan disertai demonstrasi praktik enkripsi secara langsung menggunakan berbagai alat bantu.

Pertemuan ini bertujuan untuk memperkenalkan dasar teori kriptografi modern, perbedaan antar jenis algoritma kriptografi, cara kerja proses enkripsi-dekripsi, serta penerapannya di dunia nyata.

---

## 📌 Daftar Isi

- [1. Pendahuluan](#1-pendahuluan)
- [2. Dasar Teori Kriptografi](#2-dasar-teori-kriptografi)
- [3. Jenis-Jenis Algoritma Kriptografi](#3-jenis-jenis-algoritma-kriptografi)
- [4. Visualisasi Materi](#4-visualisasi-materi)
- [5. Studi Kasus dan Demonstrasi](#5-studi-kasus-dan-demonstrasi)
- [6. Tools & Sumber Belajar](#6-tools--sumber-belajar)
- [7. Insight dan Refleksi](#7-insight-dan-refleksi)
- [8. Referensi](#8-referensi)
---

## 1. 📖 Pendahuluan

Kriptografi merupakan cabang ilmu yang berfokus pada pengamanan informasi melalui teknik penyandian. Dalam dunia modern yang serba digital, kriptografi menjadi pilar penting dalam menjaga privasi, keamanan, dan keaslian informasi yang dikirimkan melalui jaringan.

### Tujuan Umum:
- Melindungi data dari akses tidak sah
- Menjamin integritas dan autentikasi data
- Mencegah penyangkalan terhadap transaksi atau komunikasi digital

---

## 2. 🧠 Dasar Teori Kriptografi

### Konsep Dasar:
- **Plaintext**: Pesan asli yang belum dienkripsi
- **Ciphertext**: Pesan terenkripsi yang tidak dapat dipahami tanpa kunci
- **Key**: Nilai rahasia yang digunakan untuk enkripsi dan dekripsi
- **Cipher**: Algoritma yang mengubah plaintext menjadi ciphertext

### Prinsip Utama Kriptografi (CIA + AN):
1. **Confidentiality**: Kerahasiaan informasi
2. **Integrity**: Keutuhan data (tidak berubah)
3. **Authentication**: Verifikasi identitas
4. **Non-repudiation**: Tidak bisa menyangkal keterlibatan

---

## 3. 🔄 Jenis-Jenis Algoritma Kriptografi

### 3.1 Kriptografi Simetris
- Menggunakan **satu kunci yang sama** untuk enkripsi dan dekripsi.
- Lebih cepat namun kurang aman untuk komunikasi terbuka.

**Contoh Algoritma:**
- **AES (Advanced Encryption Standard)**
- **DES (Data Encryption Standard)**
- **Blowfish**

**Struktur Umum AES (128-bit):**

''' [Plaintext] → AddRoundKey → [9 Rounds: SubBytes → ShiftRows → MixColumns → AddRoundKey] → Final Round → [Ciphertext] '''


### 3.2 Kriptografi Asimetris
- Menggunakan **dua kunci berbeda**: public key (untuk enkripsi) dan private key (untuk dekripsi).
- Lebih aman, namun secara komputasi lebih lambat.

**Contoh Algoritma:**
- **RSA (Rivest–Shamir–Adleman)**
- **ECC (Elliptic Curve Cryptography)**

**Contoh RSA:**
1. Pilih dua bilangan prima: `p` dan `q`
2. Hitung `n = p * q`
3. Hitung `φ(n) = (p-1)*(q-1)`
4. Pilih `e` sedemikian sehingga `1 < e < φ(n)` dan `gcd(e, φ(n)) = 1`
5. Hitung `d ≡ e⁻¹ mod φ(n)`

Kunci publik = `(e, n)`  
Kunci privat = `(d, n)`

---

## 4. 🎨 Visualisasi Materi

Presentasi disusun dengan visualisasi untuk memperjelas konsep kriptografi. Beberapa visual penting:

| Konsep                          | Visualisasi Digunakan                                  |
|--------------------------------|----------------------------------------------------------|
| Proses Enkripsi Simetris       | Flowchart: plaintext → AES → ciphertext                 |
| RSA Key Exchange                | Diagram komunikasi dua pihak dengan public/private key  |
| Caesar Cipher                   | Animasi pergeseran alfabet                              |
| Perbandingan Simetris vs Asimetris | Tabel: kecepatan, keamanan, kompleksitas                |

Visualisasi disajikan dalam bentuk slide interaktif, video pendek, dan demonstrasi langsung menggunakan tools online.

---

## 5. 🔧 Studi Kasus dan Demonstrasi

### Studi Kasus:
**Skenario:** Seorang pengguna ingin mengirim pesan rahasia melalui jaringan tidak aman.  
Solusi yang dibahas:
- Menggunakan enkripsi AES (simetris) untuk efisiensi.
- Mendahului dengan pertukaran kunci RSA (asimetris) untuk keamanan kanal.

### Demonstrasi:
1. **Caesar Cipher (Manual)**
   - Plaintext: `HELLO`
   - Shift: `+3`
   - Ciphertext: `KHOOR`

2. **AES (Menggunakan CyberChef)**
   - Plaintext: `ini adalah pesan rahasia`
   - Kunci (128-bit): `1234567890abcdef`
   - Output: Ciphertext dalam base64/hex

3. **RSA Key Generation (dengan calculator)**
   - `p = 17`, `q = 11` → `n = 187`
   - `φ(n) = 160`, `e = 7`, `d = 23`
   - Public key: `(7, 187)`, Private key: `(23, 187)`

---

## 6. 🧰 Tools & Sumber Belajar

| Tool / Website       | Fungsi                                      |
|----------------------|---------------------------------------------|
| CyberChef            | Simulator enkripsi AES, base64, hash, dll   |
| Cryptii              | Enkripsi klasik: Caesar, Vigenère, Morse    |
| RSA Calculator       | Pembuatan manual key RSA                    |
| Google Slides        | Visualisasi dan animasi enkripsi            |

---

## 7. ✍️ Insight dan Refleksi

- Kriptografi bukan hanya teori, tapi sangat kontekstual dan digunakan di hampir semua aspek digital modern.
- Enkripsi **tidak menjamin keutuhan data**, sehingga harus dikombinasikan dengan hashing (misalnya SHA-256) atau digital signature.
- Tantangan saat ini bukan hanya membuat algoritma yang kuat, tapi juga menjaga **manajemen kunci** dan performa sistem.

**Catatan Penting:**
- Jangan pernah membuat sistem kriptografi sendiri dari nol untuk aplikasi nyata — gunakan standar yang telah diuji komunitas.
- HTTPS, SSL/TLS, JWT, dan PGP adalah contoh nyata penggunaan kriptografi.

---

## 8. 📚 Referensi

- Stallings, W. (2020). *Cryptography and Network Security: Principles and Practice*
- Paar, C., & Pelzl, J. (2010). *Understanding Cryptography*
- NIST - National Institute of Standards and Technology
- https://gchq.github.io/CyberChef/
- https://cryptii.com/
- https://www.cs.drexel.edu/~introcs/Fa15/notes/09.3_RSA.html


