# Docker compose

## Prerequisites

1. Docker Desktop
2. Docker Engine
3. Docker Compose

## Langkah-langkah :

1. buat direktori untuk proyek,anda bisa menggunakan cmd dengan mengetikan perintah berikut :
   ```
   $ mkdir composetest
   $ cd composetest
   ```

2. Buat file bernama `app.pydi` direktori proyek Anda dan tempelkan kode berikut di:
   ```
   import time

   import redis
   from flask import Flask

   app = Flask(__name__)
   cache = redis.Redis(host='redis', port=6379)

   def get_hit_count():
    retries = 5
    while True:
        try:
            return cache.incr('hits')
        except redis.exceptions.ConnectionError as exc:
            if retries == 0:
                raise exc
            retries -= 1
            time.sleep(0.5)
   @app.route('/')
   def hello():
    count = get_hit_count()
    return 'Hello World! I have been seen {} times.\n'.format(count)
   ```

3. Buat file `requirements.txt` di direktori proyek Anda dan tempelkan kode berikut di:
      ```
      flask
      redis
      ```
4. Di direktori proyek Anda, buat file bernama `Dockerfile.file` dan tempelkan kode berikut di:
   ```
    syntax=docker/dockerfile:1
   FROM python:3.7-alpine
   WORKDIR /code
   ENV FLASK_APP=app.py
   ENV FLASK_RUN_HOST=0.0.0.0
   RUN apk add --no-cache gcc musl-dev linux-headers
   COPY requirements.txt requirements.txt
   RUN pip install -r requirements.txt
   EXPOSE 5000
   COPY . .
   CMD ["flask", "run"]
   ```
Periksa apakah Dockerfiletidak memiliki ekstensi file seperti .txt. Beberapa editor mungkin menambahkan ekstensi file ini secara otomatis yang mengakibatkan kesalahan saat Anda menjalankan aplikasi.

5. Buat file bernama `compose.yaml` di direktori proyek Anda dan tempelkan yang berikut ini:
   ```
   services:
     web:
       build: .
       ports:
         - "8000:5000"
     redis:
       image: "redis:alpine"
   ```

6. Dari direktori proyek Anda, mulai aplikasi Anda dengan menjalankan `docker compose up`.
   ![jalankan docker compose up](./01-docker-compose-up.jpg)
   
