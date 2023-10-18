# Dynamic Route dan Middleware

### Dynamic Route
1. Menambahkan dynamic routes pada aplikasi lumen dengan menggunakan sintaks dibawah ini pada file `routes\web.php`.
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/fc56488a-1a32-4cf3-abff-fc4d738f21cc)

2. Selanjutnya adalah menambahkan parameter pada routes.
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/1c837cad-9d61-47de-9363-06026d89e681)

3. Menambahkan optional routes pada aplikasi lumen kita, saat memanggil endpoint tidak harus menggunakan parameter variable.
  ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/fee2522f-8776-42e6-abe2-40b9de8277d5)

### Aliases Route
1. Menggunakan aliases route untuk memberikan naman pada route yang telah dibuat.
  ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/74a8daa1-4b0c-4674-b124-d562de0c5b15)

### Group Route
1. Melakukan grouping terhadap routes agar lebih mudah pada saat penulisan route pada `web.php`.
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/285c4804-f8f3-4f8b-881a-c82ad39c2fbe)

### Middleware
1. Membuat middleware baru dengan nama `AgeMiddleware` pada path `app/Http/Middleware` dengan isi sebagai berikut.
  ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/1633a727-4e86-422c-8eac-cb5a60114393)

2. Selanjutnya adalah dengan menambahkan `AgeMiddleware` pada aplikasi yang dibuat dengan menambahkan sintaks berikut pada file `bootstrap/app.php`.
 ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/0de1ecce-6e98-42c6-9381-28e9bd31b6e8)

3. Terakhir adalah menambahkan middleware pada routes dengan sintaks berikut.
   ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e7ed7e50-418a-4bd9-b29c-809272f00434)
