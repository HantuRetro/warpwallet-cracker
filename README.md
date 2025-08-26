# warpwallet_cracker
Script ini adalah versi yang dimodifikasi dari versi nachowski/warpwallet_cracker

# Usage

```
go mod init warpwallet
go mod tidy
go install golang.org/x/crypto/pbkdf2
go install golang.org/x/crypto/scrypt
go install github.com/vsergeev/btckeygenie/btckey

go get golang.org/x/crypto/pbkdf2
go get golang.org/x/crypto/scrypt
go get github.com/vsergeev/btckeygenie/btckey

$ go get / go install 
---
$ go build
---
$ ./run.sh 
Gunakan alamat "1MkupVKiCik9iyfnLrJoZLx9RH4rkF3hnA"
```

# Performance
Peningkatan lebih lanjut:
- Menjajaki penggunaan SSE2 untuk skrip yang lebih cepat
- Menggunakan semua inti CPU
- Membangun filter bloom yang berisi percobaan sebelumnya (apakah pencarian filter bloom lebih cepat daripada percobaan hash?)
- Menemukan cara untuk berbagi filter bloom dengan cracker lain
- Pembuatan kunci deterministik untuk partisi ruang pencarian yang lebih baik (alih-alih melakukan seeding rand dengan stempel waktu unix)

# How-to
Build:

`go build warpwallet.go`

Params:

`./warpwallet [Address] [Salt - optional]`

Run (Windows):

`run.bat`

Run (*nix):

`./run.sh`

Run unit tests and benchmark:

`go test -bench=.`

Windows Command
`warpwallet.exe 1JKb1617p68H5MPkoNaMtaJCqKDU3h8qSn`


Coba gunakan dengan passphrase 2 lalu coba 3 dst. secara default hanya mencari 2 passphrase

untuk membuat alamat bitcoin menggunakan passhrase disini https://keybase.io/warp/warp_1.0.9_SHA256_a2067491ab582bde779f4505055807c2479354633a2216b22cf1e92d1a6e4a87.html

- Video Setup : https://www.youtube.com/watch?v=ZFh-9uX5lug

#DONATION 
- BTC `3ArabZutRGFscn8qi67vUBi6bbUohESdHQ`
- QUBIC `ONLYBZNXUYQFDHXMLXVHQJBULTKCYOFLCUQHPEBFEFHHLDRIJGUORZZCORHD`
