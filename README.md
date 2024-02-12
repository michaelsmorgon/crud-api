# CRUD API

#### [Assignment: Simple CRUD API](https://github.com/AlreadyBored/nodejs-assignments/blob/main/assignments/crud-api/assignment.md)

---

#### Installation

```
$ git clone https://github.com/michaelsmorgon/crud-api.git
```

```
$ npm install
```

#### Configuration

Server port can be changed in .env file. (By default 4000)

#### Scripts

```
$ npm run start:dev
```

```
$ npm run start:prod
```

#### Endpoints description

1. `api/users`:
   - **GET** `api/users` is used to get all persons
     - Response with: `status code` **200** and all users records
   - **GET** `api/users/${userId}`
     - Response with: `status code` **200** and and record with `id === userId` if it exists
     - Response with: `status code` **400** and message `Invalid user id` if provided id is not valid uuid
     - Response with: `status code` **404** and message `User with id {provided_id} not found`
   - **POST** `api/users` is used to create record about new user and store it in database
     - Response with: `status code` **201** and newly created record
     - Response with: `status code` **400** and message `Invalid user data` if request `body` does not contain **required** fields
   - **PUT** `api/users/{userId}` is used to update existing user
     - Response with: ` status code` **200** and updated record
     - Response with: ` status code` **400** and message `Invalid user id` if provided id is not valid uuid
     - Response with: ` status code` **404** and and message `User with id {provided_id} not found`
   - **DELETE** `api/users/${userId}` is used to delete existing user from database
     - Response with: `status code` **204** if the record is found and deleted
     - Response with: ` status code` **400** and message `Invalid user id` if provided id is not valid uuid
     - Response with: ` status code` **404** and and message `User with id {provided_id} not found`
