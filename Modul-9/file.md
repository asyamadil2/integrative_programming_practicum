# JSON Web Token (JWT)

## Penyesuaian Database
1. Merubah kolom token pada file migrasi `AddColumnTokenUsers`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/19b7f162-7b12-4720-a703-50eb36ce506e)

2. Menjalankan pereintah `php artisan migrate:fresh` untuk memperbarui data yang lama.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/715fb7fe-a836-44f0-8d0d-5f9827aa1de7)

3. Menjalankan endpoint `/auth/register` menggunakan postman seperti dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/82995bfb-aecb-4612-8350-a26f72ab1cc2)

## JWT Manual
1. Menambahkan 3 fungsi pada file `AuthController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/eb32b722-1ca3-4434-8bde-b871fa9e2b0d)

2. Merubah fungsi login.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/441c64d2-a5d5-47ef-838b-1862ceee790f)

3. Menambahkan 4 fungsi pada file `Middleware/Authorization.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/921d0cae-0378-43b4-b39f-43c3c58a2385)

4. Melakukan perubahan pada fungsi `handle` pada file `Authorization.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/fa8c6a51-ae83-42ce-8fbb-632aae9fb50e)

5. Menjalankan endpoint `/auth/login` menggunakan postman serta menyalin token yang didapat setelah menjalankan endpoint tersebut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/6e8bdd4a-c921-4cc7-8cae-daa659e50e92)

6. Menjalankan endpoint `/home` serta memasukkan token yang telah didapat dari langkah sebelumnya.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/2d080917-bf12-4e45-9da1-3bd8241a71e0)

## JWT Library
1. Melakukan akses terhadap website `https://djecrety.ir/` dan generate jwt key secara online.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/d1b9ee35-7c7f-4204-99e2-251ed8eeb258)

2. Setelah mendapatkan key yang sudah di generate lakukan perubahan pada file `.env` dengan membuat variabel baru dengan nama `JWT_SECRET` dan isi value nya dengan jwt key yang sudah di generate pada langkah sebelumnya.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/ef7eaa0a-93ec-4594-b21c-0001f56ea452)

3. Melakukan instalasi package jwt firebase dengan menjalankan perintah `composer require firebase/php-jwt`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/99394819-1f50-4665-a1e4-df1ae7e9d84c)

4. Menambahkan fungsi dibawah ini pada file `AuthController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/48cc34c9-f56c-4a81-a9fc-40f37e5362cc)

5. Merubah fungsi `login` pada file `AuthController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/4a215f49-eb60-4f5b-90bf-0eff4b1de7ed)

6. Membuat `JwtMiddleware.php` dan isi file tersebut dengan sintaks dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/46119d23-9952-4204-b278-b680b8d3042f)

7. Menambahkan middleware yang dibuat pada langkah sebelumnya pada `bootstrap/app.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/77a4ce4a-61eb-4d4b-9ce1-ef4341bbbb7c)

8. Menambahkan route baru pada `web.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/432b9fe6-ad47-44e4-86cb-7935daf30a8d)

9. Menjalankan endpoint `/auth/login` dengan menggunakan postman dan menyalin token yang didapat setalah menjalankan endpoint tersebut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/8c15e31f-ec1c-4661-8ccc-a9124b567910)

10. Menjalankan endpoint `/home` serta memasukkan token yang didapat dari langkah sebelumnya.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/41830894-6950-43af-8105-a018c1e9fbd2)
