# JSONServer + JWT Auth

A Fake REST API using json-server with JWT authentication.

Implemented endpoint: login,register

## Install

```bash
$ npm install
$ npm run start-auth
```

Might need to run

```
npm audit fix
```

## How to login?

You can sessions by sending a POST request to

```
POST http://localhost:3333/sessions
POST http://localhost:3333/auth/register
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
