# SPARK

Nama   : Annisa Aulia Nadhila

Kelas  : TI - 3C

NIM  : 2041720023

## Praktikum

Jelaskan masing-masing maksud kode berikut sesuai nomor kodenya pada laporan praktikum Anda!

### **mylist, myschema**
merupakan list dan scema awal yang digunakan untuk membuat dataframe


### **spark.createDataFrame**
-> berfungsi untuk membuat **DataFrame** dari RDD, list, atau pandas.DataFrame.

-> Jika skemanya hanya berupa daftar nama kolom, tipe data setiap kolom akan secara otomatis disimpulkan dari data.

-> Jika tidak ada skema yang disediakan, Spark akan mencoba menyimpulkan skema (nama dan tipe kolom) dari data yang diberikan. Data harus berupa RDD dari Baris, bernama tuple, atau dict

### **parallelize, toDF**
-> parallelize() adalah fungsi di SparkContext dan digunakan untuk membuat RDD dari kumpulan list.

-> toDF: Mengembalikan DataFrame baru dengan kolom yang diganti namanya, juga Gunakan fungsi toDF untuk mengubah Dataset menjadi DataFrame.

### **hadoop, fs, put**
-> Hadoop adalah platform perangkat lunak yang memungkinkan pengolahan data secara terdistribusi pada cluster besar yang terdiri dari ribuan node dan kapasitas data mencapai petabyte. Cluster Apache Hadoop dapat dibangun menggunakan perangkat keras standar dengan tingkat kegagalan yang tinggi.

-> `fs` (File System) pada PySpark adalah antarmuka yang menyediakan akses ke berbagai sistem file, termasuk Hadoop Distributed File System (HDFS) dan sistem file lokal. `fs` menyediakan berbagai metode untuk membaca dan menulis file, mengelola direktori, dan melakukan operasi file system lainnya.

-> `put` adalah sebuah operasi untuk mengunggah file atau objek dari mesin lokal atau virtual ke sistem penyimpanan objek pada PySpark. Untuk menggunakan `put`, perlu memanfaatkan modul atau library yang disediakan oleh penyedia layanan penyimpanan objek dan biasanya digunakan fungsi `put` untuk melakukan operasi upload ke penyimpanan objek.

### **pyspark.sql, SQLContext, createOrReplaceTempView, show**

-> Pyspark.sql adalah modul pada Apache Spark yang menyediakan antarmuka untuk bekerja dengan data terstruktur menggunakan bahasa pemrograman Python. Modul ini menyediakan API yang kuat untuk membaca, memanipulasi, dan menulis data terstruktur seperti CSV, JSON, Parquet, dan sumber data JDBC lainnya. Pyspark.sql juga memiliki dukungan untuk SQL tradisional serta fungsi analitik dan agregasi yang kuat untuk memproses data secara efisien.

-> SQLContext dapat digunakan untuk membuat DataFrame, mendaftarkan DataFrame sebagai tabel, mengeksekusi SQL di atas tabel, tabel cache, dan membaca file parket.

-> `createOrReplaceTempView` pada PySpark adalah metode untuk membuat view sementara dari DataFrame yang memungkinkan pengguna untuk mengeksekusi query SQL pada data tanpa perlu membaca ulang data. View ini memiliki nama unik dan dapat ditimpa jika sudah ada view dengan nama yang sama. View sementara ini hanya ada selama sesi Spark dan dihapus setelah sesi ditutup. Dengan `createOrReplaceTempView`, pengguna dapat menggunakan sintaks SQL untuk melakukan query pada data DataFrame dengan mudah.

-> show: Prints the first n rows to the console

### **textFile, map, lambda, strip, StructField, StringType**

-> Fungsi textFile() pada SparkContext digunakan untuk membaca file teks yang tersimpan di HDFS, S3, dan sistem file lainnya yang dapat diakses oleh Hadoop. Fungsi ini menerima argumen berupa path ke file dan dapat juga menerima argumen opsional berupa jumlah partisi.

-> (map()) adalah fungsi yang digunakan untuk memodifikasi setiap elemen RDD atau DataFrame dengan fungsi transformasi (lambda) dan menghasilkan RDD baru. 

-> Metode `strip()` adalah metode pada objek string di pandas yang dapat digunakan untuk menghapus karakter awal dan akhir dari sebuah string, termasuk spasi putih atau sekumpulan karakter tertentu. Metode ini dapat diterapkan pada setiap string dalam Seri/Indeks pada sisi kiri dan kanan. Metode `strip()` juga memiliki opsi `ke_strip` yang dapat digunakan untuk menentukan karakter yang ingin dihapus. Metode `strip()` ini setara dengan metode `str.strip()`.

-> Di PySpark, StructField adalah representasi dari sebuah field di StructType. StructField terdiri dari tiga komponen yaitu, nama (sebagai string), tipe data (Tipe Data), dan nullable (boolean), dimana nama field adalah nama dari StructField tersebut.

-> StringType atau "pyspark.sql.types.StringType" adalah tipe data pada PySpark yang digunakan untuk merepresentasikan nilai string. Untuk membuat sebuah variabel dengan tipe data string pada PySpark, Anda dapat menggunakan sintaks `StringType()`.

### **spark.read.format, jdbc, options, load**
-> spark.read.format adalah metode di Apache Spark yang digunakan untuk membaca data dari berbagai sumber data seperti file CSV, JSON, Parquet, Avro, dan lain-lain. 

-> jdbc adalah modul di Apache Spark yang digunakan untuk membaca dan menulis data dari database menggunakan JDBC (Java Database Connectivity).

-> options adalah parameter di Apache Spark yang digunakan untuk menentukan opsi konfigurasi saat membaca atau menulis data dari atau ke sumber eksternal.

-> load digunakan untuk memuat data ke dalam DataFrame dengan format tertentu, seperti CSV, JSON, parquet, atau ORC.

### **show**

-> Metode show di Apache Spark digunakan untuk menampilkan data dari DataFrame secara tabular. DataFrame adalah struktur data yang mirip dengan tabel dalam database relasional. Metode show secara default menampilkan 20 baris pertama dari DataFrame.

### **collect, rdd, take**

-> collect = metode dalam Apache Spark yang digunakan untuk mengambil seluruh data dari DataFrame dan dikumpulkan dalam bentuk Python list. Namun, metode ini dapat menyebabkan overhead yang besar terutama jika data yang diolah sangat besar.

-> rdd = RDD adalah kumpulan data yang terdistribusi di seluruh node dalam sebuah cluster, dapat diproses secara terpisah dan paralel. RDD pada Spark dapat dilakukan berbagai operasi seperti map, filter, join, dan lain-lain, dan Spark akan secara otomatis membagi pekerjaan tersebut di antara node dalam cluster.

-> take = metode dalam Apache Spark yang digunakan untuk mengambil sejumlah baris dari RDD atau DataFrame dan mengembalikan hasilnya ke driver node dalam bentuk Python list.

### **makeRDD, Seq, createDataset**

-> Metode makeRDD digunakan untuk membuat RDD baru dari data yang sudah ada di dalam memori, seperti list, tuple, atau array. Dengan menggunakan makeRDD, pengguna dapat membuat RDD secara eksplisit dari data yang disediakan.

-> Seq adalah tipe data di Scala yang merepresentasikan sebuah urutan dari elemen-elemen yang dapat diakses secara berurutan. Pada Spark, Seq sering digunakan sebagai parameter input untuk metode yang memerlukan sebuah kumpulan data atau sekumpulan nilai. Seq juga dapat digunakan untuk membuat kumpulan data dalam bentuk RDD.

-> Metode createDataset digunakan untuk membuat sebuah Dataset, yaitu struktur data yang mirip dengan DataFrame, tetapi dengan tipe data yang terjaga dan mendukung pemrograman fungsional. createDataset menerima sebuah Seq atau List dari objek-objek yang ingin dibuatkan Dataset-nya, sehingga pengguna dapat dengan mudah membuat Dataset dari sekumpulan data yang diberikan.

### **filter**

-> Filter digunakan untuk melakukan penyaringan pada Dataset atau DataFrame dengan kriteria tertentu. Metode ini menerima ekspresi boolean sebagai parameter dan mengembalikan Dataset atau DataFrame yang hanya berisi baris yang memenuhi kriteria tersebut.

### **as, toDF, first**

-> as = digunakan untuk memberikan alias (nama lain) pada sebuah kolom dalam sebuah DataFrame atau Dataset. Alias ini bisa berguna untuk memberikan nama yang lebih deskriptif dan mudah dipahami pada kolom-kolom yang dihasilkan dari operasi-operasi transformasi pada DataFrame.

-> toDF = digunakan untuk mengubah sebuah RDD (Resilient Distributed Dataset) menjadi sebuah DataFrame. toDF menerima parameter berupa nama-nama kolom untuk DataFrame yang dihasilkan, atau bisa juga tidak memiliki parameter untuk menghasilkan DataFrame dengan kolom-kolom default ("_1", "_2", dst).

-> first = digunakan untuk mengembalikan elemen pertama dari RDD. Metode ini mengambil satu elemen pertama dari RDD dan mengembalikannya ke driver program. Metode first sangat berguna ketika pengguna ingin melihat elemen pertama dari RDD, seperti ketika ingin memeriksa struktur dari data yang sedang diolah.

### **listDatabases, listTables, listFunctions, isCached, select**

-> listDatabases : Mengembalikan daftar database yang tersedia di semua sesi.
-> listTables : Mengembalikan daftar tabel/tampilan dalam database yang ditentukan.
-> listFunctions : Mengembalikan daftar fungsi yang terdaftar di database yang ditentukan.
-> isCached : Mengembalikan nilai true jika tabel saat ini di-cache dalam memori.
-> select : Memproyeksikan sekumpulan ekspresi dan mengembalikan DataFrame baru.

### **Read, text**

-> Metode Read digunakan untuk menyesuaikan cara data dibaca dari sumber data tertentu, seperti file, database, atau sumber data lainnya.

-> Metode text digunakan untuk membaca file teks dan mengonversinya menjadi sebuah DataFrame, sehingga pengguna dapat melakukan operasi transformasi dan analisis data pada file teks tersebut.

### **load, json, format, printSchema**

-> Metode load digunakan untuk memuat data dari sumber data dan mengembalikannya dalam bentuk DataFrame. 

-> Metode json digunakan untuk membaca file JSON ke dalam Spark DataFrame. 

-> Metode format digunakan untuk memuat file atau memformat data yang berasal dari sumber data dengan tipe data tertentu. 

-> Metode printSchema digunakan untuk mencetak skema DataFrame dalam format pohon.

### **write, save**

-> Metode write digunakan untuk menyimpan konten DataFrame yang bukan streaming ke penyimpanan eksternal. Metode ini dapat digunakan untuk menyimpan data ke berbagai jenis penyimpanan, seperti file sistem lokal atau Hadoop Distributed File System (HDFS).

-> Metode save digunakan untuk menyimpan konten DataFrame ke sumber data. Metode ini dapat digunakan untuk menyimpan data ke berbagai sumber data seperti HDFS, Cassandra, atau JDBC. Metode save dapat digunakan untuk menyimpan DataFrame dalam berbagai format, seperti CSV, JSON, atau Parquet.

### **parquet**

-> parquet : Menyimpan konten DataFrame dalam format Parket pada path yang ditentukan.

### **Options, inferSchema, csv, header, codec**

-> Options: digunakan untuk menyesuaikan atau memberikan opsi pada bagaimana data akan dibaca dari sumbernya.

-> inferSchema: merupakan alternatif dari fungsi schema yang dapat menyesuaikan tipe data kolom pada file CSV dengan lebih cepat.

-> csv: digunakan untuk memuat file CSV dan mengembalikan hasilnya sebagai DataFrame.

-> header: merupakan opsi yang digunakan jika file CSV memiliki header, sehingga baris pertama akan digunakan sebagai nama kolom.

-> codec: opsi ini digunakan untuk menentukan codec kompresi yang akan digunakan pada output. Beberapa codec yang didukung adalah gzip, snappy, dan bzip2.