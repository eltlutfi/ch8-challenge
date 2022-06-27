# Binar Academy Bootcamp - FSW - Chapter 8 - Challenge

Ini adalah repository RESTful API yang menjadi basis untuk teman-teman berkreasi di challenge chapter 8. Ikuti petunjuk di bawah dengan seksama untuk memastikan teman-teman dapat menjalankan RESTful API.

## Prasyarat

Sebelum memulai menyentuh repository, pastikan komputer teman-teman memenuhi prasyarat berikut:

- sudah install Node.js & NPM
- sudah install PostgreSQL
- sudah install git

## Project setup

1. Fork repository ini. Ada tombol 'fork' di kanan atas. Setelah fork nanti akan muncul repository yang sama persis di akun teman-teman.
1. Clone repository teman-teman yang sudah di fork

```sh
git clone https://github.com/{username_kalian}/ch8-challenge.github
```

3. Pindah ke folder repository yang udah di clone dengan command `cd ch8-challenge`.
1. Kode Backend atau Server terdapat pada directory `server`. Sehingga untuk melakukan setup, pindah ke folder `server` dengan command `cd server`.
1. Install dependencies pada server dengan command `npm install`.
1. Untuk konfigurasi database, terdapat dua cara. Pertama, ubah langsung `/config/config.js`. Kedua (disarankan), menggunakan `env`. Untuk menggunakan `env`, cukup copy file `.env.example` dan paste menjadi `.env` atau bisa lakukan command `cp .env.example .env` lalu lakukan konfigurasi pada file `.env`.
1. Setelah konfigurasi database. Jalankan `npx sequelize db:create`.
1. Lanjutkan dengan menjalankan migrasi `npx sequelize db:migrate`
1. Kamu juga bisa jalankan file seed yang sudah dibuat dengan cara `npx sequelize db:seed:all`

### Run

Untuk menjalankan aplikasi RESTful API, pastikan sudah berada pada directory `server`. Untuk menjalankan dalam mode development, jalankan command berikut:

```sh
npm run dev
```

Untuk menjalankan dalam mode biasa, jalankan command berikut:

```sh
npm run start
```

## Tasks

Jika teman-teman sudah berhasil menjalankan aplikasi RESTful API dari repository ini, teman-teman perlu melakukan dua hal:

1. Membuat dokumentasi API dengan Swagger
   - [ ] Baca code repository RESTful API ini baik-baik
   - [ ] Buat dokumentasi untuk semua endpoint yang terdaftar di router
   - [ ] Dokumentasi melingkupi :
     - [ ] HTTP method
     - [ ] URL
     - [ ] URL parameter (jika ada)
     - [ ] Query parameter (jika ada)
     - [ ] Request body (jika ada)
     - [ ] format response
   - [ ] Pasang dokumentasi Swagger dalam satu routing
2. Membuat client-side application dengan React.js
   - [ ] Buat folder baru, misalkan /client, kemudian buat project baru dalam folder tersebut dengan `$ npm init -y` atau `$ npx create-react-app client`
   - [ ] Buat tampilan/UI untuk fitur berikut :
     - [ ] Form untuk membuat player baru, dengan tombol Submit
     - [ ] Form untuk mengedit player, dengan tombol Submit
     - [ ] Form untuk pencarian player berdasarkan 4 kriteria pencarian : username, email, experience, dan lvl. jangan lupa juga tombol submit.
   - [ ] Kita belum belajar mengintegrasikan back-end dan front-end. Jadi untuk challenge ini, ketika di klik tombol submit tampilkan semua input sebagai satu elemen HTML baru
     - [ ] Untuk form membuat atau edit player, tampilkan info username, email, dll setelah di klik submit.
     - [ ] Untuk form mencari player, tampilkan ulang input kriteria username, email, experience, dan lvl.
   - [ ] Jalankan sebagai aplikasi client-side (npm run start di folder client (buat run react app))

## Caveats / Batasan

- Tugas nomor 1 dan 2 dibuat dalam repository yang sama dengan repository RESTful API. Dengan kata lain, teman-teman bertugas mengembangkan repository RESTful API ini menjadi repository full-stack (RESTful API + client-side + documentation)
- Code existing yang ada dalam folder /app tidak boleh diubah/dihapus, kecuali bagian config db. Yang diperbolehkan hanya penambahan line untuk memenuhi challenge.
- Jika teman-teman menemukan error/bug dalam code, silakan buat issue di repository ini atau sampaikan ke tim Binar Academy
- Pastikan folder node_modules masuk dalam .gitignore, baik untuk RESTful API maupun client-side.
- Nantinya, aplikasi RESTful API dan client-side akan berjalan sebagai 2 aplikasi berbeda. Pastikan keduanya bisa berjalan berbarengan tanpa ada issue.

## Petunjuk Submission

- Challenge di submit paling lambat hari Senin di minggu ketiga chapter 8, pukul 23:59 WIB.
- metode submission: kirim email ke mentor dan bagian akademik Binar, berisi link repository teman-teman (yang di fork) di GitHub.
