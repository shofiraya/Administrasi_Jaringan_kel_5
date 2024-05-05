<h1 align="Center">LAPORAN WORKSHOP ADMINISTRASI JARINGAN</h1>

<h2 align="Center">WEB EMAIL SYSTEM SERVER</h2>


<p align="center">
  <img src="assets/Logo_PENS.png" alt="Logo PENS">
</p>

<h4 align="Center">Disusun oleh:</h4>

<h4 align="Center">Anggota Kelompok 5</h4>

<p align="center">
1. Arsyita Devanaya Arianto (3122500008) <br>
2. Mirta Chadhirotin Nachlah (3122500009) <br>
3. Shofira Izza Nurrohmah (3122500026)
</p>

<br>
<h4 align="center">
Dosen Pengampu : Dr Ferry Astika Saputra ST, M.Sc	
</h4>

<br>
<h4 align="center">
PROGRAM STUDI TEKNIK INFORMATIKA <br>
DEPARTEMEN TEKNIK INFORMATIKA DAN KOMPUTER 
POLITEKNIK ELEKTRONIKA NEGERI SURABAYA <br> 
2024
</h4> <br><br><hr>


### Pengertian Web Server & Web Client
   Web client dan Web server berkomunikasi menggunakan protokol HTTP (HyperText Transfer Protocol). 
   - Web server adalah komputer yang tergabung dalam jaringan atau internet yang **memberikan** informasi.
   - Web client adalah komputer yang tergabung dalam jaringan atau internet yang **meminta** informasi. Untuk dapat mengakses web server, web client menggunakan aplikasi yang disebut Web browser. 

### Cara kerja Web Server

   ![alt text](assets/carakerja.png) <br>

1. Client melakukan permintaan untuk mengakses sebuah domain Uniform Resource Locator (URL) yang diketikkan pada address bar di sebuah browser
2. Permintaan tersebut dikirim ke server penyedia DNS.
3. Bila halaman web tersebut menggunakan database programming, maka akan dihubungkan dengan database server
4. Apabila domain pada URL tersebut ada di web server, maka web server akan segera melakukan respon, dengan menampilkan web yang diinginkan.
5. Apabila domain pada URL tersebut tidak ada, maka akan muncul informasi "Page Not Found" artinya halaman tidak ditemukan.
6. Pengiriman permintaan web dari client tersebut akan didelegasikan melalui DNS server.
7. Demikian seterusnya, karena setiap perangkat terhubung ke internet dan memiliki spesifikasi yang baik, juga dengan koneksi internet yang cukup, maka proses permintaan web tidak akan berlangsung lama.


### Cara kerja Web Client

   ![alt text](assets/carakerja2.png) <br>

1. Client dapat membangun sebuah halaman web berdasarkan database yang dimiliki, dengan menggunakan perangkat keras (hardware) dan software. Sehingga, menghasilkan tampilan atau UI tertentu. 
2. Server dapat mempengaruhi UI. Server web menerima permintaan dan menyimpan UI web tersebut berupa dokumen HTML. 
3. Client yang meminta akses informasi, dalam hal ini adalah pengguna, maka server akan mengirimkan dokumen HTML tersebut. Hasilnya informasi tampil di browser dan kamu dapat membacanya dengan tampilan UI yang menarik dan mudah dimengerti. 
4. Ketika client (pengguna) sudah mendapatkan informasinya, maka client akan memeriksa kode program atau sintaks. Proses ini menghasilkan database yang diperlukan. Proses ini menggunakan bahasa pemrograman SQL atau sejenisnya. 
5. Proses tersebut diteruskan ke server, sambil menunggu server mendapat respons dari pengguna akhir. Ketika pengguna merespons, permintaan database dibuat untuk client dan hasilnya tayang di layar kamu. 
