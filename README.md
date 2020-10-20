# Api de consumo para prueba front-end Destácame

A continuación encontrarás la documentación del backend para desarrollar la prueba técnica.

## Es necesario agregar en el HEADER el Token para poder acceder:
Es necesario agregar "Token " al principio y despues colocar el token...
```
    HEADER
    Authorization Token <aquí va tu token>
```

> La API recibe *JSON* como request.

> En caso de que el post necesite más parametros, agregadlos al diccionario o json.

<br/>

## Las urls:

[URL_BASE] = testing.destacame.cl

| Name | HTTP request method | Action | Url |
| --- | --- | --- | --- |
| Chofer | GET | Select All | [URL_BASE]/chofer/all |
| Chofer | GET | Select  | [URL_BASE]/chofer/\<id> |
| Chofer | POST | Insert   | [URL_BASE]/chofer |
| Chofer | PUT | Update  | [URL_BASE]/chofer/\<id> |
| Chofer | DELETE | Delete  | [URL_BASE]/chofer/\<id> |
| Asiento | GET | Select All | [URL_BASE]/asiento/all |
| Asiento | GET | Select  | [URL_BASE]/asiento/\<id> |
| Asiento | POST | Insert   | [URL_BASE]/asiento |
| Asiento | PUT | Update  | [URL_BASE]/asiento/\<id> |
| Asiento | DELETE | Delete  | [URL_BASE]/asiento/\<id> |
| Pasajero | GET | Select All | [URL_BASE]/pasajero/all |
| Pasajero | GET | Select  | [URL_BASE]/pasajero/\<id> |
| Pasajero | POST | Insert   | [URL_BASE]/pasajero |
| Pasajero | PUT | Update  | [URL_BASE]/pasajero/\<id> |
| Pasajero | DELETE | Delete  | [URL_BASE]/pasajero/\<id> |
| Horario | GET | Select All | [URL_BASE]/horario/all |
| Horario | GET | Select  | [URL_BASE]/horario/\<id> |
| Horario | POST | Insert   | [URL_BASE]/horario |
| Horario | PUT | Update  | [URL_BASE]/horario/\<id> |
| Horario | DELETE | Delete  | [URL_BASE]/horario/\<id> |
| Trayecto | GET | Select All | [URL_BASE]/trayecto/all |
| Trayecto | GET | Select  | [URL_BASE]/trayecto/\<id> |
| Trayecto | POST | Insert   | [URL_BASE]/trayecto |
| Trayecto | PUT | Update  | [URL_BASE]/trayecto/\<id> |
| Trayecto | DELETE | Delete  | [URL_BASE]/trayecto/\<id> |
| Bus | GET | Select All | [URL_BASE]/bus/all |
| Bus | GET | Select  | [URL_BASE]/bus/\<id> |
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

METHOD = GET
```
    {}
```

### Update
URL = [URL_BASE]/chofer/1

METHOD = PUT
```
    {
        "nombre": "Josue",
        "apellido": "Angelo",
        "rut": "17467125-2"
    }
```
