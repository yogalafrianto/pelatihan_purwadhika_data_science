# STOCK OPNAME BARANG TOKO

Yoga merupakan seorang programer yang handal, kebetulan yoga ini merupakan anak dari pemilik sebuah toko sembako yang masih melakukan stock opname secara manual ditulis pada dalam kertas. Yoga berinisiatif untuk membuat sebuah program stock opname yang sederhana memiliki fungsi CRUD pada sistem yang nantinya dibuat. Pada sistem ini yoga hanya membutuhkan kode dari produk, kemudian nama dari masing-masing produk, harga satuan beserta quantity, stock yang dimiliki di toko, dan kategory dari product yang ada. Dalam sistem ini yoga juga dapat mengetahui secara langsung total aset dagangan yang dimiliki.

# Feature:
## 1. Create
Create data disini berfungsi untuk menambahkan produk baru kedalam data, dimana inputan data yang diminta terdiri dari
- Kode --> Kode ini berupa string sehingga inputan yang dilakukan harus berisi alfabet dan dalam inputan ini dilakukan validasi terlebih dahulu dengan fungsi input_alfabet, serta dalam kode ini dilakukan pengecekan juga agar kode tidak boleh kembar atau sama dengan kode yang sudah ada, sehingga unik keynya disini adalah kode
- Nama Barang --> Berisi inputan berupa string, dimana dalam inputan ini dilakukan validasi menggunakan fungsi yang telah di buat dengan nama fungsi input_alfabet
- Jenis Satuan --> Inputan dengan type strin dan untuk jenis satuan ini juga dilakukan pengecekan terlebih dahulu sebelum disimpan kedalam database. Validasi ini menggunakan fungsi input_alfabet
- Harga --> Harga disini merupakan inputan data yang diminta dengan jenis numeric, dan pada inputan ini dilakukan validasi terhadap inputan yang dilakukan dengan fungsi input_numerik
- Stok --> Inputan ini berjenis numeric untuk mengetahui jumlah stok barang baru yang ingin didaftarkan
- Kategori --> Kategori merupakan inputan yang saya buat berupa alfabet dan juga charakter unik dengan mengandung symbol (*) dan symbol (&), dan untuk inputan ini dilakukan validasi dengan fungsi input_alfabet_character
  
## 2. Read
Fitur ini berfungsi untuk menampilkan data base yang telah dibuat sebelumnya, dan nantinya data base ini akan secara otomatis terupdate ketika kita melakukan penambahan, atau penghapusan, serta pengupdatean data. Serta untuk fitur ini, saya menambahkan index penomoran yang digenarate secara otomatis yang berfungsi untuk numbering saja, sehingga pengguna tidak perlu melakukan penginputan nomor.
Berikut contoh data sampel default yang saya buat:
|Index|Kode|Nama Barang|Satuan|Harga|Stock|Kategori|
|-----|-----|-----|-----|-----|-----|-----|
|1|AA|Gula|Kg|8000|50|Bahan Pokok|
|2|BB|Beras|Kg|15500|320|Makanan & Minuman|
|2|CC|Susu Beruang|Pcs|10000|80|Minuman Kaleng|

## 3. Update
Update merupakan fitur yang dibuat untuk melakukan pembaharuan data pada baris dengan kolom tertentu yang diinginkan, fitur ini melakukan validasi pada setiap kolom yang dipilih, validasi yang dilakukan bergantung pada kolom yang dipilih.

## 4. Delete
Delete data merupakan fungsi untuk menghapus stok produk yang ada didata base. Cara menghapusnya pengguna nantinya hanya perlu menginputkan kode produk yang tertera pada tabel yang tersedia. Kode ini bersifat unik sehingga satu kode produk tidak akan sama dengan kode produk yang lainnya. 

## 5. Menghitung Total Nilai Aset Product
Pada fitur ini, pengguna bisa mengetahui nilai aset yang dimiliki per produk dan juga total aset keseluruhan produk yang dimilikinya.

## 6. Validasi Kode agar tidak diizinkan untuk sama
Validasi ini merupakan fungsi untuk tidak mengizinkan kode barang sama dengan kode barang lainnya, baik itu ketika create produk ataupun melakukan update data. Sehingga kode barang bersifat unik karena kode tersebut hanya dapat dimiliki oleh satu produk.

# Keys:
1. Index (Auto Fill)
2. Kode
3. Nama Barang
4. Satuan
5. Harga
6. Kategori
7. Stock


