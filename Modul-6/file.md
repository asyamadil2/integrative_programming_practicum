# Model, Controller dan Request-Response Handler
### Model
1. Memastikan adanya table users pada aplikasi.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/2dcb1d31-5c51-4cc9-8a74-dce12d041dae)

2. Mengganti isi dari file `User.php` pada path `app/Models`dengan
   menggunakan sintkas dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/7e340647-f0f3-4061-bd58-0a5e2847550e)

### Controller
1. Membuat salinan dari file `ExampleController.php` pada folder `app/Http/Controllers` dengan nama `HomeController.php` serta membuat function index dengan sintaks dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/af31cab7-ebaf-482b-ac65-8ad9bd5eded5)

2. Mengubah route pada file `routes/web/php` seperti dibawwah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/3d020dff-335b-4262-bbdd-eb6bc1a62fd4)

3. Menjalakan aplikasi dengan memasukkan `localhost:8000` pada browser sehingga muncul tampilan seperti dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/ca813670-8bf5-44ba-b46a-b9685d907572)

### Request Handler
1. Melakukan import library request pada file `HomeController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/1b90c0dc-448b-4d9a-8afb-74d4e89a0a24)

2. Merubaha `function index()` menjadi seperti dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/966f8fbf-64af-41b6-84b6-17f1bc16fe58)

3. Menjalankan kembali aplikasi terssebut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/78d54ac5-9cc9-45a9-9ea6-1f8c2240ef1e)

### Response Handler
1. Melakukan import library response pada file `HomeController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/addd078e-d980-413e-bf8c-4767badf0d3d)

2. Membuat `function hello()`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/87364a5b-68e7-4714-9f3c-f3168f754820)

3. Menambahkan route `/hello` pada file `routes/web.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/bbdeb9f9-3b32-454c-9123-3b2f402cf567)

4. Menjalankan aplikasi pada route /hello.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/1f0ae167-6476-4d3a-988c-42b08589a1ac)

### Ppenerapan
1. Melakukan import model User dengan menambahkan sintaks berikut pada file `HomeController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/2ac06194-51df-4255-bd0d-b3c182e19934)

2. Menambahkan `function defaultUser()`, `function createUseer()`, dan `function getUsers()`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/76ac16f0-f12b-45fa-9abb-7a2814483e64)
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/b4fe0afa-23a9-44f6-8888-03e9200bc870)

3. Menambahkan route untuk setiap function yang telah dibuat sebelumnya.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/5b14766e-1231-42f8-bb66-e811dac5f6cd)

4. Menjalankan aplikasi pada route `/users/default` menggunakan Postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/617610ac-925f-4eef-b8e8-805a4389a4de)

5. Menjalankan kembali aplikasi melalui Postman pada route `/users/new` dengan mengisi field body seperti dibawah ini.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/99954231-93d4-44b7-8cdd-f78a34e3b601)

6. Menjalankan aplikasi pada route `/users/all`.
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/231e03d4-3edd-4169-a2e3-ec5b4e055d5d)
