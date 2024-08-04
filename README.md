<p><a href="https://www.buymeacoffee.com/ardean"> <img align="left" src="https://cdn.buymeacoffee.com/buttons/v2/default-yellow.png" height="50" width="210" alt="ardean" /></a><a href="https://ko-fi.com/ardean"> <img align="left" src="https://cdn.ko-fi.com/cdn/kofi3.png?v=3" height="50" width="210" alt="ardean" /></a></p><br><br>

![Logo](https://i.imgur.com/JTB841z.png)

# QR Code Generator

 Unggah logo Anda, pilih warna khusus, pilih pola, dan unduh kode QR. Format yang tersedia: .png, .svg.

 ![image](https://camo.envatousercontent.com/857ed2bda2fafa49ea01a9d76f1d1a5ebb042e72/68747470733a2f2f76656e6f2e65732f6173736574732f71726364722f71726364722d64656d6f2e6769663f763d342e30)
 
 ![images](https://i.imgur.com/nKrrmRQ.jpg)
 
# Fitur-fitur

- Color picker
- Custom Background and Foreground color
- Transparent background
- Gradient foreground
- Advanced QR Code patterns
- Custom QR Code Markers border and center
- Custom Frames
- Custom label
- Image uploader
- Custom watermarks
- Location search
- OpenMaps or GoogleMaps
- Responsive
- Multilanguage
- Easy setup
- Save QRcodes in .png and .svg format
- Custom theme color
- Custom layouts
- Live preview

# Jenis QR Code Tersedia

- Link
- Teks
- E-mail
- Lokasi (dengan GoogleMaps)
- Telepon
- SMS
- WhatsApp
- Skype
- Zoom
- Akses WI-Fi
- V-Card
- Acara
- Pembayaran PayPal
- Transaksi BitCoin

# Dokumentasi

## Instalasi

Salin semua file dan folder dari direktori /Qr ke File Manager web anda melalui FTP atau Direct Upload (letakkan semuanya di root jika Anda akan menggunakan seluruh domain sebagai pembuat kode QR, jika tidak, buat direktori khusus dan unggah semua isinya).

![images](https://i.imgur.com/ZBppiQl.png)

Navigasikan dengan browser Anda ke url tempat Anda mengunggah file.

Itu saja! Anda siap menggunakan Qr dengan pengaturan defaultnya.

## Opsi

Pengaturan default dapat disesuaikan di dalam file config.php:

```php
<?php

$_CONFIG = array(
    'lang' => 'id',                             // Bahasa Default
    'qrcodes_dir' => 'qrcodes',                 // Direktori QR Codes
    'delete_old_files' => true,                 // Hapus file lama secara berkala
    'file_lifetime' => 1,                       // Hapus file yang lebih lama dari..(jam) dari /qrcodes_dir/
    'uploader' => true,                         // Biarkan pengguna mengunggah logo mereka sendiri
    'qr_bgcolor' => '#FFFFFF',                  // Warna latar belakang default untuk kode qr yang dihasilkan
    'qr_color' => '#000000',                    // Warna latar depan default untuk kode qr yang dihasilkan
    'session_name' => 'qrSession',              // Nama sesi khusus untuk skrip || FALSE
    'placeholder' => 'images/placeholder.svg',  // Placeholder Default
    'link' => true,                             // Aktifkan tab Link
    'text' => true,                             // Aktifkan tab Teks
    'email' => true,                            // Aktifkan tab Email
    'location' => true,                         // Aktifkan tab Lokasi
    'tel' => true,                              // Aktifkan tab Telepon
    'sms' => true,                              // Aktifkan tab SMS
    'whatsapp' => true,                         // Aktifkan tab WhatsApp
    'skype' => true,                            // Aktifkan tab Skype
    'zoom' => true,                             // Aktifkan tab Zoom
    'wifi' => true,                             // Aktifkan tab WiFi
    'vcard' => true,                            // Aktifkan tab V-Card
    'event' => true,                            // Aktifkan tab Acara
    'paypal' => true,                           // Aktifkan tab PayPal
    'bitcoin' => true,                          // Aktifkan tab BitCoin
    'default_tab' => '#link',                   // Opsi Tersedia: #link | #text | #email | #location | #tel | #sms | #whatsapp | #skype | #zoom | #wifi | #vcard | #event | #paypal | #bitcoin
    'detect_browser_lang' => false,             // Mendeteksi Bahasa Browser
    'google_api_key' => 'YOUR-API-KEY',         // https://developers.google.com/maps/documentation/javascript/get-api-key#get-an-api-key
    'lat' => '40.7127837',                      // Garis lintang awal untuk peta lokasi
    'lng' => '-74.00594130000002',              // Garis bujur awal untuk peta lokasi
    'color_primary' => false,                   // Warna utama, digunakan untuk tombol dan latar belakang header. atur warna #hex atau false untuk mendapatkan warna acak
    'layout' => 'classic',                      // Tata letak utama: 'classic' || 'vertical'
    'sidebar' => 'right',                       // Posisi Sidebar: 'right' || 'left'
    'accordion' => true,                        // Ciutkan menu opsi: benar || PALSU
    'rounded_buttons' => '["tabnav", "options", "save"]',   // Tombol bulat selektif: '["tabnav", "options", "save"]' || false
    'precision' => 'Q',                         // Tersedia: L, M, Q, H
    'relative_path' => '',                      // Gunakan opsi ini jika Anda menempatkan index.php utama di lokasi yang berbeda, ini harus menjadi jalur direktori QR utama, relatif terhadap indeks
    'default_size' => '700',                    // Ukuran default kode QR akhir. nilai yang tersedia: '200', '300', '400', '500', '600', '700', '800'
    'brand_logo' => false,                      // set true untuk memaksa gambar pertama /images/watermarks/ sebagai logo default
    'options' => ['colors', 'design', 'logo', 'frame', 'options'], // available options ['colors', 'design', 'logo', 'frame', 'options']
    'debug_mode' => false,                       // Set true untuk melacak kesalahan
    );
```

 ## Watermark

Jika Anda ingin mengubah atau menyembunyikan Watermark default, cukup ganti atau hapus gambar di dalam `images/watermark/` File `.jpg, .gif, .png, .svg` tersedia.

![images](https://i.imgur.com/QJQaowS.png)

## Fonts (Jenis Huruf)

Anda dapat menambahkan font khusus untuk label bingkai di dalam folder `lib/fonts/`, formatnya harus .svg

## Lokasi

Jika Anda ingin mengaktifkan Google Maps dan bukan OpenMaps default, Anda harus mendapatkan satu API Key di sini:

[Google Developers](https://developers.google.com/maps/documentation/javascript/get-api-key#get-an-api-key)

dan salin ke dalam file config.php
Aktifkan `Maps Javascript API` dan juga `Places API` untuk proyek yang sama.

Jika Anda ingin mengubah lokasi default, perbarui nilai berikut di dalam file config.php:

```
 'lat' => '40.7127837',
 'lng' => '-74.00594130000002',
 ```

 ## Kustomisasi

Atribut 'color_primary' di dalam file config.php akan mengatur warna utama untuk semua tombol dan latar belakang header.

Anda memiliki 4 template bernama:

- footer.php
- header.php
- navbar.php
- sidebar.php

terletak di dalam folder /template/. Edit kontennya atau hapus jika Anda tidak memerlukannya.

## Kebijakan Privasi dan Syarat & Ketentuan (Halaman)

Kebijakan privasi dapat ditulis di dalam file `/template/_privacy.html` Mengganti nama file `_privacy.html` menjadi privacy.html akan mengaktifkan tautan "Privasi" di dalam footer. Teks privasi akan terbuka di dalam jendela modal.

Syarat dan ketentuan dapat ditulis di dalam file `/template/_terms.html` Mengganti nama file `_terms.html` menjadi `terms.html` akan mengaktifkan tautan "Syarat dan ketentuan" di dalam footer. teks privasi akan terbuka di dalam jendela modal.

Istilah 'privasi' dan 'terms_and_conditions' dapat ditemukan di dalam file /translations/

## Halaman Custom

Salin atau ganti nama file `/template/example.html` dan tempatkan konten khusus Anda di sana. Nama file akan dimuat dengan string kueri relatif di akhir url Anda: `?p=example` misalnya: `https://ardeanstudio.co/qr/?p=example`

jika Anda memiliki file bernama custom.html, urlnya adalah `http://...../?p=custom`

## Kelola Terjemahan

Jika Anda ingin menambahkan bahasa khusus, duplikat dan ganti nama file `lang/en.php` menggunakan 2 huruf kode ISO yang diinginkan dan perbarui juga nilai 'lang' => 'en' di dalam file konfigurasi utama Anda config.php

Menu bahasa ditampilkan dengan fungsi berikut:

```
<?php echo qrcdr()->langMenu(); ?>
```

Anda dapat memilih apakah menampilkannya sebagai menu tarik-turun (default) atau sebagai daftar sederhana, dan menetapkan kelas khusus:

```
<?php echo qrcdr()->langMenu('daftar', 'kelas khusus'); ?>
```

Variabel pertama dapat berupa 'menu' atau 'daftar', variabel kedua adalah kelas khusus opsional yang ditetapkan ke menu bahasa (default: 'langmenu')

Semua istilah yang dapat diterjemahkan, termasuk judul halaman, deskripsi, dan kata kunci meta ada di dalam file .php masing-masing di folder /translations/.

default: `/translations/en.php`

## Embed

Anda dapat menyematkan generator yang dihosting sendiri di mana saja menggunakan iframe:

```
<iframe width="100%" src="http://www.example.com/qr/" ></iframe>
```

## Catatan

Gaya media cetak, Tipografi, Formulir dan Tabel didasarkan pada Bootstrap v4

Ikon didasarkan pada Font Awesome 4.7