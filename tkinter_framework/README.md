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
- [Componen Properties](#)
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

