# Frequently Asked Questions

Dibawah ini adalah pertanyaan dan jawaban yang seringkali diajukan saat mengalami masalah penggunaan bebasid

## Pertanyaan Umum
### Bagaimana cara kerja bebasid?
- bebasid bekerja dengan cara memetakan hostname ke alamat IP dalam file hosts sehingga untuk akses ke hostname yang diblokir tidak ke DNS, melainkan langsung di resolve oleh file hosts

### Adakah batasan maksimum dalam file hosts
- Hasil riset kami pada tahun 2019 menunjukkan bahwa file hosts dengan konten lebih dari sekitar 1 juta domain yand diblokir oleh Internet Positif (18 MB file dengan format txt) akan menunjukkan error "DNS Not Resolved" terhadap domain lain yang tidak tercantum dalam file hosts alias internet hanya dapat mengakses domain yang tercatat dalam file hosts

### Apakah bebasid merupakan VPN?
- Bukan

### Apakah bebasid berimbas terhadap kecepatan koneksi internet?
- Tidak, berbeda dengan VPN, bebasid tidak menyebabkan kecepatan koneksi internet bertambah ataupun berkurang.

### Apakah aplikasi bypass DPI seperti GoodbyeDPI dan Green Tunnel merupakan VPN?
- Bukan, aplikasi bypass DPI bekerja dengan cara memanipulasi HTTP Request Header sehingga tidak mengubah alamat IP Address


## Penyelesaian Masalah untuk Windows
### Error saat menginstall menggunakan aplikasi bebasid
- Laporkan masalah ini ke Discord bebasid
- Gunakan pemasangan file hosts secara manual

### File hosts tidak terpasang, padahal sudah menggunakan aplikasi bebasid
- Seringkali aplikasi Antivirus seperti Kaspersky mengembalikan file hosts menjadi default
- Ada masalah saat melakukan pemasangan oleh aplikasi bebasid

### Sudah terpasang hosts bebasid, tetapi akses masih terblokir oleh Internet Positif
- Lakukan flushdns
- Hapus cache dan cookie
- Restart komputer

### Sudah memasang hosts bebasid, tetapi tidak dapat memutar video di Netflix
- Apakah sudah mengikuti prosedur yang ada [disini](https://github.com/bebasid/bebasid/blob/master/dev/readme/NETFLIX.md)?


## Penyelesaian Masalah untuk Linux
### Muncul "Tidak dapat terkoneksi dengan Internet" padahal terkoneksi dengan internet
- Aplikasi bebasid gagal melakukan ping ke 8.8.8.8 dikarenakan suatu sebab (misalnya menggunakan jaringan Tri Indonesia), solusinya mengulang hingga berhasil

### Sudah memasang hosts bebasid, tetapi tidak dapat memutar video di Netflix
- Apakah sudah mengikuti prosedur yang ada [disini](https://github.com/bebasid/bebasid/blob/master/dev/readme/NETFLIX.md)?

### Sudah memakai Green Tunnel untuk Linux, tetapi tetap saja tidak dapat membuka Netflix di jaringan Indihome
- Jaringan Indihome anda telah melakukan blokade sangat mendalam kepada Netflix, salah satu solusi untuk mengatasi hal ini adalah menggunakan VPN


## Penyelesaian Masalah untuk MacOS (OSX)
### Mengapa bebasid tidak bekerja di peramban Safari?
- Peramban Safari hanya menggunakan hosts jika tercantum IPv4 dan IPv6, sedangkan bebasid hanya mencantumkan IPv4

### Sudah memasang hosts bebasid, tetapi tidak dapat memutar video di Netflix
- Apakah sudah mengikuti prosedur yang ada [disini](https://github.com/bebasid/bebasid/blob/master/dev/readme/NETFLIX.md)?

### Sudah memakai Green Tunnel untuk Mac, tetapi tetap saja tidak dapat membuka Netflix di jaringan Indihome
- Jaringan Indihome anda telah melakukan blokade sangat mendalam kepada Netflix, salah satu solusi untuk mengatasi hal ini adalah menggunakan VPN

### Setelah menggunakan Green Tunnel, koneksi ke Chrome hanya dapat dibuka jika Green Tunnel dibuka
- Google Chrome tidak tertutup sempurna sehingga Google Chrome masih berjalan diatas proxy, solusinya adalah dengan menutup semua Google Chrome dengan perintah `sudo killall 'Google Chrome'`
