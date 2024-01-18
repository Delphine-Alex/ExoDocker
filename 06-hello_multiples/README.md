Oh oh problémo 😕: tu as une application node qui utilise un contenaire de base de données PostgreSQL vue précédemment, comment tu vas les faire communiquer ?

Sachant qu'un contenaire est isolé... 🤔 Débrouille-toi !

L'application devrait renvoyer les noms dans la table "personnes".

Note :

- docker network ls
- docker build -t exo-06 .
- docker run -d --name exo-06-container -p 3000:3000 exo-06
- docker network connect exo06 exo-06-container
- docker inspect exo06

[
{
"Name": "exo06",
"Id": "6716209fcce6e22855236b731c20472d8f161d73f893cfb48c54abb561b07948",
"Created": "2024-01-18T16:01:06.147113351Z",
"Scope": "local",
"Driver": "bridge",
"EnableIPv6": false,
"IPAM": {
"Driver": "default",
"Options": {},
"Config": [
{
"Subnet": "172.19.0.0/16",
"Gateway": "172.19.0.1"
}
]
},
"Internal": false,
"Attachable": false,
"Ingress": false,
"ConfigFrom": {
"Network": ""
},
"ConfigOnly": false,
"Containers": {
"1e2ca9a7f26a39c00232176dac1b9416a55f5d84d09228833fe1115f0555b2dd": {
"Name": "exo-05-container",
"EndpointID": "175bdd7e1861ebf23c41e705269305a26172cb32bdc6172c9f6d8eaa0f54e1c6",
"MacAddress": "02:42:ac:13:00:02",
"IPv4Address": "172.19.0.2/16",
"IPv6Address": ""
},
"32170d757ab0dfd8997c6d69cecf628d9a563b230ddb006b58b9221c914e615d": {
"Name": "exo-06-container",
"EndpointID": "a5206f57149805a9b44c6063f1fda6ca55cc2dc25bc4d31100d9848081a5a81e",
"MacAddress": "02:42:ac:13:00:03",
"IPv4Address": "172.19.0.3/16",
"IPv6Address": ""
}
},
"Options": {},
"Labels": {}
}
]
