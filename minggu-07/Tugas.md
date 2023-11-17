# Menjalankan Container Docker yang Berisi Image Apache

## Prerequisites
1. docker
2. git
3. apache

## Langkah-langkah

1. jalankan docker,anda juga bisa mengecek apakah sudah berjalan atau belum dengan perintah berikut:
   ```
   docker ps
   ```
   Jika docker sudah berstatus Running, maka ia akan memiliki tampilan seperti gambar di bawah ini

   ![list container](./12-docker-ps.jpg)
3. selanjutnya lakukan pull image Apache dengan perintah berikut di cmd:
   ```
   docker pull httpd
   ```
   Jika pull image Apache sudah selesai maka tampilan akan terlihat seperti berikut:

   ![pull selesai](./13-docker-pull-httpd.jpg)
   
5. lihat list image docker dengan perintah berikut :
    ```
    docker images
    ```

    ![list docker image](./08-docker-images-list.jpg)

6. lalu run countainer dengan perintah berikut :
    ```
    docker run -d --name arnesa-apache -p 81:80 -d httpd
    ```

    maka tampilan akam menjadi seperti berikut

    ![tampilan countainer](./09-docker-run-image-httpd.jpg)

7. Cek Browser Untuk Melihat Keberhasilan Menjalankan Docker dengan mengaksesnya melalui perintah berikut di browser anda :
   ```
   http://localhost:81
   ```

   sesuaikan dengan nama ip server : port anda,jika behasil maka akan muncul tampilan seprti berikut

   ![httpd berhasil](./10-docker-localhost-81.jpg)


selesai.


