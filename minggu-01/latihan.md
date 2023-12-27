## latihan 1

### 1. Instalasi Git
#### instal Git di Windows

Sebelum install Git di Windows, anda harus sudah mempunyai editor teks yang didukung oleh Windws. Editor yang bisa dipilih banyak, tetapi disarankan menggunakan Notepad++ atau Visual Studion Code atau Vim. Keberadaan editor teks ini akan menentukan keberhasilan instalasi
1. Setelah download [Git](https://git-scm.com/download/win), double click pada file yang di-download. Akan dimunculkan lisensi. Klik Next untuk lanjut.
2. Setelah itu, pilih lokasi instalasi. Secara default akan terisi C:\Program Files\Git. Ganti lokasi jika memang anda menginginkan lokasi lain, klik Next
3. Pilih komponen. Tidak perlu diubah-ubah, sesuai dengan default saja. Klik pada Next.
4. Mengisi shortcut untuk menu Start. Gunakan default (Git), ganti jika ingin mengganti - misalnya Git VCS.
5. Pilih editor yang akan digunakan bersama dengan Git.
6. Pada saat instalasi, Git menyediakan akses git melalui Bash maupun command prompt. Pilih pilihan kedua supaya bisa menggunakan dari dua antarmuka tersebut. Bash adalah shell di Linux. Dengan menggunakan bash di Windows, pekerjaan di command line Windows bisa dilakukan menggunakan bash - termasuk ekskusi dari Git.
7. Pilih OpenSSL untuk HTTPS. Git menggunakan https untuk akes ke repo GitHub atau repo-repo lain (GitLab, Assembla).
8. Pilih pilihan pertama untuk konversi akhir baris (CR-LF).
9. Pilih PuTTY untuk terminal yang digunakan untuk mengakses Git Bash.
10. Untuk opsi ekstra, pilih serta aktifkan 1 dan 2.
11. Setelah itu proses instalasi akan dilakukan.
12. Jika selesai akan muncul dialog pemberitahuan. Klik pada Finish.
13. Untuk menjalankan, dari Start menu, ketikkan "Git", akan muncul beberapa pilihan. Pilih "Git Bash" atau "Git GUI".
14. Tampilan jika akan menggunakan "Git Bash"

    ![git bash](./git-bash.jpg)
15. Tampilan jika akan menggunakan "Git GUI"

    ![git gui](./git-gui.jpg)

16. Untuk mencoba dari command prompt, masuk ke command prompt, setelah itu eksekusi `git --version` untuk melihat apakah sudah terinstall atau belum. Jika sudah terinstall dengan benar, makan akan muncul hasil berikut:
    ![git --version](./gambar-01-latihan.jpg)

17. selesai.

    

### 2. Konfigurasi Git
Secara minimal, user harus memberitahu Git tentang username serta email yang digunakan setiap kali terjadi perubahan pada repo Git. Username serta email ini yang akan dimasukkan oleh Git ke catatan perubahan di repo. Di sistem operasi Linux atau sejanis (UNIX), konfigurasi ini nantinya akan disimpan di $HOME/.gitconfig. Untuk sistem operasi Windows, konfigurasi ini akan disimpan di C:\Document and Settings\NamaUser dengan nama file .gitconfig. Secara minimal, ada 2 hal yang perlu dikonfigurasi yaitu username dan email. Gunakan perintah berikut:

```
$ git config --global user.name "Nama Anda di GitHub"
$ git config --global user.email email@domain.tld
```

Isian di atas harus disesuaikan dengan nama serta email yang digunakan untuk mendaftar di GitHub. Untuk melihat konfigurasi yang sudah ada:

```
$ git config --list
user.email=phylossophie@gmail.com
user.name=Bambang Purnomosidi D. P.
color.ui=true
```

![config-git](./gambar-02-latihan.jpg)

Langkah ini cukup dilakukan sekali saja, kecuali jika ingin melakukan perubahan nama dan email.




03-mengelola-repo : https://github.com/arnesa-aji/tekn-cloud-computing/tree/master/minggu-01

git-single.md : https://github.com/arnesa-aji/tekn-cloud-computing/blob/master/minggu-01/git-single.md


## latihan 2

### rangkuman-cloud-computing.md : https://github.com/arnesa-aji/tekn-cloud-computing/blob/master/minggu-01/rangkuman-cloud-computing.md

