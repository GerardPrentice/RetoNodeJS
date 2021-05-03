# Reto Api NODEJS con Serverless, conexion a MONGODB

## Inicio

```
npm install
serverless deploy
```

## Endpoints en caso se despliegue

*Create*

```bash
curl -XPOST -H "Content-type: application/json" -d '{
   "name" : "John",
   "firstname" : "Doe",
   "city" : "Toronto",
   "birth" : "01/01/1990"
}' 'URL del lambda/dev/user/'
```
```json
{"id": "590b52ff086041000142cedd"}
```

*READ*

```bash
curl -XGET -H "Content-type: application/json" 'URL del lambda/dev/user/590b52ff086041000142cedd'
```
```json
[
  {
    "_id": "5905e2fbdb55f20001334b3e",
    "name": "John",
    "firstname": "Doe",
    "birth": null,
    "city": "Toronto",
    "ip": "01/01/1990",
    "__v": 0
  }
]
```

*UPDATE*

```bash
curl -XPUT -H "Content-type: application/json" -d '{
   "name" : "William",
   "firstname" : "Smith",
   "city" : "Miami",
   "birth" : "01/01/2000"
}' 'URL del lambda/dev/user/590b52ff086041000142cedd'
```
```json
"Ok"
```

*DELETE*

```bash
curl -XDELETE -H "Content-type: application/json" 'URL del lambda/dev/user/590b52ff086041000142cedd'
```

```json
"Ok"
```
