# Kimin Tkinter Framework

Kimin Tkinter Framework adalah sebuah framework inovatif yang dirancang khusus untuk mempermudah pengembangan aplikasi GUI Python berbasis Tkinter. Dengan fokus pada kemudahan penggunaan, framework ini memungkinkan pengembang untuk membuat antarmuka pengguna yang menarik dengan cepat dan efisien.

## Fitur
- Konfigurasi Layout Berbasis JSON
- Konfigurasi Trigger / Event Handler Berbasis JSON
- Generate Main App
- Generate Default Trigger / Event Handler
- Otomatis Install Packages

## Version
- [v1](https://www.mediafire.com/file/14kh9qko3dr4vmy/Kimin+Tkinter+Framework+v1.exe/file)

## List Dokumen

- [Introduction](#Introduction)
- [Fitur](#Fitur)
- [Version](#Version)
- [Usage](#Usage)
- [Componen Properties](#Componen)
- [Config Layout](#Config-Layout)
- [Trigger / Event Handler](#Event-Handler)

## Introduction

#### Overview
<p style="display: flex; justify-content: space-between;">
    <img style="width: 48%;" src="foto/awal.PNG" />
    <img style="width: 48%;" src="foto/generate.PNG" />
    <img style="width: 48%;" src="foto/config.PNG" />
</p>

#### Deskripsi
<p style="display: flex; justify-content: space-between;">
    <img style="width: 48%;" src="foto/intro.png" />
</p>

Terdapat 3 aspek utama dalam Framework ini, Yang meliputi :

- [Working Area](#Working-Area)
- [Componen Area](#Componen-Area)
- [Generate Button](#Generate-Button)

###### Working Area
Working Area ditandai dengan nomor 1 pada gambar. Disinilah nanti layout yang akan digenerate pada aplikasi GUI dan tempat setiap komponen akan di tempatkan.

###### Componen Area
Componen Area ditandai dengan nomor 2 pada gambar. Disini componen yang akan ditempatkan pada working area ketika componen di klik

###### Generate Button
Digunakan untuk mengenerate Aplikasi gui ketika di klik

## Usage
``` bash
    "Kimin Tkinter Framework v1.exe" -p nama_project
```

Note : nama_project adalah nama project / aplikasi yang akan dibuat

## Config Layout
Lokasi File Config berada pada "folder project/gui_config.min"
| Parameter | Type     | Description                | Example |
| :-------- | :------- | :------------------------- | :------ |
| `judul` | `string` | Judul Aplikasi | Aplikasi 1 |
| `theme` | `enum("system", "dark", "light")` | Tema / Appearance Aplikasi | dark |
| `resolusi` | `string` | Ukuran Resolusi Aplikasi ditetapkan data json x dan y dalam satuan px | {x:"400", y:"400"} |

## Event Handler
Semua data Componen tersipan pada kimin.data[nama_componen] yang berbentuk list. Pada Class ini defaultnya adalah 1 function digunakan untuk menghadle banyak componen dengan jenis yang sama. Secara default lokasi Event Handler berada pada "folder_project/Event Trigger/trigger.py".

Misalnya untuk mengganti text pada button 1 menjadi "Ubah Button 1"
```python
    kimin.data['button'][0].configure(text="Ubah Button 1")
```

Misalnya untuk menggambil value pada entry box 1
```python
    print(kimin.data['entry'][0].get())
```

## Componen
Untuk menghapus Componen pada Working Area klik kanan pada componen dan untuk mengedit properties pada componen klik kiri 2x pada componen. Untuk mengatur ukuran layout dari aplikasi, cukup resize framework saja. Ukuran layout aplikasi akan otomatis diambil dari ukuran Working Area Ketika diresize.

Parameter Pada Properties tiap-tiap componen.
###### Button

| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `width` | `integer` | Lebar Ukuran Dalam px | 20 |
| `height` | `integer` | Tinggi Ukuran Dalam px | 20 |
| `Corner Radius` | `integer` | Ukuran Radius Sudut Dalam px | 15 |
| `Border width` | `integer` | Ukuran Tepian Button Dalam px | 5 |
| `Border Spacing` | `integer` | jarak antara teks dan gambar dan tepi button Dalam px, nilai default adalah 2 | 3 |
| `Fg color` | `string` | warna latar depan, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `Hover color` | `string` | warna hover, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `Border color` | `string` | warna tepian, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `Text color` | `string` | warna teks, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `text color disabled` | `string` | warna teks ketika dinonaktifkan, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `Text` | `string` | teks | Login |
| `Hover` | `boolean` | aktifkan/nonaktifkan efek hover: true, false | true |


###### Checkbox
| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `width` | `integer` | Lebar Ukuran Dalam px | 20 |
| `height` | `integer` | Tinggi Ukuran Dalam px | 20 |
| `Checkbox width` | `integer` | lebar Ukuran checkbox Dalam px | 20 |
| `Checkbox height` | `integer` | lebar Ukuran checkbox Dalam px | 20 |
| `Corner Radius` | `integer` | Ukuran Radius Sudut Dalam px | 15 |
| `Border width` | `integer` | Ukuran Tepian Button Dalam px | 5 |
| `Fg color` | `string` | warna latar depan, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `Border color` | `string` | warna tepian, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `Hover color` | `string` | warna hover, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `Text color` | `string` | warna teks, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `text color disabled` | `string` | warna teks ketika dinonaktifkan, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `Text` | `string` | teks | Login |
| `Hover` | `boolean` | aktifkan/nonaktifkan efek hover: true, false | true |



###### OptionMenu
| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `width` | `integer` | Lebar Ukuran Dalam px | 20 |
| `height` | `integer` | Tinggi Ukuran Dalam px | 20 |
| `Corner Radius` | `integer` | Ukuran Radius Sudut Dalam px | 15 |
| `Border width` | `integer` | Ukuran Tepian Button Dalam px | 5 |
| `Fg color` | `string` | warna latar depan, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Border color` | `string` | warna tepian, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `button color` | `string` | warna bagian kanan button, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `button hover color` | `string` | warna hover button, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `Text color` | `string` | warna teks, contohnya: (light_color, dark color) atau warna tunggal atau transparan | #000000 |
| `text color disabled` | `string` | warna teks ketika dinonaktifkan, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `Text` | `string` | teks | Login |
| `Hover` | `boolean` | aktifkan/nonaktifkan efek hover: true, false | true |
| `values` | `string` | daftar string dengan nilai yang muncul di menu dropdown | Laki-Laki,Perempuan |


###### Entry
| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `width` | `integer` | Lebar Ukuran Dalam px | 20 |
| `height` | `integer` | Tinggi Ukuran Dalam px | 20 |
| `Corner Radius` | `integer` | Ukuran Radius Sudut Dalam px | 15 |
| `Fg color` | `string` | warna latar depan, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Text color` | `string` | warna teks, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Placeholder Text color` | `string` | warna teks placeholder, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `Placeholder Text ` | `string` | petunjuk pada input entri (menghilang saat dipilih), defaultnya adalah Tidak Ada, tidak berfungsi jika dikombinasikan dengan variabel teks | masukkan username |


###### Label
| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `width` | `integer` | Lebar Ukuran Dalam px | 20 |
| `Text` | `string` | teks | Login |
| `height` | `integer` | Tinggi Ukuran Dalam px | 20 |
| `Corner Radius` | `integer` | Ukuran Radius Sudut Dalam px | 15 |
| `Fg color` | `string` | warna latar depan, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Text color` | `string` | warna teks, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Anchor` | `string` | mengontrol di mana teks diposisikan jika widget memiliki lebih banyak ruang daripada yang dibutuhkan teks, defaultnya adalah "tengah" | center |
| `Compound` | `integer` | mengontrol posisi gambar  terhadap teks, defaultnya adalah "center", lainnya adalah:" top "," bottom "," left "," right " | top |
| `Padx` | `integer` | jarak spasi yang ditambahkan di kiri dan kanan teks, defaultnya adalah 1 | 20 |
| `Pady` | `integer` | jarak spasi yang ditambahkan di atas dan bawah teks, defaultnya adalah 1 | 20 |


###### Progressbar
| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `width` | `integer` | Lebar Ukuran Dalam px | 20 |
| `height` | `integer` | Tinggi Ukuran Dalam px | 20 |
| `Corner Radius` | `integer` | Ukuran Radius Sudut Dalam px | 15 |
| `Border width` | `integer` | Ukuran Tepian Button Dalam px | 5 |
| `Fg color` | `string` | warna latar depan, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Border color` | `string` | warna tepian, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Progress color` | `string` | warna progress, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |


###### Radiobutton
| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `width` | `integer` | Lebar Ukuran Dalam px | 20 |
| `height` | `integer` | Tinggi Ukuran Dalam px | 20 |
| `Radiobutton width` | `integer` | Lebar Ukuran Radiobutton Dalam px | 20 |
| `Radiobutton height` | `integer` | Tinggi Ukuran Radiobutton Dalam px | 20 |
| `Corner Radius` | `integer` | Ukuran Radius Sudut Dalam px | 15 |
| `Border width unchecked` | `integer` | lebar batas dalam ketika tidak dicentang Dalam px | 5 |
| `Border width checked` | `integer` | lebar batas dalam ketika dicentang Dalam px | 5 |
| `Fg color` | `string` | warna latar depan, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Border color` | `string` | warna tepian, contohnya: (light_color, dark color) atau warna tunggal  | #000000 |
| `Hover color` | `string` | warna hover, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `Text color` | `string` | warna teks, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `text color disabled` | `string` | warna teks ketika dinonaktifkan, contohnya: (light_color, dark color) atau warna tunggal | #000000 |
| `Text` | `string` | teks | Login |
| `Hover` | `boolean` | aktifkan/nonaktifkan efek hover: true, false | true |
| `values` | `string` | daftar string dengan nilai yang muncul di menu dropdown | Laki-Laki,Perempuan |

Parameter layout yang terdapat pada tiap-tiap componen di "gui_config.min"
###### Layout
| Parameter | Input Type| Deskripsi                | Example |
| :-------- | :-------- | :----------------------- | :------ |
| `type` | `string` | tipe layout | grid |
| `row` | `integer` | Baris | 2 |
| `column` | `integer` | kolom | 2 |
| `sticky` | `string` | Jika sel lebih besar dari widget, opsi sticky akan menentukan sisi mana widget harus ditempel dan cara mendistribusikan ruang ekstra di dalam sel yang tidak digunakan oleh widget pada ukuran aslinya | ew |
