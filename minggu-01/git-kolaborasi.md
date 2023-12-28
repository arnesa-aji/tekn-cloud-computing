# Git untuk Kolaborasi

## Fork

Fork adalah membuat clone dari suatu repo di GitHub milik *upstream author*, diletakkan ke milik kontributor. Fork hanya dilakukan sekali saja. Pada dasarnya, proses untuk fork ini meliputi:

1. Fork repo di web GitHub.
2. Clone fork tersebut di komputer lokal.

Kontributor harus mem-*fork* repo *upstream author* sehingga di repo kontributor muncul repo tersebut. Proses *forking* ini dijelaskan dengan langkah-langkah berikut:

1. Login ke GitHub
2. Akses repo yang akan di-*fork*
3. Pada sisi kanan atas, klik Fork:
4. Pilih akan ditempatkan di account mana.
5. Setelah proses, repo dari *upstream author* sudah berada di account GitHub kita (kontributor)

Setelah proses tersebut, clone di komputer lokal:

```bash
$ git clone https://github.com/bpdp/playground-1
Cloning into 'playground-1'...
remote: Enumerating objects: 3, done.
remote: Counting objects: 100% (3/3), done.
remote: Compressing objects: 100% (2/2), done.
remote: Total 3 (delta 0), reused 3 (delta 0), pack-reused 0
Unpacking objects: 100% (3/3), done.
zaky@dellvuan:~$ ls -la playground-1/
total 16
drwxr-xr-x 3 zaky zaky 4096 Jan 21 11:31 .
drwxr-xr-x 3 zaky zaky 4096 Jan 21 11:31 ..
drwxr-xr-x 8 zaky zaky 4096 Jan 21 11:31 .git
-rw-r--r-- 1 zaky zaky   81 Jan 21 11:31 README.md
$
```

Setelah itu, konfigurasikan repo lokal kontributor. Pada kondisi saat ini, di komputer lokal sudah terdapat repo `playground-1` yang berada pada direktori dengan nama yang sama. Untuk keperluan berkontribusi, ada 2 nama repo yang harus diatur:
  1. **origin**: menunjuk ke repo milik kontributor di GitHub, hasil dari fork.
  2. **upstream**: menunjuk ke repo milik *upstream* author (repo asli) di account *oldstager*.

Repo `origin` sudah dituliskan konfigurasinya pada saat melakukan proses clone dari repo kontributor. Konfigurasi repo *upstream* harus dibuat.

```bash
$ git remote -v
origin	https://github.com/bpdp/playground-1 (fetch)
origin	https://github.com/bpdp/playground-1 (push)
$
```

Tambahkan remote upstream:

```
$ git remote add upstream https://github.com/oldstager/playground.git
```

Hasil:

```
$ git remote -v
origin	https://github.com/bpdp/playground-1 (fetch)
origin	https://github.com/bpdp/playground-1 (push)
upstream	https://github.com/oldstager/playground.git (fetch)
upstream	https://github.com/oldstager/playground.git (push)
$
```
