# Commit 1 Reflection notes

Penjelasan method handle_connection per baris:
    ```let buf_reader = BufReader::new(&mut stream);``` Struct BufReader menambahkan buffering kepada suatu reader. Secara praktek, ini

Request: [
    "GET / HTTP/1.1",
    "Host: 127.0.0.1:7878",
    "User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:124.0) Gecko/20100101 Firefox/124.0",
    "Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,*/*;q=0.8",
    "Accept-Language: en-US,en;q=0.5",
    "Accept-Encoding: gzip, deflate, br",
    "Connection: keep-alive",
    "Cookie: csrftoken=uL4eoO26S2nPYvqFPwZHCZZmwzRlyy81",
    "Upgrade-Insecure-Requests: 1",
    "Sec-Fetch-Dest: document",
    "Sec-Fetch-Mode: navigate",
    "Sec-Fetch-Site: none",
    "Sec-Fetch-User: ?1",
]

# Commit 2 Reflection notes
![Commit 2 screen capture](/screenshots/commit2.png)

# Commit 3 Reflection notess
![Commit 3 screen capture](/screenshots/commit3.png)

Respon terpisah berdasarkan isi request dari client. Jika request sesuai dengan 'request_line == "GET / HTTP/1.1"', maka hello.html akan dimunculkan. Jika tidak, yang dimunculkan adalah 404.html.

Refactoring dilakukan karena pada bagian if-else sebelum refactoring, ada banyak baris kode yang merupakan repetisi. Beberapa contoh adalah bagian 'let response' dan 'steam.write_all' yang ada pada bagian if dan bagian else. Setelah dilakukan refactoring, repetisi itu tidak ada dan kode menjadi lebih enak untuk dibaca (code smell dihapus).

# Commit 4 Reflection notes
Baris 'thread::sleep(Duration::from_secs(10));' membawa thread untuk sleep selama 10 detik. Dari percobaan request yang menggunakan sleep dan request yang biasa, terlihat bahwa ada perbedaan load time sekitar 10 detik.

# Commit 5 Reflection notes
ThreadPool akan membuat suatu thread pool (sekumpulan thread) dimana setiap thread dapat mengeksekusi suatu task. Satu thread melakukan satu task, dan thread yang tidak sedang melakukan task akan menunggu untuk kemunculan task baru. Ketika suatu task selesai, thread yang melakukan task itu akan dikembalikan ke dalam thread pool. Juga, jumlah thread yang berada pada suatu thread pool biasanya dibatasi untuk menghindari risiko terjadinya DoS attack (Denial of Service attack).