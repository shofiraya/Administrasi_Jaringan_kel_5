<h1 align="Center">LAPORAN WORKSHOP ADMINISTRASI JARINGAN</h1>


<p align="center">
  <img src="assets/Logo_PENS.png" alt="Logo PENS">
</p>

<h4 align="Center">Disusun oleh:</h4>

<h4 align="center">
Nama : Shofira Izza Nurrohmah <br>
NRP : 3122500026 <br>
Kelas: 2 D3 IT A <br>
</h4>

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

<h4>Bagaimana Cara kerja dari iterative dan recursive dari DNS Query? Ada 8 step, dari PC anda! Misal akses detik.com</h4>

1. Pengguna mengetikkan 'detik.com' ke dalam web browser dan query tersebut dikirim ke Internet dan diterima oleh resolver DNS rekursif yang bertugas mencari alamat IP terkait dengan nama domain tersebut.
2. Resolver kemudian melakukan query ke sebuah server nama root DNS (.) untuk meminta informasi tentang domain yang diminta. Server nama root DNS menyimpan informasi tentang lokasi server DNS untuk setiap TLD (Top Level Domain).

3. Setelah menerima kueri dari resolver, server root kemudian memberikan respons kepada resolver dengan alamat dari sebuah server DNS Top Level Domain (TLD) (seperti .com atau .net), yang menyimpan informasi untuk domain-domain di bawahnya. Saat mencari detik.com, permintaan diarahkan ke TLD .com.

4. Resolver kemudian membuat permintaan query ke server DNS yaitu TLD .com untuk mendapatkan informasi lebih lanjut tentang domain detik.com.

5. Server TLD kemudian memberikan respons dengan alamat IP dari nameserver yang bertanggung jawab atas domain, detik.com.

6. Resolver DNS rekursif mengirimkan query ke nameserver domain detik.com untuk mendapatkan alamat IP akhir untuk domain yang diminta.

7. Nameserver domain memberikan respons dengan alamat IP untuk domain example.com kepada resolver DNS rekursif.

8. Setelah semua langkah pencarian DNS selesai dan alamat IP untuk detik.com ditemukan, resolver DNS memberikan respons kepada web browser dengan alamat IP tersebut. 

Sehingga browser dapat melakukan permintaan untuk halaman web. Setelah langkah-langkah pencarian DNS selesai, browser dapat membuat permintaan HTTP ke alamat IP dan server di alamat IP tersebut mengembalikan halaman web yang akan dirender di browser.

<img src="https://cf-assets.www.cloudflare.com/slt3lc6tev37/1NzaAqpEFGjqTZPAS02oNv/bf7b3f305d9c35bde5c5b93a519ba6d5/what_is_a_dns_server_dns_lookup.png" alt="Logo PENS">


<h4>Perbedaan antara rekursi dan iterasi</h4>
Dua metode yang berbeda dalam ilmu komputer untuk menyelesaikan masalah. Rekursi merupakan program yang secara berulang memanggil dirinya sendiri sampai suatu kondisi terpenuhi, sementara iterasi merupakan serangkaian instruksi diulang sampai suatu kondisi terpenuhi.

Dalam pencarian rekursif, server DNS melakukan rekursi dan terus meminta server DNS lainnya sampai ia memiliki alamat IP untuk dikembalikan kepada klien. Dalam kueri DNS iteratif, setiap kueri DNS merespons langsung kepada klien dengan alamat untuk server DNS lain yang harus ditanyai, dan klien terus meminta server DNS sampai salah satu dari mereka merespons dengan alamat IP yang benar untuk domain yang diberikan.

Pemisalan: <br>
Agung kehilangan kuncinya di rumah dan mencari cara sistematis untuk menemukannya. 
- Solusi rekursif akan membuat Agung terus mencari kunci sampai dia menemukannya. Agung akan mulai mencari, dan jika dia tidak menemukan kuncinya, dia akan kembali ke instruksi awalnya untuk terus mencari hingga menemukannya. 
- Solusi iteratif membuat Agung mencari satu ruangan selama lima menit, kemudian kembali ke instruksinya dan mencari ruangan berikutnya selama lima menit, dan melanjutkan siklus ini sampai dia menemukan kunci atau telah melalui daftar ruangan yang akan diperiksa.



Sumber pustaka:
1. https://www.cloudflare.com/learning/dns/what-is-dns/
2. https://www.cloudflare.com/learning/dns/what-is-recursive-dns/
