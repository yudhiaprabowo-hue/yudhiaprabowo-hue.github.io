---
layout: post
title: Satu kali input, seluruh persyaratan tersalurkan
description: Tangerang One Permit, prototipe penapisan persyaratan dasar berusaha dan menyalurkannya ke OPD teknis secara berurutan.
image: /assets/gambar/beranda.jpg
tags: [belajar, teknologi, perizinan]
---

Semua dimulai pada 30 September 2024, judul awalnya adalah **Grand Design Perizinan v2** Sejak awal Oktober 2024, berawal dari akan diupdatenya sistem perizinan online kota tangerang yang melakukan update dari versi 1 menjadi versi 2, terpikir apakah ada perubahan signifikan yang dapat dilakukan? tidak hanya sebatas perubahan minor, namun perubahan yang mnmberikan dampak besar dan menjadi **Game Changer** dalam dunia perizinan di Indonesia. Ide ini sudah disampaikan ke beberapa orang, semua berawal dari halaman Power Point berikut, yang merupakan awal dari prototipe penapisan persyaratan dasar berusaha.

<!--lanjut-->
---
<figure>
 <img width="1372" height="765" alt="image" src="https://github.com/user-attachments/assets/93ba56c1-2818-4a0c-8b62-349972c80178" />
 <figcaption> Ide awal prototipe penapisan persyaratan dasar berusaha. </figcaption>
</figure>

<!--lanjut-->
---
Keterbatasan akan kemampuan teknis dalam mengeksekusi sebuah ide yang berkaitan dengan teknologi informasi, membuat ide itu hanya sampai sebatas ide yang coba dipasarkan ke pihak internal. 2026 menjadi awal penulis mengenal apa itu **Artificial Inteligence** , dimulai dari penggunaan **ChatGPT**, diakhiri dengan menemukan **Claude**. Penulis merasa bahwa **Claude** dapat membuat penulis melewati batas kemampuan teknis dalam penerapan prototipe penapisan persyaratan dasar yang idenya sudah terkubur sejak dia lahir di Oktober 2024. Dua tahun kemudian di Oktober 2026, sebuah prototipe website penapisan perizinan yang penulis beri nama Tangerang One Permit (TOP) lahir. Proyek ini masih berupa prototipe yang berjalan di komputer penulis sendiri dan belum menjadi layanan publik. Meski begitu, proses membangunnya sudah memberi banyak pelajaran yang sayang jika tidak dicatat.

<figure>
  <img width="1280" height="800" alt="beranda" src="https://github.com/user-attachments/assets/6020458a-d166-42cf-90ef-8b609bd07246" />
  <figcaption>Halaman beranda prototipe Tangerang One Permit.</figcaption>
</figure>

## Berawal dari satu pertanyaan

Pertanyaan yang paling sering muncul dari pelaku usaha sebenarnya sederhana: "Saya harus mengurus apa dulu?" Jawabannya ternyata tidak sesederhana pertanyaannya. Sebelum sampai ke Persetujuan Bangunan Gedung (PBG), ada beberapa persyaratan dasar yang harus dipenuhi, dan kebutuhannya berbeda untuk setiap rencana usaha.

Gagasan yang ingin saya uji dirangkum dalam satu kalimat di halaman depan website ini: satu kali input, seluruh persyaratan tersalurkan. Pemohon cukup mengisi data pemohon, rencana usaha, serta data lahan dan bangunan satu kali. Sistem kemudian menapis persyaratan apa saja yang wajib ditempuh dan menyalurkannya ke dinas teknis yang berwenang.

## Menyusun alurnya

Bagian tersulit justru bukan menulis kode, melainkan menyepakati alurnya sendiri. Setelah beberapa kali mengubah rancangan, alur yang saya pakai sekarang terdiri atas empat langkah.

<figure>
 <img width="1280" height="580" alt="alur-empat-langkah" src="https://github.com/user-attachments/assets/6b5bb36c-7e8c-4918-9d3c-a49e4c49431f" />
  <figcaption>Empat langkah yang diproses berurutan setelah permohonan diverifikasi.</figcaption>
</figure>

1. **Keterangan Rencana Kota (KRK)** sebagai pintu masuk. Awalnya tahap ini saya namai "Tata Ruang", tetapi nama itu terlalu luas dan sering disalahpahami.
2. **Persetujuan Lingkungan, Peil Banjir, dan Andalalin** diproses bersamaan oleh dinas masing-masing.
3. **Pengesahan Rencana Tapak**, atau jalur "Tidak Perlu PRT". Rencana tapak dipersyaratkan bagi pengembangan perumahan dan pengajuan kawasan. Bangunan tunggal langsung menuju PBG.
4. **PBG** sebagai langkah terakhir.

Izin yang tidak dipersyaratkan dilewati otomatis. Langkah berikutnya baru terbuka setelah seluruh izin wajib pada langkah sebelumnya selesai. Di setiap dinas, izin melalui tahapan yang sama: konsultasi, berita acara, penetapan, persetujuan, tanda tangan SK, dan cetak SK.

## Penapisan yang menyertakan dasar hukumnya

Prinsip yang saya pegang sejak awal: setiap ambang batas harus punya dasar hukum, dan dasar hukum itu harus terlihat oleh pengguna. Karena itu, hasil penapisan tidak hanya menyebut izin apa yang wajib, tetapi juga alasannya dan pasal yang menjadi rujukannya. Hasilnya diperbarui langsung saat formulir diisi.

<figure>
 <img width="1200" height="880" alt="formulir-dan-hasil-penapisan" src="https://github.com/user-attachments/assets/f9d51062-69a6-4079-a5e3-075aeb0cfdf8" />
  <figcaption>Contoh simulasi gudang 1.800 m² di atas lahan 2.500 m². Panel kanan langsung menunjukkan persyaratan yang wajib beserta dasar hukumnya. Data yang dipakai adalah data contoh.</figcaption>
</figure>

Rujukan utamanya adalah PP Nomor 28 Tahun 2025, ditambah peraturan teknis seperti Permen LHK Nomor 4 Tahun 2021 untuk persetujuan lingkungan, Permenhub Nomor 17 Tahun 2021 untuk Andalalin, dan Permen PUPR Nomor 11/PRT/M/2014 untuk peil banjir. Ketentuan yang belum ada dasar hukumnya tidak saya karang. Ketentuan seperti itu ditandai sebagai ketentuan daerah dan dijadikan parameter yang dapat diatur administrator.

## Hasil penapisan langsung

Hasil penapisan juga bisa langsung diterbitkan dalam bentuk PDF, hasil sesuai dengan data yang diinput oleh pemohon yang akan diproses penapisan berdasarkan aturan yang ada. Pemohon bisa langsung tau persyaratan apa saja yang perlu dilalui untuk bisa sampai pada perizinan Persetujuan Bangunan Gedung.

<figure>
 <img width="561" height="828" alt="PENAPISAN 1" src="https://github.com/user-attachments/assets/046e4ff5-98f1-4539-9f03-8b20cf6dec5a" />
 <img width="562" height="814" alt="PENAPISAN 2" src="https://github.com/user-attachments/assets/dbbaa567-991f-48f9-9486-23eb7dba54bd" />
 <img width="569" height="825" alt="PENAPISAN 3" src="https://github.com/user-attachments/assets/a59503a2-e500-4172-869a-30b191546424" />
</figure>

Contoh Hasil penapisan berupa file PDF.


## Tanya Kami

Saya juga menambahkan asisten percakapan bernama "Tanya Kami". Pengguna cukup menceritakan rencananya dengan bahasa sehari-hari. Asisten akan menanyakan data yang masih kurang, lalu menjalankan penapisan yang sama dengan formulir.

<figure class="sempit">
  <img src="{{ '/assets/gambar/chatbot-tanya-kami.jpg' | relative_url }}" alt="Jendela percakapan Tanya Kami yang menjawab izin apa saja yang diperlukan untuk membangun gudang">
  <figcaption>Tanya Kami menjawab kebutuhan izin untuk rencana gudang di Kecamatan Jatiuwung.</figcaption>
</figure>

## Dari sisi petugas

Di belakang layar, ada panel petugas untuk setiap dinas. DPMPTSP memverifikasi permohonan, lalu setiap dinas hanya melihat dan memproses izin yang menjadi kewenangannya. Dasbor menampilkan rekap permohonan dan beban kerja setiap subsistem.

<figure>
  <img src="{{ '/assets/gambar/panel-petugas.jpg' | relative_url }}" alt="Dasbor panel petugas berisi rekap permohonan dan beban setiap subsistem">
  <figcaption>Dasbor panel petugas dengan data contoh.</figcaption>
</figure>

## Sisi teknis

Website ini saya bangun dengan Node.js dan basis data SQLite, menggunakan HTML dan JavaScript murni tanpa framework. Pilihannya sengaja sederhana: ringan, mudah dijalankan di komputer sendiri, dan cukup untuk menguji gagasan. Dari proyek yang sama juga lahir aplikasi kecil "Cek Zonasi" untuk ponsel, yang memeriksa kesesuaian zona dari titik koordinat.

## Yang saya pelajari

- **Regulasi perlu diterjemahkan, bukan disalin.** Pasal yang jelas bagi pembaca hukum belum tentu jelas bagi sistem. Setiap ketentuan harus diubah menjadi pertanyaan yang bisa dijawab dengan data.
- **Nama itu penting.** Mengganti satu istilah, seperti "Tata Ruang" menjadi "Keterangan Rencana Kota", bisa mengubah cara orang memahami seluruh alur.
- **Tunjukkan dasarnya.** Hasil penapisan lebih mudah dipercaya jika setiap kesimpulan disertai rujukan pasalnya.
- **Mulai dari yang kecil.** Prototipe sederhana yang benar-benar berjalan lebih berguna daripada rancangan besar yang hanya ada di dokumen.

## Langkah berikutnya

Masih banyak yang ingin saya rapikan, mulai dari menguji lebih banyak skenario hingga memperkuat keamanannya. Sebelum dapat dipasang di server yang diakses publik, aplikasi ini masih memerlukan HTTPS, pencatatan audit, dan pengujian keamanan. Saya akan mencatat perkembangannya di jurnal ini.

*Catatan: Tangerang One Permit adalah proyek pribadi untuk belajar dan bereksperimen, bukan layanan resmi pemerintah. Seluruh tangkapan layar menggunakan data contoh. Untuk mengurus perizinan, silakan gunakan kanal layanan resmi.*
