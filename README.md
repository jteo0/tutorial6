# Commit 1 Reflection notes

Penjelasan method handle_connection per baris:
    ```let buf_reader = BufReader::new(&mut stream);``` Struct BufReader menambahkan buffering kepada suatu reader. Secara praktek, ini

cargo run
   Compiling hello v0.1.0 (C:\Users\Acer\code_folder\hello)
    Finished dev [unoptimized + debuginfo] target(s) in 2.93s
     Running `target\debug\hello.exe`
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