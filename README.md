# Metode-Numerik-2021

Anggota Kelompok 9:

Indah Bella Pratiwi / 26050119130048 / Oseanografi B
Nia Oktaviani Annisa Putri / 26050119130047 / Oseanografi A
Khofifah Itsna Maghfiroh / 26050119130045 / Oseanografi B
Renita Setyowati / 26050119130044 / Oseanografi B
Muhammad Azizi Dirgantara B.N. / 26050119130041 / Oseanografi B
Muhammad Shulhan J. / 26050119130040 / Oseanografi A
M Azka Zahran / 26050119130037 / Oseanografi B
Gamma Haqqul Fikriawan / 26050119130036 / Oseanografi B
Adwitiyadewi Nuraziza A. / 26050119130034 / Oseanografi B
Tia oktavia / 26050119120032 / Oseanografi A
Beltrand Yordan Simangunsong / 26050119120031 / Oseanografi B
KATA PENGANTAR
Alhamdulillah, puji dan syukur kami panjatkan kepada Tuhan Yang Maha Esa yang telah melimpahkan rahmat serta hidayat Nya, sehingga kami dapat menyelesaikan penyusunan tugas akhir praktikum metode numerik ini dengan semaksimal mungkin. Selama proses penyusunan tugas ini, kami mendapatkan banyak bimbingan dan bantuan dari berbagai pihak. kami menyadari bahwa tanpa bantuan dan dorongan yang tiada henti dari pihak lain rasanya penyusunan tugas ini sulit untuk diselesaikan. Maka dari itu kami ucapkan terima kasih kepada:

Dosen Pengampu Mata kuliah Metode Numerik yang telah memberikan ilmunya
Tim asisten yang telah membimbing serta memberikan ilmunya selama praktikum.
Bapak dan Ibu yang selalu mendo’akan, memotivasi, dan mendukung setiap Langkah kami.
Teman-teman yang selalu memberikan bantuan dan dukungan hingga penyusunan tugas akhir praktikum ini selesai. Penyusunan tugas akhir praktikum ini tentunya masih banyak kekurangan. Maka dari itu, kami sangat mengharapkan saran dan kritikan yang bersifat membangun. Kami berharap tugas ini dapat memberikan manfaat kepada pembaca khususnya kami mengenai metode numerik ini.
Semarang, 3 Juni 2021

Tim Penulis

Library dan Modul yang digunakan
Pada praktikum metode numerik kali ini, digunakan beberapa library seperti matplotlib, numpy, dan lain-lain. Penjelasan dari tiap library dijelaskan sebagai berikut:

Matplotlib
Berdasarkan homepage dari matplotlib (https://matplotlib.org/2.0.2/index.html): “matplotlib adalah library python untuk melakukan plotting 2D yang mana akan menghasilkan gambar berkualitas dalam format yang bervariasi dan dalam lingkungan yang interaktif dalam berbagai platform. Matplotlib dapat digunakan dalam script python, shell python dan Ipython, jupyter notebook, aplikasi web dan lain-lain”. Dalam kata lain, matplotlib dapat dengan mudah membuat plot, histogram, grafik batang, scatterplot, dan hal lainnya hanya dengan menggunakan python dan beberapa baris kode saja. Library ini dapat membantu sehingga dalam melakukan analisis dan explorasi dapat dilakukan lebih cepat (Morgan, 2016).

image

Gambar 1. Contoh diagram batang menggunakan matplotlib

(Sumber: Morgan, 2016)

Numpy
Numpy merupakan salah satu package primer pada python untuk melakukan komputasi saintifik. Library tersebut mempunyai N-dimensional array, tools untuk melakukan integrasi C/C++ dan kode fortran, aljabar linear, fourier transofrn, dan lain-lain. Numpy juga mendukung broadcasting yang mana merupakan sebuah cara bagi fungsi universal untuk berhubungan dengan input yang tidak mempunyai bentuk yang sama. Selain kemampuan tersebut, kelebihan lain dari NumPy adalah dapat diintegrasikan dalam program python. Dalam kata lain, suatu data dapat diambil dari database, output program lain, file external, atau halaman HTML dan kemudian diproses menggunakan NumPy. NumPy dapat juga digunakan dengan Pygame, yang merupakan sebuah package python untuk membuat games (Asadi, 2016).

SYS
Module ini menyediakan akses untuk beberapa variabel yang digunakan atau dimaintain oleh interpreter dan sebagai fungsi yang dapat beriteraksi dengan interpreter. Hal ini sudah tersedia dalam python sehingga tidak perlu mengimport.

OS
OS merupakan sebuah library dalam python yang menyediakan suatu cara portable dalam menggunakan fungsi yang bergantung pada operating system.

Beberapa contoh dalam library ini adalah:

open(), yang berguna untuk membuka atau memodifikasi suatu files
os.path yang berguna untuk memanipulasi path
fileinput untuk membaca semua baris dalam semua file pada command line
tempfile untuk membuat temporary files dan directories
Hal yang harus dicatat dalam ketersediaan fungsi pada library ini:

Desain dari semua modul Python bergantung pada sistem operasi bawaan sedemikian rupa sehingga selama fungsionalitas yang sama tersedia, ia menggunakan interface yang sama.
Ekstensi khusus untuk sistem operasi tertentu juga tersedia melalui modul os, tetapi menggunakannya tentu saja merupakan ancaman bagi portabilitas.
Semua fungsi yang menerima nama path atau file menerima objek byte dan string, dan menghasilkan objek dengan tipe yang sama, jika path atau nama file dikembalikan.
Pada VxWorks, os.fork, os.execv dan os.spawnp tidak didukung.
Ipython
Salah satu dari fitur utama python adalah interpreternya yang interaktif. Hal tersebut memungkinkan untuk testing suatu hal secara cepat tanpa harus membuat test files sebagaimana bahasa pemrograman yang lain. Akan tetapi, interpreter yang didukung oleh distribusi standar python mempunyai Batasan bagi penggunaan yang interaktif.

Tujuan dari IPython adalah untuk membuat suatu kondisi atau lingkunagn yang interaktif dalam suatu komputasi. Untuk mendukung hal ini, IPython mempunyai 3 komponen utama:

Peningkatan python shell yang lebih interaktif
Model komunikasi dua proses yang dipisahkan, yang memungkinkan beberapa klien untuk terhubung ke kernel komputasi, terutama notebook berbasis web yang menggunakan Jupyter
Arsitektur untuk komputasi interaktif parallel yang menjadi bagian dari package ipyparallel
Shell interaktif IPython (ipython), memiliki tujuan sebagai berikut:

Memberikan shell interaktif yang lebih unggul dari shell Python default. IPython memiliki banyak fitur untuk penyelesaian tab, introspeksi objek, akses ke system shell, pengambilan riwayat perintah di seluruh sesi, dan sistem perintah khusus untuk menambahkan fungsionalitas saat bekerja secara interaktif. Hal ini menjadi lingkungan yang sangat efisien baik untuk pengembangan kode Python dan untuk eksplorasi masalah menggunakan objek Python (seperti dalam analisis data).
Menjadi interpreter yang siap digunakan dan dapat disematkan dalam suatu program. Shell IPython yang interaktif dapat dibuka dengan satu panggilan dari dalam program lain, menyediakan akses ke namespace saat ini. Hal Ini sangat berguna baik untuk tujuan debugging maupun untuk situasi dimana campuran batch-processing dan eksplorasi interaktif diperlukan.
Menawarkan framework fleksibel yang dapat digunakan sebagai kondisi atau lingkungan dasar untuk bekerja dengan sistem lain, menggunakan Python sebagai bahasa dasar.
Memungkinkan pengujian interaktif toolkit grafis. IPython memiliki dukungan untuk kontrol interaktif dan tidak terblokir dari aplikasi GTK, Qt, WX, GLUT, dan OS X melalui flag threading khusus. Sedangkan shell Python normal hanya dapat melakukan ini untuk aplikasi Tkinter.
MODUL 1: PENGENALAN METODE NUMERIK DAN PYTHON
1.1 Definisi Metode Numerik

Metode numerik adalah teknik untuk menyelesaikan permasalahan yang diformulasikan secara matematis dengan cara operasi hitungan. Dalam metode numerik terdapat beberapa bentuk proses hitungan atau algoritma untuk menyelesaikan suatu tipe persamaan matermatis, seperti operasi dasar hitungan penjumlahan, pengurangan, perkalian dan pembagian. Menurut Sudiarta (2020), terdapat empat bagian utama dalam metode numerik, yaitu:

Teori yang mendasari perhitungan numerik
Algoritma atau langkah-langkah yang dilakukan dalam menyelesaikan masalah atau mendapatkan hasil
Pemograman yang dibutuhkan untuk memberikan instruksi kepada computer dalam melakukan perhitungan numerik
Visualisasi yang merupakan proses menampilkan anka-angka atau data dalam bentuk berbeda sehingga mudah untuk mengenali dalam interpretasi hasil
1.2 Prinsip Kerja dan Cara Pengerjaan Metode Numerik

Untuk menerapkan metode numerik, dibutuhkan berbagai pendekatan-pendekatan matematiss, dan setiap pendekatan memiliki tingkat kesalahan yang berbeda-beda. Metode numerik memberikan solusi yang menghampiri atau mendekati solusi sejati sehingga dinamakan solusi hampiran, tetapi solusi hampiran dapat dibuat seteliti yang diinginkan dan terdapat nilai galat yang tidak sama dengan nol (Faradillah, 2020). Metode numerik memberikan cara-cara untuk menyelesaikan bentuk persamaan tersebut secara perkiraan hingga didapat hasil yang mendekati penyelesaian secara besar (eksak). Penyelesaian numerik dilakukan dengan perkiraan yang berurutan (iterasi), maka tiap hasil akan lebih teliti yang dianggap cukup akan didapat hasil perkiraan yang mendekati hasil yang benar (eksak) dengan toleransi yang disesuaikan (Panjaitan, 2017). Kemudahan dalam pemograman dan banyaknya tambhan modul-modul yang membantu dalam penyelesaian permasalahan matematis serta visualisasi hasil yang baik, menjadikan Phyton sebagai pilihan dalam penerapan metode numerik. Pengerjaan kalkulasi pada dokumen interaktif Jupyter Notebook menghasilkan sebuah dokumen yang menampilkan secara lengkap empat bagian metode numerik.

1.3 Peranan Komputer dalam Metode Numerik

Perhitungan operasi aritmatika dalam metode numerik (jumlah, kali, bagi dan perbandingan) sangat banyak dan sering berulang sehingga akan memerlukan tenaga yang besar untuk mengolah data tersebut dan sering kali timbul berbagai kesalahan. Dengan bantuan computer maka akan mempercepat proses perhitungan dengan hasil yang benar. Penggunaan computer dalam metode numerik antara lain untuk membuat program. Langkah-langkah metode numerik diformulasikan menjadi program komputer dengan Bahasa pemograman tertentu. Selain mempercepat perhitungan metode numerik, dengan penggunaan komputer maka akan dapat menyelesaikan berbagai persoalan yang terjadi akibat perubahan beberapa parameter. Solusi yang diperoleh juga dapat ditingkatkan ketelitiannya dengan mengubah nilai parameter (Rachmad et al., 2017).

1.4 Phyton

Bahasa Phyton merupakan bahasa pemograman tingkat tinggi yang mudah digunakan dan memiliki cara penulisan atau syntax yang sederhana, mudah ditulis dan dibaca (dalam bahasa Inggris). Kode bahasa Phyton berupa script, perintah-perintah atau pernyataan-pertanyaan yang tidak memerlukan kompilasi sehingga dapat langsung dijalankan. Hal ini membuat penulisan kode program dapat lebih cepat. Program Phyton merupakan sebuah interpreter seperti program Matlab ataupun yang lainnya, yang dapat menerjemahkan kode Phyton. Program Phyton juga menyediakan fasilitas development environment IDLE. Pada environment ini kita dapat menjalankan atau mengevaluasi perintah-perintah atau kode Phyton secara langsung atau disebut REPL atau Read-Evaluate-Print-Loop (Sudiarta, 2020). Terdapat empat cara untuk menjalankan kode program Phython yaitu:

Menggunakan Phyton Interpreter
Menggunakan aplikasi Phyton IDLE
Menggunakan Phyton pada Command Prompt
Menggunakan Jupyter Notebook Perintah-perintah atau pernyataan-pernyataan dengan bahasa Phyton dapat langsung dieksekusi di sel pada sebuah dokumen interaktif Jupyter Notebook. Kode dan hasilnya dapat langsung ditampilkan dalam satu dokumen sehingga membuat Jupyter Notebook menjadi pilihan dalam penerapan metode numerik.
1.5 Jupyter Notebook

Jupyter Notebook memungkinkan pengguna bahasa pemograman utama yang lebih beragam yaitu Julia, Python dan R. Jupyter Notebook bersifat opensource sehingga setiap orang dapat mengunduhnya dari internet. Bagi pengguna pemula, cara yang paling mudah adalah dengan mengunduh anaconda dari website. Anaconda memuat lebih dari 300 paket Python terpopuler di bidang matematika, sains, rekayasa dan analisis data termasuk Jupyter Notebook App. Menurut Setiabudidaya (2018), Jupyter Notebook (file yang berekstensi ipynb) adalah dokumen yang dihasilkan oleh Jupyter Notebook App yang berisikan kode komputer dan rich text element seperti paragraph, persamaan matematik, gambar dan tautan (links). Jupyter Notebook dikenal sebelumnya sebagai IPython Notebook dan dalam waktu dekat akan berevolusi menjadi Jupyter Lab

MODUL 2: AKAR-AKAR PERSAMAAN
Pada penyelesaian akar- akar persamaan ada lima metode yang dapat digunakan dalam metode numerik. Pertama adalah metode setengah interval yaitu Kelebihan dari metode ini adalah selalu berhasil dalam menentukan akar-akar (solusi) yang dicari atau dengan kata lain selalu konvergen. Selain kelebihan, dalam metode bisection juga terdapat kekurangan, yaitu pada metode biseksi hanya dapat dilakukan apabila ada akar persamaan pada interval yang diberikan. Kedua Metode Interpolasi Linier yang hampir mirip dengan metode setengah interval. Kemiripannya adalah terletak dalam hal diperlukan dua harga taksiran awal pada awal pengurungan akar persamaan. Sedangkan, perbedaannya terletak pada proses pencarian pendekatan akar persamaan selanjutnya setelah pendekatan akar saat ini ditemukan Prinsip pencarian akar persamaan dari metode ini didasarkan pada penggunaan interpolasi linier. Ketiga yaitu Metode Newton-Raphson yang terbukti memiliki laju konvergensi lebih cepat dibandingkan dengan metode bagi dua maupun metode Regula Falsi. Akan tetapi,syarat yang harus dipenuhi adalah bahwa taksiran awal yang diberikan harus sedekat mungkin dengan harga eksaknya. Hal ini untuk mengantisiasi seandainya fungsi nonliniernya tidak seperti yang kita harapkan. Keempat adalah metode iterasi Metode tidak langsung atau iterative, merupakan metode yang berbasiskan terhadap aplikasi dari langkah – langkah/algoritma sederhana yang diulang – ulang pada sistem persamaan tersebut hingga sistem persamaan mencapai keadaan konvergen yang merepresentasikan solusi dari sistem persamaan tersebut. Pada metode iterative, banyaknya langkah – langkah perhitungan yang dilakukan tidak dapat diprediksi, dimana tipikalnya adalah sebanyak N perhitungan per satu kali iterasi. Kekurangan lainnya adalah, jika sistem persamaan tidak berada pada kondisi yang kondusif, maka konvergensi dari suatu sistem persamaan tidak dapat terjamin. Satu – satunya kelebihan dari penggunaan metode iterative adalah sedikitnya memori computer yang digunakan sebagai akibat dari algoritma yang mendesain agar computer hanya menyimpan koefisien – koefisien yang tidak nol. Kelima adalah metode seccant, Pada dasarnya metode ini sama dengan metode Newton-Raphson, perbedaannya hanya terletak pada pendekatan untuk turunan pertama dari f saja.

MODUL 3: SISTEM PERSAMAAN LINIER DAN MATRIKS
Sistem persamaan linear merupakan salah satu materi yang memegang peranan penting dalam matematika. Sistem persamaan linear dapat digunakan oleh kehidupan kita sehari-hari. Sistem persamaan linear ini merupakan salah satu materi aljabar yang sangat berguna untuk memecahkan suatu masalah. Salah satu contoh materi dari sistem persamaan linear adalah menentukan koordinat titik potong dua garis, menentukan persamaan garis dan menentukan konstanta-konstanta pada suatu persamaan (Islamiyah et al., 2018). Terdapat beberapa materi atau metode yang dapat digunakan untuk menyelesaikan sistem persamaan linear menggunakan matriks. Metode-metode tersebut adalah:

Metode Gauss
Metode eliminasi Gauss termasuk dalam metode penyelesaian persamaan linear dengan cara langsung. Inti dari metode ini adalah membawa persamaan ke dalam bentuk matriks dan menyederhanakam matriks tersebut menjadi bentuk segitiga atas. Setelah mendapat bentuk segitiga atas, dilakukan substitusi balik untuk mendapat nilai dari akar persamaan tadi.

Metode Gauss-Jordan
Metode ini merupakan pengembangan dari metode eliminasi Gauss. Dimana tujuan kita membuat matriks identitas bukan lagi segitiga atas. Sehingga tidak diperlukan lagi substitusi balik untuk mencari nilai dari akar persamaan.

Metode Gauss-Seidel
Berbeda dengan dua metode yang sebelumnya, yaitu eliminasi Gauss dan Gauss-Jordan yang menggunakan matriks untuk menyelesaikan sistem persamaan. Metode Gauss-Seidel menggunakan metode Iterasi dalam menyelesaikan masalahnya. Metode ini dikembangkan dari gagasan penyelesaian masalah tak linear.

Metode Iterasi Jacobi
Metode ini merupakan suatu teknik penyelesaian SPL berukuran n x n; AX = b; secara iterative. Proses penyelesaian dimulai dengan suatu hampiran awal terhadap penyelesaian X. Teknik iterative jarang digunakan untuk menyelesaikan SPL dengan ukuran kecil karena metode-metode langsung seperti metode eliminasi Gauss lebih efisien daripada metode iterative. Tetapi, metode ini sangat berguna untuk menyelesaikan SPL dengan ukuran yang besar.

MODUL 4: INTEGRASI NUMERIK
Suatu cara yang digunakan untuk mengintegrasikan suatu persamaan di luar metode analitis. Integrasi numerik digunakan untuk mendapatkan nilai nilai hampiran dari beberapa integral tertentu yang memerlukan penyelesaian numerik sebagai hampirannya.

Metode Trapesium 1 Pias
Metode yang digunakan pada saat hanya terdapat dua data (f(a), f(b)) karena hanya dapat membentuk satu trapesium

Metode Trapesium Banyak Pias
Metode yang digunakan apabila tersedia data lebih dari dua, maka dapat dilakukan pendekatan dengan lebih dari satu trapesium dan luas total adalah jumlah dari trapesium – trapesium yang terbentuk

Metode Simpson 1/3
Mengasumsikan bahwa lengkungan dengan tiga ordinat berjarak sama y0, y1, y2 adalah suatu polinomial derajat dua

image

Metode Simpson 3/8
Mengasumsikan bahwa lengkungan dengan empat ordinat memiliki jarak sama, y0, y1, y2, y3 adalah suatu polinomila berderajat tiga

image

MODUL 5: PERSAMAAN DIFERENSIAL BIASA
Suatu persamaan disebut dengan persamaan differensial apabila mempunyaai bentuk differensial, misalnya 𝑑𝑦/𝑑𝑡 atau 𝑑𝑦/𝑑𝑥. Persamaan differensial biasa atau sering disebut juga dengan Ordinary Differential Equations (ODE) adalah persamaan differensial yang hanya memiliki satu variabel bebas. Metode yang dikembangkan untuk menyelesaikan persamaan diferensial biasa secara numerik (secara pendekatan karena penyelesaian secara analitis sulit untuk diperoleh), yang antara lain dapat dilakukan dengan dua metode yaitu metode satu-langkah (one-step) dan metode banyak-langkah (multi-step). Metode satu langkah terdiri dari beberapa metode, dimana dua diantaranya adalah metode Euler dan metode Heun..Metode Euler mempunyai ketelitian lebih rendah dari metode Heun namun metode ini cukup sederhana dan mudah pemahamannya. Metode Euler dapat diturunkan dari Deret Taylor. Metode ini pada dasarnya adalah merepresentasikan solusinya dengan beberapa suku deret Taylor. Misal, bentuk persamaan differensial berikut y’= f(x,y). Dengan menggunakan pendekatan nilai awal (x0,y0) maka nilai-nilainya berikutnya dapat diperoleh dengan: yn+1 = yn + h.f(xn, yn). Metode Heun merupakan perbaikan dari metode Euler tetapi memiliki iterasi lebih banyak dibandingkan dengan metode Euler. Metode Heun merupakan bentuk peningkatan dari metode Euler. Metode ini menaksir nilai y(tn+1) yang membutuhkan satu buah taksiran nilai sebelumnya yaitu y(tn). Metode ini melibatkan 2 buah persamaan, yaitu persamaan prediktor untuk memprediksi nilai integrasi awal dan persamaan korektor untuk mengoreksi hasil integrasi awal. Akurasi pada metode ini memang lebih baik karena metode ini melakukan koreksi ulang terhadap suati nilai koreksi menggunakan persamaan selanjutnya. Dari hasilnya dapat dibandingkan dan diamati bahwa metode Heun lebih baik dan efektif digunakan karena hasil perhitungannya lebih mendekati ke nilai asli dibandingkan dengan hasil dari metode Euler. Semua hasil metode Heun lebih mendekati ke hasil analitik dibandingkan dengan hasil dari metode Euler. Dari kurva-kurva yang ada pada kedua grafik juga dapat dilihat bahwa hasil pendekatan metode Heun lebih mendekati hasil analitik dibanding dengan hasil pendekatan metode Euler. Perbedaan keduanya memang cukup tipis, namun tetap saja, hasil metode Heun lebih medekati nilai aslinya. Galat metode Heun lebih kecil daripada metode Euler, berarti hasil perhitungannya semakin baik. Dengan demikian maka dapat disimpulkan bahwa baik dari hasil perhitungan maupun galatnya, metode yang paling baik digunakan adalah metode Heun. Adanya perbedaan hasil perhitungan dan nilai galat (error) ini dapat disebabkan oleh perbedaan prinsip perhitungan pada kedua metode ini.

DAFTAR PUSTAKA
Asadi, A. 2016. Python: The Complete Manual: The Essential Handbook for Python User. Imagine Publishing: West Midlands

Ermawati, E., Rahayu, P., & Zuhairoh, F. (2017). Perbandingan Solusi Numerik Integral Lipat Dua Pada Fungsi Aljabar Dengan Metode Romberg Dan Simulasi Monte Carlo. Jurnal MSA (Matematika dan Statistika serta Aplikasinya), 5(1), 46.

Faradillah, Ayu. 2020. Metode Numerik. Jakarta: Program Studi Pendidikan Matematika Fakultas Keguruan dan Ilmu Pendidikan UHAMKA.

Islamiyah, A. C., Prayitno, S., & Amrullah, A. (2018). Analisis Kesalahan Siswa SMP pada Penyelesaian Masalah Sistem Persamaan Linear Dua Variabel. Jurnal Didaktik Matematika, 5(1), 66-76.

Jami’in, M. A., Hidayat, E. P., Mujiono, U., Julianto, E., & Asmara, I. P. S. (2017, December). Analisa Data Hasil Pelatihan Pengukuran Kapal di Brondong dengan Pendekatan Fungsi Polinomial. In Seminar MASTER PPNS (Vol. 2, No. 1, pp. 181-186).

Morgan, P. 2016. Data Analysis From Scratch With Python. AI Sciences

Panjaitan, Melda. 2017. Pemahaman Meotde Numerik Menggunakan Pemograman MATLAB (Studi Kasus: Metode Secant). Jurnal Teknologi Informasi., 1(1).

Rachmad, Cahya, Deasy Sandhya E. I. dan Yan W. Syaifudin. 2017. Metode Numerik. Malang: Polinema Press.

Setiabudidaya, Dedi. 2018. Penggunaan Piranti Lunak Jupyter Notebook dalam Upaya Mensosialisasikan Open Science.

Sudiarta, I Wayan. 2020. Metode Numerik. Jakarta: Arga Puju Press.

https://docs.python.org/3/library/os.html

https://docs.python.org/3/library/sys.html

https://ipython.readthedocs.io/en/stable/overview.html

Saran Praktikum
Sebaiknya diberikan video tutorial agar praktikan lebih memahami
Sebaiknya penjelasan praktikum bisa diberikan dan diterangkan lebih rinci lagi karena materi dari metode numerik sendiri sangat kompleks dan sulit dipahami
Sebaiknya penjelasan mengenai library di phyton lebih diperjelas
Sebaiknya tugas yang telah diberikan dikoreksi bersama agar praktikan lebih mengerti letak kesalahannya
