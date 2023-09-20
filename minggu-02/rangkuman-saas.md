Secara ringkas, perbedaan antara model-model ini terletak pada tingkat kendali dan tanggung jawab manajemen Anda terhadap infrastruktur dasarnya



1. IaaS (Infrastructure as a Service): Dalam model ini, Anda memperoleh bahan mentah (sumber daya komputasi, disk penyimpanan, OS) dari Penyedia Layanan Cloud (CSP). Anda memiliki kendali atas konfigurasi OS Anda, pemutakhiran (patching), dan beban kerja yang dijalankan pada lingkungan Anda. Ini mirip dengan membeli bahan untuk membuat pizza di rumah, di mana Anda mengendalikan proses memasak tetapi tidak mengendalikan infrastrukturnya.



2. PaaS (Platform as a Service): PaaS mirip dengan membeli pizza dari sumber eksternal dan menikmatinya di rumah. Anda tidak perlu khawatir tentang mengkonfigurasi basis data, penyeimbang beban, dll. Ini adalah layanan yang dikelola yang disediakan oleh CSP Anda. Anda fokus pada membangun dan mendeploy aplikasi Anda, mengurangi tingkat kendali Anda dibandingkan dengan IaaS.



3. SaaS (Software as a Service): Dalam model ini, penyedia layanan Anda mengelola sebagian besar aspek, dan persyaratan konfigurasi atau pengaturan Anda sangat minimal. Ini mirip dengan memesan pizza yang sudah jadi dari restoran; Anda memiliki sangat sedikit kendali atas bahan atau proses memasak.


4. Control Gradation: Saat Anda bergerak dari kiri ke kanan dalam diagram ini, tingkat kendali Anda terhadap sumber daya cloud semakin berkurang. Anda memiliki kendali tertinggi dalam IaaS, diikuti oleh PaaS, dan kendali paling sedikit dalam SaaS.


====================================================


SAAS (Software as a Service) Platform Architecture


SAAS, atau Perangkat Lunak sebagai Layanan, adalah model lisensi dan pengiriman perangkat lunak yang di lisensikan berdasarkan langganan dan di-host secara sentral. Pengguna dapat mengaksesnya melalui peramban web. Ini adalah model pengiriman umum untuk banyak aplikasi bisnis, termasuk perangkat lunak kantor, perangkat lunak manajemen, virtualisasi, dll. SAAS adalah bagian dari terminologi komputasi awan, bersama dengan infrastruktur sebagai layanan (IaaS), platform sebagai layanan (PaaS), dan desktop sebagai layanan (DaaS). Ini terkait dengan penyedia layanan aplikasi (ASPs) yang menyediakan aplikasi siap pakai kepada pengguna bisnis melalui Internet.

SAAS memiliki arsitektur tunggal, multi-penyewa, yang menyediakan pengalaman berfitur kompetitif dengan aplikasi on-premise. Arsitek aggregator menggabungkan penawaran SAAS dari berbagai vendor dan menawarkannya sebagai bagian dari platform aplikasi yang terpadu. Penyedia SAAS meng-host aplikasi dan data secara sentral, menyediakan pemutakhiran dan patching aplikasi secara transparan, memberikan akses kepada pengguna akhir melalui Internet, dan menyediakan berbagai mekanisme keamanan untuk menjaga keamanan data selama transmisi dan penyimpanan.

Arsitektur SAAS mencakup penggunaan satu versi aplikasi dengan konfigurasi tunggal untuk semua pelanggan. Aplikasi diinstal di beberapa mesin untuk mendukung skalabilitas. Ada dua varietas utama SAAS: SAAS Vertikal yang menjawab kebutuhan industri tertentu dan SAAS Horizontal yang fokus pada kategori perangkat lunak tertentu tanpa batasan industri.

Manfaat SAAS termasuk mengurangi risiko akuisisi perangkat lunak, menghilangkan kebutuhan infrastruktur di lokasi pelanggan, dan memungkinkan integrasi yang mudah. Ini juga memungkinkan uji coba perangkat lunak dengan risiko minimal sebelum pembelian. Sementara SAAS membawa manfaat, pengguna perlu mempertimbangkan keamanan data, kebutuhan pelaporan, dan dampaknya pada peran dan tanggung jawab IT saat beralih ke model ini.

Pada akhirnya, penggunaan SAAS membawa fleksibilitas dan manajemen risiko, dan integrasi dengan arsitektur yang ada adalah kunci keberhasilannya sebagai bagian dari infrastruktur TI berbasis layanan.

Jadi, SAAS adalah model pengiriman perangkat lunak yang dapat memudahkan akses dan pengelolaan perangkat lunak melalui Internet, dengan banyak manfaat yang mungkin untuk organisasi.



========================================================



Apa itu Software as a Service SaaS Architecture

SaaS adalah cara untuk mengirimkan perangkat lunak, penyedia perangkat lunak secara terpusat menghosting satu atau lebih aplikasi dan membuatnya tersedia untuk pelanggan melalui internet. Arsitektur SaaS juga merupakan salah satu pilar utama cloud computing.
Ledakan dalam komputasi Cloud, yang didorong oleh penyedia layanan cloud seperti Microsoft dengan Azure, Amazon Web Services (AWS), Oracle, dan IBM, telah menyebabkan pertumbuhan pada produk dan layanan lain yang disampaikan melalui internet.
Setiap pembaruan atau patch pada aplikasi arsitektur SaaS semuanya ditangani oleh penyedia. Pelanggan tidak perlu mengunduh pemutakhiran atau menginstal ulang versi baru suatu produk karena perangkat lunak dikirimkan melalui internet.
Mengapa Menggunakan Arsitektur SaaS,Dari sudut pandang konsumen, aplikasi SaaS adalah salah satu cara termudah dan paling dapat diandalkan untuk menggunakan layanan atau produk digital.Dari perspektif bisnis, produk perangkat lunak yang diberikan “sebagai layanan” memungkinkan perusahaan untuk menawarkan produk mereka dalam skala besar dan global.

Setiap pembaruan atau patch pada aplikasi arsitektur SaaS semuanya ditangani oleh penyedia. Pelanggan tidak perlu mengunduh pemutakhiran atau menginstal ulang versi baru suatu produk karena perangkat lunak dikirimkan melalui internet.
Mengapa Menggunakan Arsitektur SaaS,Dari sudut pandang konsumen, aplikasi SaaS adalah salah satu cara termudah dan paling dapat diandalkan untuk menggunakan layanan atau produk digital.Dari perspektif bisnis, produk perangkat lunak yang diberikan “sebagai layanan” memungkinkan perusahaan untuk menawarkan produk mereka dalam skala besar dan global.

Platform SaaS memiliki beragam kemampuan. Apalagi jika digabungkan dengan penawaran cloud lainnya seperti IaaS (Infrastructure as a Service) dan PaaS (Platform as a Service).Teknologi cloud seperti Microsoft Azure memungkinkan Anda menyediakan server yang dapat menghosting situs web, database, dan banyak lagi.

==============================================================


Cara membangun aplikasi SaaS berbasis cloud

Saat membangun aplikasi SaaS, kemungkinan besar Anda akan membangunnya di cloud.cloud memiliki keuntungan, terutama dalam hal skalabilitas, dibandingkan dengan lingkungan server lokal.Pemilihan bahasa pemrograman yang modern menjadi penting dalam membangun produk SaaS. Python adalah salah satu pilihan yang populer karena fleksibilitasnya.penggunaan basis data berorientasi dokumen, seperti MongoDB, yang dapat memberikan performa, ketersediaan, dan skalabilitas tinggi.Sistem antrian (queuing system) digunakan untuk komunikasi asynchronous antara aplikasi dan layanan pihak ketiga. RabbitMQ adalah salah satu contoh sistem antrian yang populer.AWS dan EC2 menyediakan infrastruktur untuk menjalankan aplikasi web dan tugas besar dengan kapasitas yang dapat disesuaikan.

Penyimpanan Web S3: Amazon S3 adalah layanan penyimpanan objek yang skalabel dan dapat digunakan untuk berbagai keperluan, termasuk penyimpanan data aplikasi web dan pencadangan basis data.
Content Delivery Network (CDN): CDN adalah sistem server terdistribusi yang meningkatkan performa dan ketersediaan penyampaian konten aplikasi ke pengguna.







=============================================================================

latihan no 2 :

Berikut adalah dua layanan SaaS (Software as a Service) 

1. Google Workspace :Google Workspace adalah kumpulan alat produktivitas berbasis cloud yang mencakup Gmail, Google Drive, Google Docs, Google Sheets, Google Slides, dan banyak lagi. Ini digunakan oleh perusahaan dan individu untuk berkolaborasi secara online, berbagi dokumen, dan mengelola komunikasi email mereka.

2. Microsoft 365 :Microsoft 365 adalah paket perangkat lunak berlangganan yang mencakup berbagai aplikasi produktivitas, seperti Microsoft Word, Excel, PowerPoint, Outlook, dan lainnya. Layanan ini juga mencakup penyimpanan cloud, alat kolaborasi tim, serta fitur keamanan dan manajemen yang kuat.Microsoft 365 digunakan oleh individu, bisnis kecil, dan perusahaan besar sebagai solusi produktivitas berbasis cloud. Pengguna dapat mengakses aplikasi ini dari berbagai perangkat dengan langganan bulanan atau tahunan.


berikut memiliki fungsionalitas serupa dengan dua layanan SaaS yang telah disebutkan sebelumnya:

-Alternatif Desktop untuk Microsoft 365:Microsoft Office Suite

-Alternatif untuk Google Workspace: LibreOfficee 
