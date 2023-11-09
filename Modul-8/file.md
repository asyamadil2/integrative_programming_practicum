# Register, Authentication dan Authorization
## Register
1. Memastikan terdapat tabel users pada aplikasi.

   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/0622317f-c40c-48ff-b4d5-3672c252f97c)

2. Memastikan adanya model `User.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a966d321-c2fc-4003-9b16-b575d7f954a2)

3. Membuat file `AuthController.php` dan isi file tersebut dengan sintaks dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/636d007d-538f-4e0b-a1f3-18b89ea618a5)

4. Menambahkan group route pada `routes/web.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/bf3bf85b-c2b0-4715-8227-12dd190f7c6a)

5. Menjalankan aplikasi pada endpoint `/auth/register` dengan ini body seperti dibawah ini menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/9d37f312-4aa2-4047-b6ba-bdd2d6b1b8b1)

## Authentication
1. Membuat fungsi `login(Request $request)` pada file `AuthController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/f5a14266-b9ea-487e-b165-3787cb8b6c6d)

2. Menambahkan route pada file `web.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/6b13bc32-e059-4e6f-ae61-afe1734b2ddf)

3. Menjalankan aplikasi pada endpoint `/auth/login` dengan ini body seperti dibawah ini menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/79dd87c2-e7eb-4af4-9947-7816461687e8)

## Token
1. Menjalankan perintah dibawhah ini untuk membuat migrasi baru.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/12e63a1d-8110-4903-96d6-55c148fbeb7a)

2. Menambahkan sintaks dibawah ini pada file migration yang dibuat pada langkah sebelumnya.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/f1f230a6-1d9d-4694-9f1e-e30a85a0d30d)

3. Menambahkan atribut token di `$fillable` pada `User.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/6b8825b0-7555-4c2a-b5fb-17e158967dc4)

4. Menambahkan baris berikut pada file `AuthController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/d1a45059-236d-402f-b695-715b5a3040d8)

5. Menjalankan perintah dibawah ini untuk menjalankan migrasi terbaru.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/af47be37-238f-4846-bf87-23dd35b1bf2e)

6. Menjalankan aplikasi pada endpoint `/auth/login` dengan ini body seperti dibawah ini menggunakan postman, dan salin token yang didapat ke notepad.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/131d2d65-aa5c-4294-ac4d-5cf60e5ca4ac)

## Authorization
1. Membuat file `Authorization.php` pada folder `App/Http/Middleware` dan isi dengan sintaks dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/ac0bbe84-0c5b-485f-8125-d37657eb2844)

2. Menambahkan middleware yang baru dibuat pada `bootstrap/app.php.`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/35a2d931-6915-4b89-bc23-74abac748c3b)

3. Membuat fungsi `home()` pada `HomeController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/3872af1e-3be5-42bf-8b14-a1db735e4ed0)

4. Menambahkan route pada file `web.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/fde42520-5704-44fc-8f4b-abc67399ec9f)

5. Menjalankan alikasi pada endpoint `/home` dengan memasukkan nilai token yang telah didapat sebelumnya.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/4a6e1337-7e79-4b5d-9390-0dafed1c15ad)
