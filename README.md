# Dokumentasi OpenAPI WhatsAuth

[Editor](https://editor.swagger.io/) dan [URL](https://wa.my.id/apidocs/openapi.yaml)
# authorize
masukan token di bagian itu ada dibagian paling atas sebelah kanan

# Pendaftaran, refresh token dengan input URL dan Secret WebHook
masuk ke website https://wa.ulbi.ac.id/apidocs 
bagian signup, methode POST, try it out|
{
  "url": "",
  "secret": ""
}
masukan url "https://msg.ulbi.ac.id/webhook/nomor/62..."
masukan secret|
execute


# Menambahkan wa user ke server
masuk ke website https://wa.ulbi.ac.id/apidocs|
bagian device methode GET, try it out|
masukan token(Token yang diberikan kepada user), execute

# Mengirim pesan
masukan nomor tujuan|
{
  "to": "62",
  "isgroup": false,
  "messages": "hai kak"
}
execute



