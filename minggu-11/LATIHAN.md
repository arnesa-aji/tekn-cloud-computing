# Application Containerization and Microservice Orchestration
## Stage Setup
1. clone repositori demo code berikut :
```
git clone https://github.com/ibnesayeed/linkextractor.git
cd linkextractor
git checkout demo
```
![page setup](./stage-setup/page-setup.jpg)
## Step 0: Basic Link Extractor Script
1. periksa `step0` cabang dan daftar file didalamnya
```
git checkout step0
tree
```
![tree 0](./step-0/01-tree.jpg)

## Step 1: Containerized Link Extractor Script
1. periksa `step1` cabang dan daftar file didalamnya
```
git checkout step1
tree
```
![tree 1](./step-1/04-tree.jpg)
2. selanjutnya jalankan perintah berikut :
```
docker image build -t linkextractor:step1 .
```
![image build](./step-1/06-build-image.jpg)
image Docker yang diberi nama `linkextractor:step1` berdasarkan Dockerfile ilustrasi di atas. Jika build berhasil, anda akan melihatnya di daftar image:
```
docker image ls
```
![image ls](./step-1/07-image-ls.jpg)
