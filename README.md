# API-doc


-i, --include       Include protocol response headers in the output
-H, --header <header/@file> Pass custom header(s) to server
| jq
| code . 


## Endpoints and methods

### http://api.softhouse.rocks

* /users
  * Available http methods: GET, POST

* /users/{usersId}
  * Available http methods: GET, PUT

* /posts
  * Available http methods: GET, POST

* /posts/{postsId}
  * Available http methods: GET, PUT, PATCH, DELETE

---

## /users

### GET
#### Description: 
Fetches all the users

#### Command:
```sh
curl http://api.softhouse.rocks/users
```

#### Example of body data response:
  Each userobject lies in an an object in the array.

```javascript
[
 {
    "address": {
      "geo": {
        "lat": -31.8129,
        "lng": 62.5342
      },
      "street": "Skiles Walks",
      "suite": "Suite 351",
      "city": "Roscoeview",
      "zipcode": "33263"
    },
    "_id": "5e806d9f42fbde006b6b9ec9",
    "id": 5,
    "name": "Chelsey Dietrich",
    "username": "Kamren",
    "email": "Lucio_Hettinger@annie.ca",
    "__v": 0
  },
] 
```

#### Result code: 200 OK 
<br/>
<br/>




### POST
#### Description: 
Posts a user to the API

#### Command: 
```sh
curl -X POST -H "Content-Type:application/json" http://api.softhouse.rocks/users -d '{"name": "string","username":"string","email": "string","address": {"street": "string","suite": "string","city": "string","zipcode": "string","geo": {"lat": 0,"lng": 0}}}'
```

#### Example of body data request:
```json
{
  "address": {
    "geo": {
      "lat": 0,
      "lng": 0
    },
    "street": "string",
    "suite": "string",
    "city": "string",
    "zipcode": "string"
  },
  "_id": "5e9ff081619a44002135097a",
  "name": "string",
  "username": "string",
  "email": "string",
  "id": 1,
  "__v": 0
}
```

#### Result code: 201 created

---

## /users/userId

### GET
#### Description: 
Fetches the data of the chosen user

#### Command:
```sh
curl http://api.softhouse.rocks/users/10
```

#### Example of body data request:
```json
{
  "address": {
    "geo": {
      "lat": 0,
      "lng": 0
    },
    "street": "string",
    "suite": "string",
    "city": "string",
    "zipcode": "string"
  },
  "_id": "5e806d9f42fbde006b6b9ece",
  "id": 10,
  "name": "string",
 
"username": "string",
  "email": "string",
  "__v": 0
}
```

#### Result code: 200 OK
___


### PUT
#### Description: 
Replaces the chosen user with what is passed in. In example below, no email is passed in and 
body data response shows email: null.

#### Command:
```sh
curl -X PUT "https://api.softhouse.rocks/users/382" -H  "accept: application/json" -H  "Content-Type: application/json" -d "{\"name\":\"emma\",\"username\":\"hej\",\"address\":{\"street\":\"string\",\"suite\":\"string\",\"city\":\"string\",\"zipcode\":\"string\",\"geo\":{\"lat\":0,\"lng\":0}}}"
```

#### Example of body data response: 
```json
{
  "address": {
    "geo": {
      "lat": 0,
      "lng": 0
    },
    "street": "string",
    "suite": "string",
    "city": "string",
    "zipcode": "string"
  },
  "_id": "5e9ff081619a44002135097a",
  "name": "emma",
  "username": "hej",
  "email": null,
  "id": 382,
  "__v": 0
}
```


#### Result code: 200

---

## /posts

