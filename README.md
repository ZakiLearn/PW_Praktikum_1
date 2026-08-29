Panduan Memodifikasi Repository GitHub

README ini menjelaskan cara memodifikasi repository GitHub menggunakan Git. Dengan cara ini, kamu bisa mengambil repository ke komputer, mengubah file, lalu mengirim perubahan tersebut kembali ke GitHub.

1. Persiapan

Pastikan Git sudah terpasang di komputer.

Cek dengan perintah:

git --version

Kalau Git sudah terpasang, akan muncul versi Git yang digunakan.

Selain itu, pastikan kamu sudah memiliki akses ke repository GitHub yang ingin dimodifikasi.

2. Clone Repository

Pertama, clone repository ke komputer:

git clone https://github.com/USERNAME/NAMA-REPOSITORY.git

Masuk ke folder repository:

cd NAMA-REPOSITORY

3. Buat Branch Baru

Sebaiknya buat branch sendiri sebelum melakukan perubahan:

git checkout -b nama-branch

Contohnya:

git checkout -b update-readme

Dengan menggunakan branch, perubahan yang kamu buat tidak langsung mengubah branch utama.

4. Modifikasi File

Sekarang kamu bisa membuka repository menggunakan editor seperti VS Code dan melakukan perubahan yang diperlukan.

Setelah selesai, cek perubahan dengan:

git status

Untuk melihat detail perubahan:

git diff

5. Commit Perubahan

Tambahkan file yang sudah diubah:

git add .

Kemudian buat commit:

git commit -m "Menjelaskan perubahan yang dilakukan"

Contohnya:

git commit -m "Update dokumentasi README"

Sebaiknya gunakan pesan commit yang singkat dan menjelaskan perubahan yang dilakukan.

6. Push ke GitHub

Kirim branch yang sudah dibuat ke GitHub:

git push -u origin nama-branch

Contohnya:

git push -u origin update-readme

Setelah berhasil, branch tersebut akan muncul di repository GitHub.

7. Buat Pull Request

Setelah melakukan push, buka repository di GitHub.

Kemudian buat Pull Request dari branch yang kamu buat menuju branch utama, biasanya main.

Jelaskan secara singkat perubahan yang kamu lakukan agar lebih mudah diperiksa sebelum digabungkan.

Alur Singkat

Secara umum, prosesnya seperti ini:

GitHub Repository
|
v
git clone
|
v
Buat branch
|
v
Modifikasi file
|
v
git add
|
v
git commit
|
v
git push
|
v
Pull Request
|
v
Merge

Perintah yang Sering Digunakan

# Mengambil repository

git clone <URL-REPOSITORY>

# Masuk ke repository

cd <NAMA-REPOSITORY>

# Melihat branch

git branch

# Membuat branch baru

git checkout -b <NAMA-BRANCH>

# Melihat perubahan

git status
git diff

# Menambahkan perubahan

git add .

# Membuat commit

git commit -m "Pesan commit"

# Mengirim branch ke GitHub

git push -u origin <NAMA-BRANCH>

# Mengambil perubahan terbaru dari repository

git pull

Catatan

Sebelum mulai mengerjakan perubahan baru, sebaiknya pastikan repository sudah dalam kondisi terbaru:

git checkout main
git pull origin main

Setelah itu, buat branch baru untuk pekerjaan yang akan dilakukan.

Jangan langsung melakukan perubahan pada main jika repository digunakan bersama. Gunakan branch dan Pull Request agar perubahan bisa diperiksa terlebih dahulu.

Dengan alur ini, setiap orang bisa mengerjakan perubahan masing-masing tanpa mengganggu pekerjaan anggota lain.
