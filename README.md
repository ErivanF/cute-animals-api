# Description

A Nest.JS API to upload and get cute animals pictures

## Technologies

Nest.js
Typescript
Docker
Mongoose
MongoDB

## Endpoints

## User

### Create user

Creates a new user

```http
/user
```

Method: POST

Authentication: None

Body:

```JSON
{
  "username": "myUsername",
  "password": "myPassword",
}
```

Response:
Status: 200

```JSON
{
  "id": "1q2w3e4r",
  "username": "myUsername",
  "isAdmin": false
}
```

### Login

Gets an authentication token

```http
/user/login
```

Method: POST

Authentication: None

Body:

```JSON
{
  "username": "myUsername",
  "password": "myPassword",
}
```

Response:
Status: 200

```JSON
{
  "authentication": "Bearer <token>"
}
```

### Profile

Gets the data for the logged user

```http
/user
```

Method: GET

Authentication: Bearer token

Body:

Response:
Status: 200

```JSON
{
  "id": "1q2w3e4r",
  "username": "myUsername",
  "isAdmin": false
}
```

### User List

Gets a list of users

```http
/user/list
```

Method: GET

Authentication: Bearer token

Body:

Response:
Status: 200

```JSON
[
  {
  "id": "1q2w3e4r",
  "username": "myUsername",
  "isAdmin": false
  }
]
```

## Project setup

```bash
 npm install
```

## Compile and run the project

```bash
# development
$ npm run start

# watch mode
$ npm run start:dev

# production mode
$ npm run start:prod
```

## Run tests

```bash
# unit tests
$ npm run test

# e2e tests
$ npm run test:e2e

# test coverage
$ npm run test:cov
```

## Deployment

When you're ready to deploy your NestJS application to production, there are some key steps you can take to ensure it runs as efficiently as possible. Check out the [deployment documentation](https://docs.nestjs.com/deployment) for more information.

If you are looking for a cloud-based platform to deploy your NestJS application, check out [Mau](https://mau.nestjs.com), our official platform for deploying NestJS applications on AWS. Mau makes deployment straightforward and fast, requiring just a few simple steps:

```bash
$ npm install -g mau
$ mau deploy
```

With Mau, you can deploy your application in just a few clicks, allowing you to focus on building features rather than managing infrastructure.
