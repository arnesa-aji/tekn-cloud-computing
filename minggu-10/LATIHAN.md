# Section #1 - Networking Basics

## Bagian #1 - Dasar-Dasar Jaringan

- Perintah tersebut docker networkmerupakan perintah utama untuk mengkonfigurasi dan mengelola jaringan kontainer. Jalankan perintah `docker network` dari terminal
   ```
   docker network
   ```
   ![docker network](./01-docker-network.jpg)

## Langkah 2: Buat daftar jaringan
- Jalankan perintah `docker network ls` untuk melihat jaringan kontainer yang ada di host Docker saat ini.
  ```
  docker network ls
  ```
  ![docker network ls](./02-docker-network-ls.jpg)

## Langkah 3: Periksa jaringan
- lalu jalankan perintah :
  ```
  docker network inspect bridge
  ```
  ![docker network inspect bridge](./03-docker-network-inspect-bridge.jpg)

## Langkah 4: Buat daftar plugin driver jaringan
- Jalankan perintah `docker info` dan temukan daftar plugin jaringan.
  ```
  docker info
  ```
  ![docker info](./04-docker-info.jpg)



  # Section #2 - Bridge Networking
  
  ## Langkah 1: Dasar-dasar
  - Setiap instalasi Docker yang bersih dilengkapi dengan jaringan siap pakai yang disebut bridge . Verifikasi ini dengan `docker network ls`.
    ```
    docker network ls
    ```
    ![docker net ls](./02-docker-network-ls.jpg)

Output di atas menunjukkan bahwa jaringan jembatan dikaitkan dengan driver jembatan . Penting untuk dicatat bahwa jaringan dan driver terhubung, tetapi keduanya tidak sama. Dalam contoh ini jaringan dan driver memiliki nama yang sama - namun keduanya bukanlah hal yang sama!

Output di atas juga menunjukkan bahwa jaringan jembatan dicakup secara lokal. Artinya jaringan hanya ada di host Docker ini. Hal ini berlaku untuk semua jaringan yang menggunakan driver bridge - driver bridge menyediakan jaringan host tunggal.

Semua jaringan yang dibuat dengan driver jembatan didasarkan pada jembatan Linux (alias saklar virtual).

Instal brctlperintah dan gunakan untuk membuat daftar jembatan Linux di host Docker Anda. Anda dapat melakukan ini dengan menjalankan sudo apt-get install bridge-utils.
```
apk update
apk add bridge
```
![apk update](./images/05-apk-update.jpg)
Kemudian, daftarkan jembatan pada host Docker Anda, dengan menjalankan `brctl show`.
```
brctl show
```
![brctl](./images/06-brctl-show.jpg)

   ## Langkah 2: Hubungkan kontainer

   - Buat wadah baru dengan menjalankan `docker run -dt ubuntu sleep infinity`.
     ```
     docker run -dt ubuntu sleep infinity
     ```
     ![-dt ubuntu](./images/08-ubuntu-sleep-infinity-.jpg)
  
   - Anda dapat memverifikasi bahwa wadah contoh kami sudah aktif dengan menjalankan `docker ps`
     ![docker ps](./images/09-docker-ps-.jpg)
   - Jalankan `brctl show` perintah lagi.
     ![brctl show](./images/10-brctl-show.jpg)

     ## Langkah 3: Uji konektivitas jaringan
     - Ping alamat IP wadah dari prompt shell host Docker Anda dengan menjalankan `ping -c5 <IPv4 Address>`. Ingatlah untuk menggunakan IP wadah di lingkungan Anda .
       ![ping](./images/12-ping.jpg)
     - Pertama, kita perlu memulai ID container pada langkah sebelumnya. Anda bisa lari docker psuntuk mendapatkannya.
       ```
       docker ps
       ```
       ![docker ps](./images/13-docker-ps.jpg)
     - Selanjutnya, mari kita jalankan shell di dalam container ubuntu tersebut, dengan menjalankan docker exec -it <CONTAINER ID> /bin/bash
       ![bash](./images/14-docker-ecec-it.jpg)
     - Selanjutnya kita perlu menginstal program ping. Jadi, ayo lari `apt-get update && apt-get install -y iputils-ping`.
       ```
       apt-get update && apt-get install -y iputils-ping
       ```
     - Mari kita ping ke www.github.com dengan menjalankan `ping -c5 www.github.com`
       ![ping](./images/16-ping-github.jpg)
     - Terakhir, lepaskan shell kita dari container, dengan menjalankan exit.
       ```
       exit
       ```
       ## Langkah 4: Konfigurasikan NAT untuk konektivitas eksternal
       

       
       
       
