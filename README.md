# Dokumentasi OpenAPI WhatsAuth

cara menggunakan API WhatsAuth untuk pendaftaran, otorisasi, menambahkan pengguna, dan mengirim pesan melalui WhatsApp. Akses editor Swagger [di sini](https://editor.swagger.io/) dan file OpenAPI YAML [di sini](https://wa.my.id/apidocs/openapi.yaml).

# Wa bisnis
siapakan nomor wa bisnis
Lalu di wa bisnis masuk ke bagian perangkat tertaut untuk menaut kan perangkat
pilih tautkan dengan nomor telepon saja, ada di bagian paling bawah setelah mengklik tautkan perangkat
akan ada halaman untuk memasukan kode, untuk mendapatkan kode
Masuk ke dashboard domyikado, dibagian sidebar terdapat masuk menu profile lalu pilih linked device
![Foto Penulis 3](Penulis3.jpg)

 tambahkan di database pamongdesa collection profile
```{
  "token": "",
  "phonenumber": "62....",
  "secret": "",
  "url": "http://172.18.0.147:8080/webhook/nomor/62...",
  "urlapitext": "http://172.18.0.148:8080/api/v2/send/message/text",
  "urlapiimage": "http://172.18.0.148:8080/api/send/message/image",
  "urlapidoc": "http://172.18.0.148:8080/api/send/message/document",
  "urlqrlogin": "http://172.18.0.148:8080/api/whatsauth/request",
  "qrkeyword": "wh4t5auth0",
  "publickey": "",
  "botname": "Peedee",
  "triggerword": "pd",
  "telegramtoken": "",
  "telegramname": ""
}
```
## 2. Authorize

 masukkan token di bagian **Authorize** di halaman API.

## 2. Pendaftaran dan Refresh Token

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

- Pastikan token sudah dimasukan dibagian Authorize sebelum testing.
