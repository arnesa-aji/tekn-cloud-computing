# Minikube

## Objectives 
- Deploy contoh aplikasi ke minikube.
- Jalankan aplikasi.
- Lihat log aplikasi.

## minikube start
1. Unduh dan jalankan penginstal [disini](https://translate.google.com/website?sl=auto&tl=id&hl=id&client=webapp&u=https://storage.googleapis.com/minikube/releases/latest/minikube-installer.exe)
2. Tambahkan `minikube.exe` biner ke file `PATH`.Pastikan untuk menjalankan PowerShell sebagai Administrator.
3. Start your cluster
   ```
   minikube start
   ```
   ![minikube start](./01-minikube-start.jpg)

4. Buka dasbor Kubernetes
   ```
   minikube dashboard
   ```
   ![minikube dashboard](./03-minikube-dashboard.jpg)

## Create a Deployment

1. Gunakan `kubectl create` perintah untuk membuat Deployment yang mengelola sebuah Pod. Pod menjalankan sebuah Container berdasarkan image Docker yang disediakan.
   ```
   kubectl create deployment hello-node --image=registry.k8s.io/e2e-test-images/agnhost:2.39 -- /agnhost netexec --http-port=8080
   ```
   ![kubectl create](./04-kubectl-create.jpg)

2. View the Deployment:
   ```
   kubectl get deployments
   ```
   ![get deploy](./05-kubectl-deploy.jpg)

3. View the Pod:
   ```
   kubectl get pods
   ```
   ![get pods](./06-kubectl-get-pods.jpg)

4. View cluster events:
   ```
   kubectl get events
   ```
   ![get event](./07-kubectl-get-events.jpg)

5. View the configuration:
   ```
   kubectl config view
   ```
   ![config view](./08-kubectl-config.jpg)

6. Melihat log aplikasi untuk sebuah container di dalam pod.
   ```
   kubectl logs hello-node-5f76cf6ccf-br9b5
   ```
   ![logs](./09-kubectl-logs.jpg)

## Create a Service
1. Ekspos Pod ke internet publik menggunakan `kubectl expose` perintah:
   ```
   kubectl expose deployment hello-node --type=LoadBalancer --port=8080
   ```
   ![expose deploy](./10-kubectl-expose.jpg)
2. Lihat Layanan yang telah di buat:
   ```
   kubectl get services
   ```
   ![get service](./11-kubectl-get-services.jpg)
3. Jalankan perintah berikut:
   ```
   minikube service hello-node
   ```
   ![service hello-node](./12-minikube-service-hello-node.jpg)
   Ini akan membuka jendela browser yang menyajikan aplikasi Anda dan menampilkan respons aplikasi.
   ![ui](./12-minikube-service-hello-node-ui.jpg)
