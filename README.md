# Dokumentasi OpenAPI WhatsAuth

cara menggunakan API WhatsAuth untuk pendaftaran, otorisasi, menambahkan pengguna, dan mengirim pesan melalui WhatsApp. Akses editor Swagger [di sini](https://editor.swagger.io/) dan file OpenAPI YAML [di sini](https://wa.my.id/apidocs/openapi.yaml).

# Wa bisnis
siapakan nomor wa bisnis

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
tambahkan di database waapi collection profile
```
{
"token":" ",
  "phonenumber": "628...",
  "secret": "",
  "url": "http://172.18.0.147:8080/webhook/inbox",
  "qrkeyword": "wh4t5auth0"
}
```

### Melakukan Pendaftaran nomor di WAAPI

## 1. Authorize
Buka [halaman API WhatsAuth](https://wa.ulbi.ac.id/apidocs)
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
masukan **Token** baru di  **Authorize** mengganti token sebelumnya.

## 3. Menambahkan Pengguna WhatsApp ke Server

Pilih bagian **`device`** dengan metode **GET**.
Klik **Try it out** masukkan token.
**Execute**
maka akan muncul 
**code** untuk dimasukan di bagian tautkan perangkat wa bisnis
buka wa bisnis masuk ke bagian perangkat tertaut
pilih tautkan dengan nomor telepon saja, ada di bagian paling bawah setelah mengklik tautkan perangkat
akan ada halaman untuk memasukan kode

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


# menambahkan nomor di leafly

tambahkan nomor di database pamongdesa koleksi config

```
{
  "leaflyurl": "http://172.18.0.149:8080/face/detect",
  "leaflysecret": "",
  "phonenumber": "628....",
  "domyikadosecret": "",
  "domyikadopresensiurl": "https://asia-southeast2-awangga.cloudfunctions.net/domyid/notif/ux/postpresensi/628...",
  "domyikadotasklisturl": "https://asia-southeast2-awangga.cloudfunctions.net/domyid/notif/ux/posttasklists/628...",
  "leaflyurlktp": "https://lea.fly.dev/ktp/detect",
  "leaflyurllmsdesagambar": "http://172.18.0.149:8080/arsip/gambar/lmsdesa",
  "leaflyurllmsdesafile": "http://172.18.0.149:8080/arsip/file/lmsdesa",
  "domyikadouserurl": "https://asia-southeast2-awangga.cloudfunctions.net/domyid/data/user/wa/628...",
  "siakadloginurl": "https://asia-southeast2-domytest.cloudfunctions.net/domytest/login",
  "bapurl": "https://asia-southeast2-domytest.cloudfunctions.net/domytest/BAP",
  "approvebimbinganbypoinurl": "https://asia-southeast2-awangga.cloudfunctions.net/domyid/approvebimbingan",
  "approvebimbinganurl": "https://asia-southeast2-domytest.cloudfunctions.net/domytest/approve/bimbingan",
  "urlkimseokgis": "https://asia-southeast2-gis-project-401902.cloudfunctions.net/backend-ai/chatDomykado",
  "approvebapurl": "https://asia-southeast2-domytest.cloudfunctions.net/domytest/ApproveBAP",
  "cekapprovalbapurl": "https://asia-southeast2-domytest.cloudfunctions.net/domytest/StatusApproval"
}
```

lalu tambahkan di koleksi module
masukan ke bagian dengan name: presensi-masuk, presensi-pulang, selfie-masuk, selfie-pulang
```
{
  "name": "presensi-masuk",
  "keyword": [
    "cekin",
    "presensi",
    "masuk"
  ],
  "phonenumbers": [
    "628...",
    "628...",
    "628...",
    "628..."
  ],
  "group": true,
  "personal": true
}
```


