# JSONServer + JWT Auth

A Fake REST API using json-server with JWT authentication. You can find the [complete tutorial here](https://www.techiediaries.com/fake-api-jwt-json-server/)

For Angular 2+ apps: 
* Copy db.json and server.js to root project
* Add "api-auth": "node server.js" to package.json file


## Install

```bash
$ npm install
$ npm run api-auth
```

## How to login?

You can login by sending a POST request to

```
POST http://localhost:3000/auth/login
```
with the following data 

```
{
  "email": "admin@admin.com",
  "password":"admin"
}
```

You should receive an access token with the following format 

```
{
   "access_token": "<ACCESS_TOKEN>"
}
```


You should send this authorization with any request to the protected endpoints

```
Authorization: Bearer <ACCESS_TOKEN>
```

## How to get movies from db.json file?

GET http://localhost:3000/movies
Add to headers Bearer Token