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

  
