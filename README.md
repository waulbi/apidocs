# Dokumentasi OpenAPI WhatsAuth

[Editor](https://editor.swagger.io/) dan [URL](https://wa.my.id/apidocs/openapi.yaml)

# Pendaftaran, refresh token dengan input URL dan Secret WebHook
masuk ke website https://wa.ulbi.ac.id/apidocs
bagian signup, POST, try it out
{
  "url": "",
  "secret": ""
}
masukan url "https://msg.ulbi.ac.id/webhook/nomor/62..."
masukan secret
execute


# Menambahkan wa user ke server
masuk ke website https://wa.ulbi.ac.id/apidocs
bagian device methode GET, try it out
masukan token(Token yang diberikan kepada user), execute

# Mengirim pesan
masukan nomor
{
  "to": "62",
  "isgroup": false,
  "messages": "hai kak"
}
execute



