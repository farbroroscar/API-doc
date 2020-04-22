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

###### Command:
```sh
curl http://api.softhouse.rocks/users
```

###### Example of body data response:
  (each userobject lies in an array.) 

```json
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
´´´


```sh
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
´´´

###### Result code: 200 OK

---

#### POST
###### Description: 
Posts a user to the API

###### Command: 
curl -i -X POST -H "Content-Type:application/json" http://api.softhouse.rocks/users -d 
  '{
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
    "name": "Nisse",
    "username": "Kamren",
    "email": "Lucio_Hettinger@annie.ca",
    "__v": 0
  }'

###### Example of body data request:

###### Result code: 201 created


### /users/userId

#### GET
###### Description: 
Fetches the data of the chosen user

###### Command:

###### Example of body data request:
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

###### Result code: 

#### PUT
###### Description: 
Replaces the chosen user with what is passed in.

###### Command:
curl

###### Example of body data request: 

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
  "_id": "5e9ed9803c9c34a2d807f91b",
  "id": 14,
  "__v": 0,
  "email": "string",
  "name": "string",
  "username": "hej"
}

###### Result code: 200



## /posts

#### GET
###### Description:
###### Command:
###### Example of body data request:
###### Result code:

#### POST
###### Description:
###### Command:
###### Example of body data request:
###### Result code:



### /posts/postId

#### GET
###### Description:
Fetches the chosen post

###### Command:
curl -H "Content-Type:application/json" http://api.softhouse.rocks/posts/1 | jq

###### Example of body request data:

###### Result code:

#### PATCH
###### Description: 
Updates chosen post only with the input

###### Command:
curl -X PATCH "https://api.softhouse.rocks/posts/10" -H  "accept: application/json" -H  "Content-Type: application/json" -d "{\"title\":\"this is a title\",\"body\":\"string\",\"userId\":5}"

###### Example of body data request: 
{
  "n":1,
  "nModified":0,
  "opTime": {
    "ts":"6818118904313806849",
    "t":136
  },
  "electionId":"7fffffff0000000000000088",
  "ok":1,
  "operationTime":"6818118904313806849",
  "$clusterTime": {
    "clusterTime":"6818118904313806849",
    "signature": {
      "hash":"AAAAAAAAAAAAAAAAAAAAAAAAAAA=",
      "keyId":0
    }
  }
}

###### Result code: 

#### PUT
###### Description:
###### Command:
###### Example of body data request:
###### Result code:

#### DELETE
###### Description:
###### Command:
###### Example of body data request:
###### Result code:




