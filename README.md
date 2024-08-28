# Dokumentasi OpenAPI WhatsAuth

cara menggunakan API WhatsAuth untuk pendaftaran, otorisasi, menambahkan pengguna, dan mengirim pesan melalui WhatsApp. Akses editor Swagger [di sini](https://editor.swagger.io/) dan file OpenAPI YAML [di sini](https://wa.my.id/apidocs/openapi.yaml).

## 1. Pendaftaran dan Refresh Token

Untuk mendaftarkan webhook URL dan mendapatkan token baru:
Buka [halaman API WhatsAuth](https://wa.ulbi.ac.id/apidocs).
bagian **`signup`** dengan metode **POST**.
Klik **Try it out** untuk mengisi parameter.
   ```json
   {
     "url": "http://172.18.0.147:8080/webhook/nomor/62...",
     "secret": "masukkan_secret_anda"
   }
   ```
**Execute** 

   Setelah dieksekusi, balasan berupa **Token** yang baru.

## 2. Authorize

 masukkan token di bagian **Authorize** di halaman API.

## 3. Menambahkan Pengguna WhatsApp ke Server

Pilih bagian **`device`** dengan metode **GET**.
Klik **Try it out** masukkan token.
**Execute**

## 4. Mengirim Pesan

   ```json
   {
     "to": "62nomortujuan",
     "isgroup": false,
     "messages": "hai kak"
   }
   ```
 **Execute**

- Pastikan token sudah dikasukan dibagian Authorize sebelum testing.
