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
   ![alpine hostname](./2-run-alpine-hostname.jpg)

3. lalu lihat Daftar semua kontainer
   ```
   docker container ls --all
   ```
   ![ls --all](./3-ls-all.jpg)

   ID penampung adalah nama host yang ditampilkan penampung. Dalam contoh di atas itu `3530ce937f9a`.


## Run an interactive Ubuntu container

Anda dapat menjalankan container berdasarkan versi Linux yang berbeda dengan yang dijalankan pada host Docker Anda.disini kita akan menjalankan container Ubuntu Linux di atas host Alpine Linux Docker (Play With Docker menggunakan Alpine Linux untuk nodenya).

1. Jalankan container Docker dan akses shellnya.
   ```
    docker container run --interactive --tty --rm ubuntu bash
   ```
   
   ![ubuntu bash](./4-ubuntu-bash.jpg)


## Run a background MySQL container

1. Jalankan wadah MySQL baru dengan perintah berikut.

   ```
   docker container run \
    --detach \
    --name mydb \
    -e MYSQL_ROOT_PASSWORD=my-secret-pw \
    mysql:latest
   ```
   ![background MySQL container](./8-mydb.jpg)

2. Buat daftar container yang sedang berjalan.

   ```
   docker container ls
   ```
   Perhatikan kontainer Anda sedang berjalan.
   ![container ls](./9-container-ls.jpg)

3. periksa apa yang terjadi di container Anda dengan menggunakan beberapa perintah Docker bawaan: `docker container logs` dan `docker container top`.
   ```
   docker container logs mydb
   ```
   Ini menunjukkan log dari kontainer MySQL Docker.
   ![logs mydb](./11-logs-mydb-1.jpg)
   ![logs mydb 2](./11-logs-mydb-2.jpg)

4. Daftar versi MySQL menggunakan `docker container exec`.
   ```
    docker exec -it mydb \
    mysql --user=root --password=$MYSQL_ROOT_PASSWORD --version
   ```
   Anda akan melihat nomor versi MySQL.
   ![exec -it mydb](./12-exec-it-mydb.jpg)

5. Ketik `exit` untuk keluar dari sesi shell interaktif.
   ```
   exit
   ```

## Task 2: Package and run a custom app using Docker

====================================================================================
### Bangun gambar situs web sederhana

1. Pastikan Anda berada di `linux_tweet_app` direktori.
   ```
   cd ~/linux_tweet_app
   ```

2. Menampilkan konten Dockerfile.
   ```
   cat Dockerfile
   ```
   atau anda juga bisa ubah lewat text editor sebagai berikut:

   ```
   FROM nginx:latest

    COPY index.html /usr/share/nginx/html
    COPY linux.png /usr/share/nginx/html

    EXPOSE 80 443     

    CMD ["nginx", "-g", "daemon off;"]
   ```

3. Untuk membuat perintah berikut lebih ramah salin/tempel, ekspor variabel lingkungan yang berisi DockerID Anda (jika Anda tidak     memiliki DockerID, Anda bisa mendapatkannya secara gratis melalui Docker Hub ).

   Anda harus mengetikkan perintah ini secara manual karena memerlukan DockerID unik Anda.

   `export DOCKERID=<your docker id>`

4. Echo nilai variabel kembali ke terminal untuk memastikannya disimpan dengan benar.
   ```
   echo $DOCKERID
   ```
   ![DOCKERID](./)

5. Gunakan `docker image build` perintah untuk membuat image Docker baru menggunakan instruksi di Dockerfile.
   ```
   docker image build --tag $DOCKERID/linux_tweet_app:1.0 .
   ```

   Output di bawah ini menunjukkan daemon Docker yang mengeksekusi setiap baris di Dockerfile

   ![output Dockerfile](./)

   
6. Gunakan `docker container run` perintah untuk memulai wadah baru dari gambar yang Anda buat.
   ```
   docker container run \
   --detach \
   --publish 80:80 \
   --name linux_tweet_app \
   $DOCKERID/linux_tweet_app:1.0
   ```
   Lalu lintas eksternal apa pun yang masuk ke server pada port 80 sekarang akan diarahkan ke kontainer pada port 80.

   Pada langkah selanjutnya Anda akan melihat cara memetakan lalu lintas dari dua port berbeda - ini diperlukan ketika dua            kontainer menggunakan port yang sama untuk berkomunikasi karena Anda hanya dapat mengekspos port tersebut satu kali pada host.

   ![container_port](./)

7. Setelah Anda mengakses situs web Anda, matikan dan hapus.
   ```
   docker container rm --force linux_tweet_app
   ```
   ![tampilan situs](./)


## Task 3: Modify a running website

### Mulai aplikasi web kami dengan bind mount

1. -
2. -
   ...
   
   

