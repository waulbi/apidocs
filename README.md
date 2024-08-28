# Dokumentasi OpenAPI WhatsAuth

[Editor](https://editor.swagger.io/) dan [URL](https://wa.my.id/apidocs/openapi.yaml)

# Pendaftaran, refresh token dengan input URL dan Secret WebHook
masuk ke website https://wa.ulbi.ac.id/apidocs 
bagian signup, methode POST, try it out/n 
{
  "url": "",
  "secret": ""
}
masukan url "https://msg.ulbi.ac.id/webhook/nomor/62..."
masukan secret/n
execute


# Menambahkan wa user ke server
masuk ke website https://wa.ulbi.ac.id/apidocs/n 
bagian device methode GET, try it out/n
masukan token(Token yang diberikan kepada user), execute

# Mengirim pesan
masukan nomor/n
{
  "to": "62",
  "isgroup": false,
  "messages": "hai kak"
}
execute



