# JSON Web Token (JWT)

## Penyesuaian Database
1. Merubah kolom token pada file migrasi `AddColumnTokenUsers`.
![Cuplikan layar 2023-11-04 201603](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/fae9bcc0-a6d2-4614-8609-d2409af06f98)

2. Menjalankan pereintah `php artisan migrate:fresh` untuk memperbarui data yang lama.
![Cuplikan layar 2023-11-04 201739](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/2fba36d1-c561-41f9-aeed-0c74ad31bc74)

3. Menjalankan endpoint `/auth/register` menggunakan postman seperti dibawah ini.
![Cuplikan layar 2023-11-04 205725](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/dd8e44d5-15d9-4090-9516-b99a325d5c67)

## JWT Manual
1. Menambahkan 3 fungsi pada file `AuthController.php`.
![Cuplikan layar 2023-11-04 211351](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/1c8965de-0f0f-4e3e-987b-13c3363850f4)

2. Merubah fungsi login.
![Cuplikan layar 2023-11-04 212646](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/1de0a417-cc34-4a9b-b6c9-21d7cfb74e12)

3. Menambahkan 4 fungsi pada file `Middleware/Authorization.php`.
![Cuplikan layar 2023-11-04 212804](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/ee3d5168-2a10-411e-bc2a-8663ba729f76)

4. Melakukan perubahan pada fungsi `handle` pada file `Authorization.php`.
![Cuplikan layar 2023-11-05 182705](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/3cb8a5c2-43fa-481d-a91b-678fe079d836)

5. Menjalankan endpoint `/auth/login` menggunakan postman serta menyalin token yang didapat setelah menjalankan endpoint tersebut.
![Cuplikan layar 2023-11-05 183154](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/eef1937d-0066-4349-8780-ae6dd9f2fd88)

6. Menjalankan endpoint `/home` serta memasukkan token yang telah didapat dari langkah sebelumnya.
![Cuplikan layar 2023-11-05 183326](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/9e040374-6723-4f08-a917-251e44a57b02)

## JWT Library
1. Melakukan akses terhadap website `https://djecrety.ir/` dan generate jwt key secara online.
![Cuplikan layar 2023-11-05 183602](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/c4f8a260-a7ea-4966-8040-edc6002d8ac6)

2. Setelah mendapatkan key yang sudah di generate lakukan perubahan pada file `.env` dengan membuat variabel baru dengan nama `JWT_SECRET` dan isi value nya dengan jwt key yang sudah di generate pada langkah sebelumnya.
![Cuplikan layar 2023-11-05 183602](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/8828cbe0-e443-4deb-a401-837619890f0d)

3. Melakukan instalasi package jwt firebase dengan menjalankan perintah `composer require firebase/php-jwt`.
![Cuplikan layar 2023-11-05 184543](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/390c043a-ddd1-4bae-a0a2-60b076e08ac5)

4. Menambahkan fungsi dibawah ini pada file `AuthController.php`.
![Cuplikan layar 2023-11-05 202228](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/ef1ecbc1-6e21-4d47-9d28-2311f16ea2b6)

5. Merubah fungsi `login` pada file `AuthController.php`.
![Cuplikan layar 2023-11-05 202325](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/277f048c-1d89-4897-8505-304698a55b49)

6. Membuat `JwtMiddleware.php` dan isi file tersebut dengan sintaks dibawah ini.
![Cuplikan layar 2023-11-05 202353](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/9d7ccfb3-ec62-4460-8395-e36eb5caaafa)

7. Menambahkan middleware yang dibuat pada langkah sebelumnya pada `bootstrap/app.php`.
![Cuplikan layar 2023-11-05 202441](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/a39af9b0-bb74-4392-8aab-630c6c8eb1eb)

8. Menambahkan route baru pada `web.php`.
![Cuplikan layar 2023-11-05 202522](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/bccb0210-7aeb-40e6-bdab-b6f592314de9)

9. Menjalankan endpoint `/auth/login` dengan menggunakan postman dan menyalin token yang didapat setalah menjalankan endpoint tersebut.
![Cuplikan layar 2023-11-06 102541](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/d1090d54-64de-47ae-a9e3-4ee8c4512b73)

10. Menjalankan endpoint `/home` serta memasukkan token yang didapat dari langkah sebelumnya.
![Cuplikan layar 2023-11-06 102659](https://github.com/alfiyantogw/Prak-Pemin/assets/99490388/0473d9fa-9918-4f4b-a85a-db3ea2469710)
