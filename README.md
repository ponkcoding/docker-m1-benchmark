Project ini berisi angular & golang project yang digunakan untuk benchmark docker container di macbook air M1.
Angular & golang project ini akan di running di dalam docker container dimana kita akan menggunakan intel-based container & ARM-based container.
Selanjutnya kita akan melihat seberapa jauh perbedaan performance yang dihasilkan oleh kedua container ini.

## Spesifikasi

### Hardware

* CPU: Apple M1 (8-core)
* Graphics: Integrated 7-core GPU.
* RAM: 8GB Unified PDDR4X-4266 MHz SDRAM.
* Storage: 256GB PCIe SSD

### docker image

* node:15
* golang:1.16

## Run the app

```
docker-compose build
docker-compose up
```

Setelah appnya running, kita bisa melihat compile/build time di output terminal.
Kita bisa coba mengubah source codenya agar app-nya di rebuild/recompile. 

### URLs

* http://localhost:4201 angular - ARM-based container (arm64)
* http://localhost:4202 angular - intel-based container (amd64)
* http://localhost:5001/api/ping/ golang-gin - ARM-based container (arm64)
* http://localhost:5002/api/ping/ golang-gin - intel-based container (amd64)

## Build/Compile time benchmark
| Project  |  ARM-based container | intel-based container  |
|---|---|---|
|  Angular |   |   |
|  Golang |   |   |

## Referensi

* https://angular.io/guide/example-apps-list#tour-of-heroes-tutorial-application
* https://github.com/gothinkster/golang-gin-realworld-example-app