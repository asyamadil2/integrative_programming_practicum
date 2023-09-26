![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/bf66cfe1-4188-446c-8851-e0052b063989)## Instalasi NodeJS

1. Buka halaman
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/5f394156-6943-4600-a9f9-2c5d2523763c)
2. Download dan jalankan node setup
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/f202535c-869c-4461-ad93-bbd5f1e1cf99)
3. Setelah instalasi selesai jalankan command "node -v" untuk memeriksa apakah NodeJS sudah terinstall
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/ae3def46-51c5-4ccb-ac37-614bd6071fbf)
  
## Inisiasi project Express dan pemasangan package

1. Lakukan pembuatan folder dengan nama express-mongodb dan masuk ke dalam folder tersebut lalu buka melalui text editor masing-masing
2. Lakukan npm init untuk mengenerate file package.json dengan menggunakan command "npm init -y"
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/5859d284-20d0-4b5e-8270-78c4ec515b04)
3. Lakukan instalasi express, mongoose, dan dotenv dengan menggunakan command "npm i express mongoose dotenv"
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/b05148ae-3687-4df8-9473-011304bc856e)

## Koneksi Express ke MongoDB

1. Buatlah file "index.js" pada root folder dan masukkan kode di bawah ini
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/67faaf22-db6d-4d88-99e2-becb9da18157)
   Setelah itu coba jalankan aplikasi dengan command "node index.js"
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/03863ddf-1ac3-4252-be7e-02f760fa7bc6)
2. Lakukan pembuatan file ".env" dan masukkan baris berikut
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a74949e1-b87e-4425-a6b7-b30816a4b445)
   Setelah itu ubahlah kode pada listening port menjadi berikut dan coba jalankan aplikasi kembali
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/05b7b00f-e611-44c0-be96-5ecfb5ebfdde)
3. Copy connection string yang terdapat pada compas atau atlas dan paste kan pada ".env" seperti berikut
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/12a02bb9-0e58-484a-bdfb-c4f5f7806bf7)
4. Tambahkan baris kode berikut pada file "index.js"
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a8c7426d-0866-47a2-9488-b4de27980588)
   Setelah itu coba jalankan aplikasi kembali
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a2abc49d-6ea3-4bd6-8990-870590f6fab6)

## Pembuatan Routing

1. Lakukan pembuatan direktori "routes" di tingkat yang sama dengan index.js

   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/38fed318-521f-45ad-b4b0-eaf949b3c7d0)
2. Buatlah file book.route.js di dalamnya

   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/392d6fc1-4625-46a0-b384-ae63116bb076)
3. Tambahkan baris kode berikut untuk fungsi getAllBooks
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a089596f-1392-4c55-bac6-3249d8b22c3c)

4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/38240f39-3026-4c32-b17e-80292cfc947b)
5. Lakukan import book.route.js pada file index.js dan tambahkan baris kode berikut
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/58e98aba-1243-4ace-8648-ae527516f722)
6. Uji salah satu endpoint dengan Postman
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/732666b6-12b2-4249-b0ce-32712dd1afe4)

## Pembuatan Controller

1. Lakukan pembuatan direktori controllers di tingkat yang sama dengan index.js

   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/5eb11598-ee83-47fe-a33a-929c7866e9f6)
2. Buatlah file book.controller.js di dalamnya

   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/d66dc764-19e4-42c3-895c-87ea424a8d0a)
3. Salin baris kode dari routes untuk fungsi getAllBooks
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/2e191696-c8f6-474f-9159-140d909ecf83)
4. Lakukan hal yang sama untuk getOneBook, createBook, updateBook, dan deleteBook
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/5f53363a-b18f-42c4-9a2e-67b0ee3f1258)
5. Lakukan import book.controller.js pada file book.route.js
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/d3b0cd7d-391d-4211-88fc-1621bdee0fc0)
6. Lakukan perubahan pada fungsi agar dapat memanggil fungsi dari book.controller.js
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/41c47b0c-6438-4d3a-8368-ef84210d3f9f)
7. Lakukan pengujian kembali, pastikan response tetap sama
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a7d45166-575b-4c3e-a813-ee179caa629b)

## Pembuatan Model

1. Lakukan pembuatan direktori models di tingkat yang sama dengan index.js

   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/f5f5de16-b524-4fa1-bc21-adc1a59150ce)
2. Buatlah file book.model.js di dalamnya

   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/3598440c-dd03-4388-a1c8-67f35dd54989)
3. Tambahkan baris kode berikut sesuai dengan tabel di atas
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a1e4ba72-af40-42e7-b629-03a959036f1c)

## Operasi CRUD

1. Hapus semua data pada collection books
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/4698a7ed-c9c4-4f6a-a153-8d3b38963773)
2. Lakukan import book.model.js pada file book.controller.js
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e7d8de6b-623a-46f1-8a36-7950bd5701f9)
3. Lakukan perubahan pada fungsi createBook
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/81596b06-dd54-4dba-a93e-33cbe66102d6)
4. Buatlah dua buah buku dengan data di bawah ini dengan Postman
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/874b09f2-7a21-4cc4-86e2-3344e95f28e3)
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e2702f9b-7442-4b74-a663-bdeb172f9ee0)
5. Lakukan perubahan pada fungsi getAllBooks

6. Lakukan perubahan pada fungsi getOneBook

7. Tampilkan semua buku dengan Postman

8. Tampilkan buku Dilan 1990 dengan Postman

9. Lakukan perubahan pada fungsi updateBook

10. Ubah judul buku Dilan 1991 menjadi “<NAMA PANGGILAN> 1991” dengan Postman

11. Lakukan perubahan pada fungsi deleteBook

12. Hapus buku Dilan 1990 dengan Postman
