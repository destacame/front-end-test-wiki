# Api de consumo para prueba front-end Destácame

A continuación encontrarás la documentación del backend para desarrollar la prueba técnica.

## Para utilizar los post es necesario siempre enviar:
```
    {
        "user": "ejemploAdmin",
        "pass": "destacado"
    }
```
> La API recibe json como request.

> En caso de que el post necesite más parametros, agregadlos al diccionario o json.

<br/>

## Las urls:

[URL_BASE] = http://ec2-18-231-131-247.sa-east-1.compute.amazonaws.com

| Name | HTTP request method | Action | Url |
| --- | --- | --- | --- |
| Chofer | POST | Select All | [URL_BASE]/chofer/all |
| Chofer | POST | Select  | [URL_BASE]/chofer/\<id> |
| Chofer | POST | Insert   | [URL_BASE]/chofer |
| Chofer | PUT | Update  | [URL_BASE]/chofer/\<id> |
| Chofer | DELETE | Delete  | [URL_BASE]/chofer/\<id> |
| Asiento | POST | Select All | [URL_BASE]/asiento/all |
| Asiento | POST | Select  | [URL_BASE]/asiento/\<id> |
| Asiento | POST | Insert   | [URL_BASE]/asiento |
| Asiento | PUT | Update  | [URL_BASE]/asiento/\<id> |
| Asiento | DELETE | Delete  | [URL_BASE]/asiento/\<id> |
| Pasajero | POST | Select All | [URL_BASE]/pasajero/all |
| Pasajero | POST | Select  | [URL_BASE]/pasajero/\<id> |
| Pasajero | POST | Insert   | [URL_BASE]/pasajero |
| Pasajero | PUT | Update  | [URL_BASE]/pasajero/\<id> |
| Pasajero | DELETE | Delete  | [URL_BASE]/pasajero/\<id> |
| Horario | POST | Select All | [URL_BASE]/horario/all |
| Horario | POST | Select  | [URL_BASE]/horario/\<id> |
| Horario | POST | Insert   | [URL_BASE]/horario |
| Horario | PUT | Update  | [URL_BASE]/horario/\<id> |
| Horario | DELETE | Delete  | [URL_BASE]/horario/\<id> |
| Trayecto | POST | Select All | [URL_BASE]/trayecto/all |
| Trayecto | POST | Select  | [URL_BASE]/trayecto/\<id> |
| Trayecto | POST | Insert   | [URL_BASE]/trayecto |
| Trayecto | PUT | Update  | [URL_BASE]/trayecto/\<id> |
| Trayecto | DELETE | Delete  | [URL_BASE]/trayecto/\<id> |
| Bus | POST | Select All | [URL_BASE]/bus/all |
| Bus | POST | Select  | [URL_BASE]/bus/\<id> |
| Bus | POST | Insert   | [URL_BASE]/bus |
| Bus | PUT | Update  | [URL_BASE]/bus/\<id> |
| Bus | DELETE | Delete  | [URL_BASE]/bus/\<id> |

<br/>

## El modelo:

| MODEL | ATRIBUTES | length |
| ---   | --- | --- |
| Chofer  |  nombre *String*,<br> apellido *String*,<br> rut *String* | 150, 150, 10 |
| Pasajero | nombre *String*,<br> apellido *String*,<br> rut *String* | 150, 150, 10 |
| Trayecto | ida *String*,<br> vuelta *String*,<br> terminal *String* | 300, 300, 250 |
| Bus | patente *String*,<br> marca *String*,<br> id_chofer *Int* | 50, 100, \- |
| Asiento | num_asiento *Int*,<br> id_bus *Int*,<br> id_pasajero *Int*| \-,\-,\- |
| Horario| fecha *String* 'Mes/Dia/Año',<br> hora *String* 'Hora:Min:Seg',<br> id_trayecto *Int*,<br> id_bus *Int* | \-, \-, \-, \- |

<br/>

## Ejemplos:
### Select All
URL = [URL_BASE]/chofer/all

METHOD = POST
```
    {
        "user": "ejemploAdmin",
        "pass": "destacado"
    }
```

### Update
URL = [URL_BASE]/chofer/2

METHOD = PUT
```
    {
        "user": "ejemploAdmin",
        "pass": "destacado",
        "nombre": "Jose",
        "apellido": "Angel",
        "rut": "17467125-1"
    }
```
