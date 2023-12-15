# Docker Orchestration Hands-on Lab

##  What is Orchestration?
Jadi, apa sebenarnya Orkestrasi itu? Ya, Orkestrasi mungkin paling baik dijelaskan dengan menggunakan sebuah contoh. Katakanlah Anda memiliki aplikasi yang memiliki lalu lintas tinggi dan persyaratan ketersediaan tinggi. Karena persyaratan ini, Anda biasanya ingin menerapkan setidaknya di 3+ ​​mesin, sehingga jika sebuah host gagal, aplikasi Anda masih dapat diakses dari setidaknya dua mesin lainnya. Tentu saja, ini hanyalah sebuah contoh dan kasus penggunaan Anda kemungkinan besar memiliki persyaratannya sendiri, tetapi Anda mengerti maksudnya.

Menyebarkan aplikasi Anda tanpa Orkestrasi biasanya sangat memakan waktu dan rawan kesalahan, karena Anda harus melakukan SSH secara manual ke setiap mesin, memulai aplikasi Anda, dan terus mengawasi berbagai hal untuk memastikan aplikasi berjalan sesuai harapan.

Namun, dengan peralatan Orkestrasi, Anda biasanya dapat melepaskan sebagian besar pekerjaan manual ini dan membiarkan otomatisasi melakukan pekerjaan berat. Salah satu fitur keren Orkestrasi dengan Docker Swarm adalah Anda dapat menerapkan aplikasi di banyak host hanya dengan satu perintah (setelah mode Swarm diaktifkan). Selain itu, jika salah satu node pendukung mati di Docker Swarm Anda, node lain akan secara otomatis mengambil beban, dan aplikasi Anda akan terus berjalan seperti biasa.

## 1. Configure Swarm Mode
```
docker run -dt ubuntu sleep infinity
```
Perintah ini akan membuat container baru berdasarkan gambar ubuntu:latest dan akan menjalankan perintah sleep agar container tetap berjalan di latar belakang.

