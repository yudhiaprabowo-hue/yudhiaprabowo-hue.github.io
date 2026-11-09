---
layout: post
title: Satu kali input, seluruh persyaratan tersalurkan
description: Cerita di balik Tangerang One Permit, prototipe penapisan persyaratan dasar berusaha dan menyalurkannya ke OPD teknis secara berurutan.
image: /assets/gambar/beranda.jpg
tags: [belajar, teknologi, perizinan]
---

Semua dimulai pada 30 September 2024, judul awalnya adalah **Grand Design Perizinan v2** Sejak awal Oktober, sebagian besar waktu luang saya habis untuk satu proyek: 

<!--lanjut-->
<figure>
<img width="1372" height="765" alt="image" src="https://github.com/user-attachments/assets/93ba56c1-2818-4a0c-8b62-349972c80178" />
 <figcaption>Ide awal prototipe penapisan persyaratan dasar berusaha.</figcaption>
</figure>

<!--lanjut-->

Sebuah website penapisan perizinan yang saya beri nama Tangerang One Permit (TOP). Proyek ini masih berupa prototipe yang berjalan di komputer saya sendiri dan belum menjadi layanan publik. Meski begitu, proses membangunnya sudah memberi banyak pelajaran yang sayang jika tidak dicatat.

<figure>
  <img src="{{ '/assets/gambar/beranda.jpg' | relative_url }}" alt="Halaman beranda Tangerang One Permit dengan judul Satu kali input, seluruh persyaratan tersalurkan">
  <figcaption>Halaman beranda prototipe Tangerang One Permit.</figcaption>
</figure>

## Berawal dari satu pertanyaan

Pertanyaan yang paling sering muncul dari pelaku usaha sebenarnya sederhana: "Saya harus mengurus apa dulu?" Jawabannya ternyata tidak sesederhana pertanyaannya. Sebelum sampai ke Persetujuan Bangunan Gedung (PBG), ada beberapa persyaratan dasar yang harus dipenuhi, dan kebutuhannya berbeda untuk setiap rencana usaha.

Gagasan yang ingin saya uji dirangkum dalam satu kalimat di halaman depan website ini: satu kali input, seluruh persyaratan tersalurkan. Pemohon cukup mengisi data pemohon, rencana usaha, serta data lahan dan bangunan satu kali. Sistem kemudian menapis persyaratan apa saja yang wajib ditempuh dan menyalurkannya ke dinas teknis yang berwenang.

## Menyusun alurnya

Bagian tersulit justru bukan menulis kode, melainkan menyepakati alurnya sendiri. Setelah beberapa kali mengubah rancangan, alur yang saya pakai sekarang terdiri atas empat langkah.

<figure>
  <img src="{{ '/assets/gambar/alur-empat-langkah.jpg' | relative_url }}" alt="Diagram empat langkah: Keterangan Rencana Kota, lalu Persetujuan Lingkungan, Peil Banjir, dan Andalalin secara paralel, lalu Pengesahan Rencana Tapak atau Tidak Perlu PRT, lalu PBG">
  <figcaption>Empat langkah yang diproses berurutan setelah permohonan diverifikasi.</figcaption>
</figure>

1. **Keterangan Rencana Kota (KRK)** sebagai pintu masuk. Awalnya tahap ini saya namai "Tata Ruang", tetapi nama itu terlalu luas dan sering disalahpahami.
2. **Persetujuan Lingkungan, Peil Banjir, dan Andalalin** diproses bersamaan oleh dinas masing-masing.
3. **Pengesahan Rencana Tapak**, atau jalur "Tidak Perlu PRT". Rencana tapak dipersyaratkan bagi pengembangan perumahan dan pengajuan kawasan. Bangunan tunggal nonperumahan langsung menuju PBG.
4. **PBG** sebagai langkah terakhir.

Izin yang tidak dipersyaratkan dilewati otomatis. Langkah berikutnya baru terbuka setelah seluruh izin wajib pada langkah sebelumnya selesai. Di setiap dinas, izin melalui tahapan yang sama: konsultasi, berita acara, penetapan, persetujuan, tanda tangan SK, dan cetak SK.

## Penapisan yang menyertakan dasar hukumnya

Prinsip yang saya pegang sejak awal: setiap ambang batas harus punya dasar hukum, dan dasar hukum itu harus terlihat oleh pengguna. Karena itu, hasil penapisan tidak hanya menyebut izin apa yang wajib, tetapi juga alasannya dan pasal yang menjadi rujukannya. Hasilnya diperbarui langsung saat formulir diisi.

<figure>
  <img src="{{ '/assets/gambar/formulir-dan-hasil-penapisan.jpg' | relative_url }}" alt="Formulir permohonan di sebelah kiri dan panel Hasil Penapisan Otomatis di sebelah kanan">
  <figcaption>Contoh simulasi gudang 1.800 m² di atas lahan 2.500 m². Panel kanan langsung menunjukkan persyaratan yang wajib beserta dasar hukumnya. Data yang dipakai adalah data contoh.</figcaption>
</figure>

Rujukan utamanya adalah PP Nomor 28 Tahun 2025, ditambah peraturan teknis seperti Permen LHK Nomor 4 Tahun 2021 untuk persetujuan lingkungan, Permenhub Nomor 17 Tahun 2021 untuk Andalalin, dan Permen PUPR Nomor 11/PRT/M/2014 untuk peil banjir. Ketentuan yang belum ada dasar hukumnya tidak saya karang. Ketentuan seperti itu ditandai sebagai ketentuan daerah dan dijadikan parameter yang dapat diatur administrator.

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
