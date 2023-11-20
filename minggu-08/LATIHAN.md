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

   
