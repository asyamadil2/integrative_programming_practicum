# Relasi One-to-Many dan Many-to-Many
## Pembuatan Tabel
1. Memastikan sudah ada database dengan nama `lumenpost`.

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/0e86ef25-0f6d-43f7-9c4c-07da3e4ca9a9)

2. Mengubah konfigurasi database pada file `.env`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/bf59adb5-f22f-47be-994a-fa1659d6ca0c)
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/d6d77900-1648-466e-a9ef-b181718e9cb6)

3. Menghidupkan library dengan melakukan uncomment sintak pada file `app.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/c7167bfc-27e8-41f6-a693-e03333a5ae7a)

4. Menjalankan perintah dibawah pada command line untuk membuat file migration.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e10981b6-ffb1-4167-8fef-ff4638b18e15)

5. Merubah fungsi `up()` pada file `migrasi create_posts_table`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/ad6f5b90-6fdc-47ba-9ac1-26da6518e2cc)

6. Merubah fungsi `up()` pada file `create_comments_table`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/981fd70e-e9b3-4e7a-9285-e36d0be75504)

7. Merubah fungsi `up()` pada file `create_tags_table`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/5f9f2d65-1475-4086-9eb5-05abc1bec6a5)

8. Merubah fungsi `up()` pada file `create_post_tag_table`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/f45399a2-c5af-45d2-a2e4-e2b9d720634e)

9. Menjalankan command `php artisan migrate`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/4b3a5fbb-fdc0-4367-83a0-3f56113b6fc1)

## Pembuatan Model
1. Membuat file dengan nama `Post.php` dan isi dengan sintak berikut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a4b70ea8-c21f-4c4c-9016-cee693d588fd)

2. Membuat file dengan nama `Comment.php` dan isi dengan sintak berikut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e116fdd3-ffbb-4275-8fe6-9286a2d30cfe)

3. Membuat file dengan nama `Tag.php` dan isi dengan sintak berikut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/ab922a29-193e-4159-b0fe-5cca3be35034)

## Relasi One-to-Many
1. Menambahkan fungsi `comments()` pada file `Post.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/47ffaf77-461f-45ed-adaf-c241bc0fb3aa)

2. Menambahkan fungsi `post()` dan atribut postId pada `$fillable` pada file `Comment.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/9943fcaa-0d3e-4d5b-8615-3ef320cc1775)

3. Membuat file dengan nama `PostController.php` dan isi dengan sintak berikut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/90758ca6-fea9-4b0f-8609-5fc654d376f1)

4. Membuat file dengan nama `CommentController.php` dan isi dengan sintak berikut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/6afaf4ee-d1c0-4543-ab43-46f7b7a6e3ae)

5. Menambahkan sintak dibawah pada `routes/web.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/1046e65a-613d-4817-b364-b5716f133357)

6. Membuat satu post menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/f8f3828e-d0e2-4662-8916-1185633c2c7d)

7. Membuat satu comment menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/8a12020c-3a37-49fe-b19c-768836acfbe6)

8. Menampilkan post menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/aaf9716f-e610-408d-b530-06a34729aa38)

## Relasi Many-to-Many
1. Menambahkan fungsi `tags()` pada file `Post.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/125cca0f-a088-4316-9a10-e9b4ae512352)

2. Menambahkan fungsi `posts()` pada file `Tag.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/8ad6a44d-2bd3-4525-a571-addd8729f8b1)

3. Membuat file dengan nama `TagController.php` dan isi dengan sintak berikut.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e9ede433-a6da-40db-9101-6244a2eb36f9)

4. menambahkan fungsi `addTag` dan response `tags` pada `PostController.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/c13d62e5-a59c-4c2e-9fc4-5c6001a8188f)

5. Menambahkan sintak dibawah pada `routes/web.php`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/c47abff6-c9cf-4d44-957a-a40f7c5e45c9)

6. Membuat satu tag menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/fab8a84b-2964-4bf5-8d54-c38a06f4e1a7)

7. Menambahkan tag `jadul` pada post `disana engkau berdua`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e7359baa-bc92-4cba-9d12-0f5bde929543)

8. Menampilkan post `disana engkau berdua` menggunakan Postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/1060561f-1623-4c8d-9e59-9a014a356a98)

9. Membuat postingan `tanpamu apa artinya` menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/c2e4037f-4bde-4673-8880-907a7ae1ab12)

10. Menambahkan tag `jadul` pada postingan `tanpamu apa aritnya`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/dbacdd63-38aa-473a-aae2-c472cdd4294b)

11. Membuat tag `lagu` menggunakan postman.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/939953c6-6835-44ba-9f9d-68c23068aca2)

12. Menambahkan tag `lagu` pada postingan `tanpamu apa artinya`.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/0aa86cb5-d09d-4b70-8a69-1b40d80b122d)

13. Menampilkan post pertama.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/8e56f395-9cdd-4c1c-8f2e-0a507d633171)

14. Menampilkan post kedua.
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a2c69dcb-ce17-4381-9ba6-8f3b93abd0e3)
