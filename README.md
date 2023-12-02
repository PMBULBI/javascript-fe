
# Panduan Edit sidebar CDN

Link Import CDN  
```
https://cdn.jsdelivr.net/gh/PMBULBI/javascript-fe/
```

1. Pertama, jika ingin mengubah sidebar yang ada bisa langsung ubah file sidebar.html
    ```
    static/sidebar.html
    ```
2. Setelah edit sidebar, selanjutnya edit import pada sidebar.js dengan versi tag terbaru
    ```
    bar/sidebar.js

    ```
3. Line yang diubah pada sidebar.js adalah line load seperti pada gambar dibawah:
Line yang perlu diupdate
```
$("#sidebar-container").load("https://cdn.jsdelivr.net/gh/PMBULBI/javascript-fe@0.2.1/static/sidebar.html");
```

- NOTE : Contoh jika saat ini versi javascript yang digunakan adalah versi 0.2.1 maka update selanjutnya sebelum melakukan tag ubah loadnya menjadi versi 0.2.2.

4. Jika perubahan sudah selesai lakukan tag dan push ke repository

```
$ git tag <version>
$ git push --tags
$ git push
```

5. Selanjutnya, setelah selesai update maka edit HTML yang ada pada repo pmb-mhs
6. Ubah import di setiap halaman agar load sidebar terbaru
```
 <script src="https://cdn.jsdelivr.net/gh/PMBULBI/javascript-fe@0.1.8/bar/sidebar.js"></script>
```
Update versi setiap sidebar.js sesuai dengan tag Javascript-fe terbaru

