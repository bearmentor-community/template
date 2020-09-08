# Template API Specifications

> For specific documentation, visit [azobu-projects/template-api](https://github.com/azobu-projects/template-api).

The resources and endpoints are configured using Express middlewares. CORS (Cross-Origin Resource Sharing) is enabled because the web and API run on a different host and port.

Available resources:

- [Common](#common-)
- [Auth](#auth-)
- [Users](#users-)
- [Items](#items-)
- [Images](#images-)
- [Search](#search-)

Each resources are connected to data model or layer using ORM (Object-Relational Mapper) or ODM (Object Document Mapper):

- Mongoose models that connected to MongoDB
- Sequelize models that connected to PostgreSQL or MySQL

The request and response object should set `Content-Type` as `application/json`. Some request set `Content-Type` as `multipart/form-data` when uploading file(s).

Each endpoint has:

- Path: Relative path to the endpoint
- Method: HTTP methods (`GET`, `POST`, `PUT`, `PATCH`, `DELETE`)
- Description: Brief explanation
- Params: `/:params`
- Query: `/path?query=value`
- Headers: HTTP headers (`Content-Type`, `Authorization`)
- Available: Whether the API already or should be implemented in Template API

## Common [🔝](#template-api-specifications)

Resources for commonly used data and special functions.

Endpoints:

| Path | Method   | Description         | Params | Query             | Headers | Available?  |
| ---- | -------- | ------------------- | ------ | ----------------- | ------- | ----------- |
| `/`  | `GET`    | Get welcome message | -      | -                 | -       | `available` |
| `/`  | `DELETE` | Reset everything    | -      | `resetEverything` | -       | `available` |

> ⚠️ You can remove the "reset everything" functionality if you don't need it.

Object structure:

| Field       | Type        | Description                                 |
| ----------- | ----------- | ------------------------------------------- |
| `id`        | `number`    | Generated automatically by auto incrementer |
| `_id`       | `ObjectId`  | Generated automatically by MongoDB          |
| `createdAt` | `timestamp` | Generated automatically by ORM/ODM          |
| `updatedAt` | `timestamp` | Generated automatically by ORM/ODM          |

Object data:

```json
{
  "id": 0,
  "_id": "abc",
  "createdAt": "",
  "updatedAt": ""
}
```

## Auth [🔝](#template-api-specifications)

Resources for authentication and authorization that includes registration, login, logout, and get authenticated user profile.

Endpoints:

| Path             | Method | Description                    | Params | Query | Headers         | Available?  |
| ---------------- | ------ | ------------------------------ | ------ | ----- | --------------- | ----------- |
| `/auth/register` | `POST` | Register new user              | -      | -     | -               | `available` |
| `/auth/login`    | `POST` | Login to user                  | -      | -     | -               | `available` |
| `/auth/logout`   | `GET`  | Logout from user               | -      | -     | `Authorization` | `available` |
| `/auth/profile`  | `GET`  | Get authenticated user profile | -      | -     | `Authorization` | `available` |

Object structure:

| Field      | Type     | Description       |
| ---------- | -------- | ----------------- |
| `name`     | `string` | Initial full name |
| `username` | `string` | Initial username  |
| `email`    | `string` | Initial email     |
| `password` | `string` | Initial password  |

Object data:

```json
{
  "name": "M Haidar Hanif",
  "username": "mhaidarhanif",
  "email": "name@example.com",
  "password": "********"
}
```

## Users [🔝](#template-api-specifications)

Resources for managing users.

Endpoints:

| Path                  | Method   | Description                | Params     | Query | Headers     | Available?  |
| --------------------- | -------- | -------------------------- | ---------- | ----- | ----------- | ----------- |
| `/users`              | `GET`    | Get all users              | -          | -     | -           | `available` |
| `/users/seed`         | `POST`   | Seed initial users         | -          | -     | `X-API-Key` | `available` |
| `/users/count`        | `GET`    | Get count of all users     | -          | -     | -           | `available` |
| `/users/:username`    | `GET`    | Get user by username       | `username` | -     | -           | `available` |
| `/users/:id/settings` | `GET`    | Get user settings by id    | `id`       | -     | -           | `available` |
| `/users/:id/settings` | `PUT`    | Update user settings by id | `id`       | -     | -           | `available` |
| `/users`              | `DELETE` | Delete all users           | -          | -     | -           | `available` |
| `/users/:id`          | `DELETE` | Delete user by id          | `id`       | -     | -           | `available` |

Object structure:

| Field       | Type     | Description                           |
| ----------- | -------- | ------------------------------------- |
| `name`      | `string` | User's name                           |
| `username`  | `string` |                                       |
| `email`     | `string` |                                       |
| `bio`       | `string` | Editable through update user profile  |
| `hash`      | `string` | Encrypted `password`                  |
| `salt`      | `string` |                                       |
| `avatarUrl` | `string` | Generated automatically               |
| `roles`     | `string` | Assigned automatically                |
| `url`       | `string` | Generated automatically by `username` |

Object data:

```json
{
  "id": 0,
  "_id": "abc",
  "name": "M Haidar Hanif",
  "username": "mhaidarhanif",
  "email": "name@example.com",
  "bio": "Educator, Engineer, Explorer. Write everything education and tech.",
  "avatarUrl": "https://api.template.azobu.com/uploads/mhaidarhanif_123.jpg",
  "roles": ["user"],
  "url": "https://template.azobu.com/mhaidarhanif",
  "createdAt": "",
  "updatedAt": ""
}
```

## Items [🔝](#template-api-specifications)

Resources for managing items.

Endpoints:

| Path           | Method   | Description        | Params | Query | Headers     | Available?  |
| -------------- | -------- | ------------------ | ------ | ----- | ----------- | ----------- |
| `/items`       | `GET`    | Get all items      | -      | -     | -           | `available` |
| `/items/seed`  | `POST`   | Seed initial items | -      | -     | `X-API-Key` | `available` |
| `/items/:slug` | `GET`    | Get item by slug   | `slug` | -     | -           | `available` |
| `/items`       | `DELETE` | Delete all items   | -      | -     | -           | `available` |

Object structure:

- `slug`
- `imageUrl`
- `title`
- `html`

Object data:

```json
{
  "id": 0,
  "_id": "abc",
  "url": "https://template.azobu.com/items/iron-man-suit",
  "slug": "iron-man-suit",
  "imageUrl": "images/iron-man-suit.jpg",
  "title": "Iron Man Suit",
  "contentFormat": "html",
  "content": "<p><a href='/ironman'>Tony Stark</a>'s Iron Man suits are ...</p>",
  "createdAt": "",
  "updatedAt": ""
}
```

## Images [🔝](#template-api-specifications)

Resources for managing uploaded images.

Endpoints:

| Path             | Method | Description      | Params | Query | Headers         | Available?  |
| ---------------- | ------ | ---------------- | ------ | ----- | --------------- | ----------- |
| `/images`        | `GET`  | Get all images   | -      | -     | -               | -           |
| `/images/upload` | `POST` | Upload new image | -      | -     | `Authorization` | `available` |

Supported image content types:

- `image/jpeg`
- `image/png`
- `image/gif`

Object structure:

- `name`: Just the file name with extension
- `url`: Complete URL to the asset
- `path`: Relative path to the disk or file system (if any)
- `title`

Object data:

```json
{
  "id": 0,
  "_id": "abc",
  "name": "",
  "url": "",
  "path": "",
  "createdAt": "",
  "updatedAt": ""
}
```

## Search [🔝](#template-api-specifications)

Resources for searching other resources.

| Path            | Method | Description           | Params | Query     | Headers | Available?  |
| --------------- | ------ | --------------------- | ------ | --------- | ------- | ----------- |
| `/search`       | `GET`  | Get index of search   | -      | -         | -       | -           |
| `/search/users` | `GET`  | Search users by query | -      | `keyword` | -       | -           |
| `/search/items` | `GET`  | Search items by query | -      | `keyword` | -       | `available` |

Query structure:

- `keyword`: Keyword to search for
