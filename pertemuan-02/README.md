# Pertemuan 2 - Format Dokumen XML

## 1. Profil XML

File `profil_saya.xml` dibuat untuk menyimpan data profil mahasiswa dalam struktur XML yang well-formed.

## 2. Analisis Kesalahan XML

| No | Bagian yang Salah | Alasan | Perbaikan |
|---|---|---|---|
| 1 | `<nama>Budi Santoso</Nama>` | Huruf besar dan kecil pada tag XML bersifat case-sensitive. Tag pembuka dan penutup harus sama. | Ubah menjadi `<nama>Budi Santoso</nama>` |
| 2 | `<hobi>Programming</hobi>` lalu `<hobi>Membaca</hobi>` tanpa masalah struktur lain, tetapi jika ada tag yang tidak ditutup maka XML menjadi tidak well-formed. | Setiap elemen XML wajib memiliki tag penutup yang sesuai. | Pastikan setiap `<hobi>` ditutup dengan `</hobi>` |
| 3 | `<deskripsi>Saya suka AI & Web Semantik</deskripsi>` | Karakter `&` tidak boleh ditulis langsung dalam XML karena merupakan karakter khusus. | Ubah menjadi `Saya suka AI &amp; Web Semantik` |

## 3. Analisis XML Schema

1. Root element yang diizinkan: `buku`.
2. Tipe data elemen `judul`: `xs:string`.
3. Tipe data elemen `tahun`: `xs:gYear`.
4. Tipe data elemen `harga`: `xs:decimal`.
5. Atribut `isbn` wajib dituliskan karena pada XSD menggunakan `use="required"`.

## 4. Analisis Namespace

1. Kedua elemen `title` tidak dianggap sama karena berada pada namespace yang berbeda, yaitu namespace `buku` dan namespace `web`.
2. Prefix `buku` dan `web` digunakan untuk membedakan elemen yang berasal dari namespace berbeda.
3. Atribut `xmlns` digunakan untuk mendeklarasikan namespace XML.
4. URI namespace tidak harus dapat dibuka sebagai halaman web. URI berfungsi sebagai identitas unik untuk membedakan namespace.

## 5. Pertanyaan Evaluasi

1. **Apa perbedaan utama XML dan HTML?**  
   XML digunakan untuk menyimpan dan mengorganisasi data secara terstruktur, sedangkan HTML digunakan untuk menampilkan dan mengatur tampilan informasi pada halaman web.

2. **Apa yang dimaksud XML yang well-formed?**  
   XML well-formed adalah dokumen XML yang mengikuti aturan sintaks XML dengan benar, seperti memiliki satu root element, tag pembuka dan penutup yang sesuai, serta struktur elemen yang benar.

3. **Jelaskan perbedaan well-formed dan valid.**  
   Well-formed berarti dokumen mengikuti aturan sintaks XML. Valid berarti dokumen tidak hanya well-formed, tetapi juga sesuai dengan aturan struktur yang ditentukan oleh schema seperti XSD.

4. **Mengapa XSD lebih kuat dibandingkan DTD?**  
   XSD mendukung lebih banyak tipe data, namespace, serta aturan struktur dan validasi data yang lebih rinci dibandingkan DTD.

5. **Mengapa namespace penting ketika data XML berasal dari beberapa kosakata berbeda?**  
   Namespace mencegah konflik nama elemen yang sama dengan memberikan identitas berbeda berdasarkan namespace masing-masing.

6. **Apa kegunaan XPath dalam pengolahan dokumen XML?**  
   XPath digunakan untuk memilih, mencari, dan mengambil elemen, atribut, atau nilai tertentu dari struktur dokumen XML.
