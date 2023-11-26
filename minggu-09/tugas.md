## Prerequisites

1. clone dari GitHub repo
   
   Gunakan perintah berikut untuk mengkloning repo lab dari GitHub
   ```
    git clone https://github.com/dockersamples/linux_tweet_app
   ```
2. DockerID

   Pastikan Anda memiliki DockerID,Jika Anda tidak memiliki DockerID (login gratis yang digunakan untuk mengakses Docker Hub), silakan     kunjungi Docker Hub dan daftar untuk mendapatkannya. Anda akan memerlukan ini untuk langkah selanjutnya.


## menjalankan container Docker sederhana

1. jalankan docker desktop anda
2. gunakan perintah berikut ini di cmd
   ```
   docker container run alpine hostname
   ```
   ![alpine hostname](./)

3. lalu lihat Daftar semua kontainer
   ```
   docker container ls --all
   ```
   ![ls --all](./)

   ID penampung adalah nama host yang ditampilkan penampung. Dalam contoh di atas itu `3530ce937f9a`.

5. 
