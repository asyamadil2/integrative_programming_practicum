![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/15c40770-01e1-4f7f-b943-845a1c114d79)## Menggunakan Mongo DB Compass

1. Lakukan koneksi ke MongoDB menggunakan connection string
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/af5eef16-91c1-4f30-a025-353650d08b3c)
2. Buat database dengan melakukan klik “Create Database”
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/d2eb62fb-2fce-4ed8-8d27-059ea235bccf)
3. Lakukan insert buku pertama dengan melakukan klik “Add Data”, pilih “Insert Document”, isi dengan data yang diinginkan dan klik “Insert”
   
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/e545db2c-39c3-4e6b-ab09-96c440436974)

4. Lakukan insert buku kedua dengan cara yang sama.

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/5755cf1d-6cf6-4b65-8784-bf6ef8dce0e0)

5. Lakukan pencarian buku dengan author “Osamu Dazai” dengan mengisi filter yang diinginkan dan klik “Find”
  
![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/09b76176-d1dc-409c-8fc3-2f20e37bd0d9)

6. Lakukan perubahan summary pada buku “No Longer Human” menjadi “Buku yang
bagus (<NAMA>,<NIM>) dengan melakukan klik “Edit Document” (berlambang
pensil), mengisi nilai summary yang baru, dan melakukan klik “Update”

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/f8ad88a6-97d5-4d5a-a19c-be862183283c)

7. Lakukan penghapusan pada buku “I Am a Cat” dengan melakukan klik “Remove
Document” (berlambang tong sampah) dan melakukan klik “Delete”

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/585e3d4f-6473-468b-a0d9-198bbf9bd6af)

## Menggunakan Mongo DB Shell

1. Lakukan koneksi ke MongoDB Server dengan menjalankan command mongosh bagi
yang menggunakan terminal build in OS sehingga tampilan terminal kalian akan
menjadi seperti berikut

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/451061be-687d-41bc-adb0-ca9a3e21654d)

2. Mencoba melihat list database yang ada di server dengan menjalankan command
`show dbs`

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/59bf81e0-174c-42ed-94b4-ccaa68d608a4)

Untuk berpindah ke database “bookstore” gunakan command `use bookstore` , kalian
dapat memastikan telah berpindah ke database yang benar dengan melihat tulisan
sebelum tanda “>”

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/574220da-badf-46f0-98e1-05c4b9090915)

Cobalah untuk melihat collection yang ada pada database tersebut dengan
menggunakan command `show collections`

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/7bd0db11-d6be-423e-9e24-6622d6e322c4)

3. Lakukan insert buku “Overlord I” dengan menggunakan command
`db.books.insertOne(<data kalian>)` , setelah insert buku berhasil maka MongoDB akan
mengembalikan pesan sebagai berikut.

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a8352e98-b11c-442b-8e3c-aa84a894620c)

4. Lakukan insert buku “The Setting Sun” dan “Hujan” dengan insert many dengan
menggunakan command `db.books.insertMany(<data kalian>)` , dan akan mengembalikan pesan sebagai berikut.

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/41e83de3-7160-427a-8d24-8237aa8633d9)

5. Lakukan pencarian buku dengan menggunakan command `db.books.find()` untuk
melakukan pencarian semua buku.

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/3d9a700d-dfaf-4070-9951-659361c5bf49)

6. Tampilkan seluruh buku dengan author “Osamu Dazai” dengan mengisi argument
pada find() dengan menggunakan command `db.books.find({<filter yang ingin
diisi>})`

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/03edaa4c-a7e9-4db9-abff-b9b1e3fbff1d)

7. Lakukan perubahan summary pada buku “Hujan” menjadi “Buku yang bagus
(<NAMA>,<NIM>) dengan mengunakan `command db.books.updateOne({<filter>},
{$set: {<data yang akan di update>}})` sehingga output yang dihasilkan oleh MongoDB
akan menjadi seperti berikut

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/7f3871c2-0411-48b3-9ed2-d962da19abab)


8. Lakukan perubahan publisher menjadi “Yen Press” pada semua buku “Osamu
Dazai” dengan menggunakan command `db.books.updateMany({<filter>}, {$set: {<data
yang akan di update>}})`

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/1f4dc8a1-965c-4443-a8ab-1db15789ff54)

9. Lakukan penghapusan pada buku “Overlord I” dengan menggunakan command
`db.books.deleteOne({<argument>})`

 ![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/278fcbcd-8d58-46d1-82f7-0bc4d11fa868)

10.Lakukan penghapusan pada semua buku “Osamu Dazai dengan menggunakan
command `db.books.deleteMany({<argument>})` 

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/a22f0e79-7b3c-4bb9-a06c-dc638dddb461)

![image](https://github.com/asyamadil2/integrative_programming_practicum/assets/107811435/6122014e-9853-4a07-8115-6fa5eba19134)

