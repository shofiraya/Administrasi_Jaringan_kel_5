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


<h3>Containerization</h3>

1. <h4>Before Install Docker Engine, Uninstall Conflicted</h4>
- `for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done`
![alt text](assets/uninstall.png)

2. <h4>Install Docker Engine</h4>

- Add Docker's official GPG key: 
- `sudo apt-get update`

- `sudo apt-get install ca-certificates curl`

- `sudo install -m 0755 -d /etc/apt/keyrings`

- `sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc`

- `sudo chmod a+r /etc/apt/keyrings/docker.asc`
![alt text](assets/install.png)
![alt text](assets/install2.png)

- <h5>Add the repository to Apt sources:</h5>
`echo \`

`"deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \`

` $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \`

`sudo tee /etc/apt/sources.list.d/docker.list > /dev/null`

`sudo apt-get update`
![alt text](assets/install2.png)

3. <h4>Install Docker Packages</h4>
`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`
![alt text](assets/install3.png)

4. <h4>Start Docker Engine</h4>
`sudo service docker start`
![alt text](assets/install4.png)

5. <h4>Run a Container</h4>
Command : docker run [image-name]
`sudo docker run hello-world`
![alt text](assets/runhelloworld.png)


<h4>Menjalankan project docker-example dari github</h4>

1. Clone dari github
`git clone https://github.com/alfiyansys/docker-examples.git`
![alt text](assets/gitcloneexample.png)

2. Build ke dalam docker images
`docker build -t example`
![alt text](assets/build.png)

3. Menjalankan docker images
`docker run -p 3000:80 example`
![alt text](assets/runexample.png)

4. Buka port berikut pada browser
http://localhost:3000
![alt text](assets/cekexample.png)

<h4></h4>

1. Run Uptime-Kuma monitoring service using docker: https://github.com/louislam/uptime-kuma
    - `docker run -d --restart=always -p 3001:3001 -v uptime-kuma:/app/data --name uptime-kuma louislam/uptime-kuma:1`
    ![alt text](assets/runuptime.png)

    - Pengecekan pada port 3000
    `http://localhost:3000`
    ![alt text](assets/cekuptime.png)

2. Run using virtualhost with access domain, example: http://monitoring.kelompokX.local 

- Konfigurasi file db.kelompok5.local
-  > Menambahkan monitoring pada CNAME ns
`sudo nano /var/lib/bind/db.kelompok5.local`
![alt text](assets/konfignamed.png)
`sudo systemctl restart named`

- Install a2enmod
`sudo a2enmod`
![alt text](assets/a2enmod.png)
![alt text](assets/a2enmod1.png)
Memasukkan package proxy
`proxy proxy_ajp proxy_http rewrite deflate headers proxy_balancer proxy_connect proxy_html`

- Konfigurasi Apache2
`sudo nano /etc/apache2/sites-enabled/000-default.conf`
![alt text](assets/konfigapache2.png)
Menambahkan beberapa baris untuk monitoring subdomain dengan proxy
`sudo systemctl restart apache2`

- Cek dengan browser
![alt text](assets/monitoring.png)