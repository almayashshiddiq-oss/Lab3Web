<img width="1275" height="579" alt="SS tgs pemerograman 2" src="https://github.com/user-attachments/assets/2affc282-4970-4661-8134-4da02f98c660" />


1. Mengubah dan menambah properti CSS
Buka `style_eksternal.css`. Coba ubah nilai `background-color`, `color`, `font-size`, `padding`, `margin`, `border-radius`, dan `line-height`. Simpan file lalu muat ulang halaman di browser untuk melihat hasilnya.

2. Mencoba selector `h1` dan `#intro h1`
Selector `h1` menargetkan semua elemen `<h1>`, sedangkan `#intro h1` hanya menargetkan elemen `<h1>` di dalam elemen yang memiliki ID `intro`. Selector yang lebih spesifik biasanya menang untuk properti yang sama jika tidak ada aturan cascade lain yang mengalahkannya.

3.. Membandingkan CSS internal, eksternal, dan inline
CSS internal ditulis di dalam tag `<style>`, CSS eksternal berada di file terpisah dan dihubungkan dengan `<link>`, sedangkan inline CSS ditulis pada atribut `style` di elemen HTML. Untuk deklarasi biasa pada properti yang sama, inline CSS umumnya lebih diprioritaskan daripada internal dan eksternal. `!important`, spesifisitas, dan urutan aturan juga memengaruhi hasil akhir.

4. Membandingkan selector ID dan Class
Elemen contoh pada halaman:

```html
<p id="paragraf-1" class="text-paragraf">
    Paragraf ini menggunakan selector ID dan Class sekaligus.
</p>
```

`#paragraf-1` adalah selector ID dan `.text-paragraf` adalah selector Class. ID memiliki spesifisitas lebih tinggi daripada Class untuk deklarasi biasa yang mengatur properti yang sama. Pada contoh di halaman, ID menentukan warna teks, sedangkan Class memberikan latar belakang dan garis di sisi paragraf.




5. Eksperimen Mengubah dan Menambah Properti CSS

Pada bagian ini dilakukan eksperimen dengan mengubah nilai properti CSS dan menambahkan beberapa properti baru agar tampilan halaman web lebih menarik.

Contoh CSS yang dimodifikasi:

```css
body {
    font-family: Arial, sans-serif;
    background-color: #f0f4f8;
    color: #333333;
    margin: 0;
    padding: 20px;
}

header {
    min-height: 80px;
    background-color: #1565c0;
    border-bottom: 3px solid #00bcd4;
    padding: 10px;
}

h1 {
    font-size: 30px;
    color: white;
    text-align: center;
    padding: 20px 10px;
}

h1 i {
    color: #ffeb3b;
}

#intro {
    background-color: white;
    padding: 25px;
    margin: 20px auto;
    border-radius: 10px;
    max-width: 800px;
    box-shadow: 0 4px 10px #cccccc;
}

#intro p {
    font-size: 16px;
    line-height: 1.8;
    text-align: justify;
}

.button {
    display: inline-block;
    background-color: #1565c0;
    color: white;
    padding: 10px 18px;
    text-decoration: none;
    border-radius: 5px;
}

.button:hover {
    background-color: #00bcd4;
}
```
Hasil Eksperimen

- `background-color` digunakan untuk mengubah warna latar belakang.
- `font-size` digunakan untuk mengatur ukuran tulisan.
- `color` digunakan untuk mengubah warna teks.
- `line-height` digunakan untuk mengatur jarak antarbaris.
- `padding` digunakan untuk mengatur jarak antara isi dan tepi elemen.
- `border-radius` digunakan untuk membuat sudut elemen menjadi melengkung.
- `box-shadow` digunakan untuk memberikan efek bayangan.
- `:hover` digunakan untuk mengubah tampilan tombol ketika kursor diarahkan ke tombol tersebut.

Kesimpulan: perubahan properti dan nilai CSS dapat mengubah warna, ukuran, jarak, serta tampilan elemen HTML tanpa harus mengubah struktur HTML-nya.

6. Perbedaan Deklarasi CSS `h1` dan `#intro h1`

Kedua deklarasi tersebut memiliki perbedaan pada elemen HTML yang menjadi target CSS.

### A. Selector `h1`

```css
h1 {
    color: blue;
    font-size: 24px;
}
```

CSS tersebut berlaku untuk semua elemen `<h1>` di halaman, selama tidak ada aturan lain yang mengubah hasil tampilannya.

 B. Selector `#intro h1`

```css
#intro h1 {
    color: red;
    font-size: 30px;
}
```

CSS tersebut hanya berlaku untuk elemen `<h1>` yang berada di dalam elemen dengan ID `intro`.

Contoh HTML:

```html
<h1>Judul Utama</h1>

<div id="intro">
    <h1>Hello World</h1>
</div>
```

Hasil: tulisan “Judul Utama” berwarna biru dan berukuran 24 px, sedangkan tulisan “Hello World” berwarna merah dan berukuran 30 px.

Kesimpulan: selector `h1` menargetkan semua elemen `<h1>`, sedangkan `#intro h1` hanya menargetkan elemen `<h1>` di dalam elemen dengan ID `intro`. Selector `#intro h1` juga memiliki tingkat spesifisitas lebih tinggi daripada selector `h1`.

7. Prioritas CSS Internal, Eksternal, dan Inline

Apabila CSS internal, eksternal, dan inline diterapkan pada elemen yang sama, CSS inline umumnya memiliki prioritas lebih tinggi daripada CSS internal dan eksternal biasa, dengan asumsi deklarasi lainnya memiliki tingkat kepentingan yang sama.

Contoh CSS eksternal (`style.css`):

```css
h1 {
    color: blue;
}
```

Contoh CSS internal di dalam HTML:

```html
<style>
    h1 {
        color: green;
    }
</style>
```

Contoh CSS inline:

```html
<h1 style="color: red;">Hello World</h1>
```

Hasil: tulisan “Hello World” berwarna merah karena properti `color` ditentukan langsung melalui atribut `style` pada elemen HTML.

Urutan prioritas secara umum:

- Inline CSS umumnya mengalahkan aturan internal dan eksternal biasa untuk properti yang sama.
- Prioritas CSS internal dan eksternal ditentukan oleh spesifisitas, urutan deklarasi, dan penggunaan `!important`.
- Jika tingkat kepentingan dan spesifisitas sama, aturan yang ditulis belakangan biasanya diterapkan.

Kesimpulan: pada contoh di atas, inline CSS menghasilkan warna merah karena ditulis langsung pada elemen `<h1>`. Namun, deklarasi `!important`, spesifisitas, dan cascade dapat memengaruhi hasil akhir.

8. Prioritas Selector ID dan Class

Diketahui elemen HTML berikut:

```html
<p id="paragraf-1" class="text-paragraf">
    Saya sedang belajar CSS.
</p>
```

Terdapat dua selector CSS yang menargetkan elemen tersebut.

 A. Selector ID

```css
#paragraf-1 {
    color: red;
    font-size: 20px;
}
```

### B. Selector Class

```css
.text-paragraf {
    color: blue;
    font-size: 16px;
}
```

**Hasil:** teks paragraf akan berwarna merah dengan ukuran font 20 px karena selector ID memiliki tingkat spesifisitas lebih tinggi daripada selector Class untuk properti yang sama.

Perbandingan spesifisitas:

| Selector | Tingkat spesifisitas |
| --- | --- |
| `p` (elemen) | `0-0-1` |
| `.text-paragraf` (class) | `0-1-0` |
| `#paragraf-1` (ID) | `1-0-0` |

Contoh tambahan:

```css
#paragraf-1 {
    color: red;
}

.text-paragraf {
    color: blue !important;
}
```

Dalam contoh tambahan ini, teks akan berwarna biru karena deklarasi Class menggunakan `!important`, sedangkan deklarasi ID tidak. Jadi, prioritas tidak hanya ditentukan oleh ID atau Class, tetapi juga oleh kepentingan deklarasi dan aturan cascade.

Kesimpulan: jika selector ID dan Class sama-sama mengatur properti yang sama tanpa `!important`, selector ID akan menang karena tingkat spesifisitasnya lebih tinggi. Properti lain yang tidak bertentangan tetap dapat diterapkan dari selector Class.
