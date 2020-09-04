# Template Specifications

Specifications for all of the web application and API.

## Table of Contents

- Introduction
- [Tech Stack](#tech-stack)
- [Web Pages](#web-pages)
- [Data Structure](#data-structure)

## Tech Stack

- HTML, CSS, JavaScript
- Node.js
- React
- Redux
- Express
- MongoDB
- PostgreSQL
- Nginx
- PM2

## Web Pages

Pages are configured using React Router and integrated into Redux with Connected React Router.

### Web

| Path           | Component         | Description         | Environment   |
| -------------- | ----------------- | ------------------- | ------------- |
| `/`            | `PageHome`        | Home                |               |
| `/404`         | `PageNotFound`    | Not found           |               |
| `/about`       | `PageAbout`       | About               |               |
| `/users`       | `PageUsers`       | All users           |               |
| `/:slug`       | `PageUserProfile` | Single user profile |               |
| `/items`       | `PageItems`       | All items           |               |
| `/items/:slug` | `PageItem`        | Single item detail  |               |
| `/register`    | `PageRegister`    | Register new user   |               |
| `/login`       | `PageLogin`       | Login user          |               |
| `/logout`      | `PageLogout`      | Logout user         |               |
| `/settings`    | `PageSettings`    | User settings       |               |
| `/debug`       | `PageDebug`       | Debug mode          | `development` |
| `/upload`      | `PageUpload`      | Upload mode         | `development` |

### Admin

| Path               | Component      | Description       | Environment |
| ------------------ | -------------- | ----------------- | ----------- |
| `/`                | `PageHome`     | Home              |             |
| `/404`             | `PageNotFound` | Not found         |             |
| `/users`           | `PageUsers`    | All users         |             |
| `/users/:username` | `PageUser`     | Single user info  |             |
| `/items`           | `PageItems`    | All items         |             |
| `/items/:slug`     | `PageItem`     | Single item info  |             |
| `/images`          | `PageImages`   | All images        |             |
| `/images/:slug`    | `PageImage`    | Single image info |             |
| `/login`           | `PageLogin`    | Login user        |             |
| `/logout`          | `PageLogout`   | Logout user       |             |

## API Endpoints

Endpoints are configured using Express middlewares. Each of them could configured with either:

- Mongoose models that connected to MongoDB
- Sequelize models that connected to PostgreSQL or MySQL

### Common

| Endpoint | Method   | Description         | Params | Query             | Headers | Available |
| -------- | -------- | ------------------- | ------ | ----------------- | ------- | --------- |
| `/`      | `GET`    | Get welcome message | -      | -                 | -       | YES       |
| `/`      | `DELETE` | Reset everything    | -      | `resetEverything` | -       | YES       |

### Auth

| Endpoint         | Method | Description                    | Params | Query | Headers         | Available |
| ---------------- | ------ | ------------------------------ | ------ | ----- | --------------- | --------- |
| `/auth/register` | `POST` | Register new user              | -      | -     | -               | YES       |
| `/auth/login`    | `POST` | Login to user                  | -      | -     | -               | YES       |
| `/auth/logout`   | `GET`  | Logout from user               | -      | -     | `Authorization` | YES       |
| `/auth/profile`  | `GET`  | Get authenticated user profile | -      | -     | `Authorization` | YES       |

### Users

| Endpoint              | Method   | Description                | Params     | Query | Headers     | Available |
| --------------------- | -------- | -------------------------- | ---------- | ----- | ----------- | --------- |
| `/users`              | `GET`    | Get all users              | -          | -     | -           | YES       |
| `/users/seed`         | `POST`   | Seed initial users         | -          | -     | `X-API-Key` | YES       |
| `/users/count`        | `GET`    | Get count of all users     | -          | -     | -           | YES       |
| `/users/:username`    | `GET`    | Get user by username       | `username` | -     | -           | YES       |
| `/users/:id/settings` | `GET`    | Get user settings by id    | `id`       | -     | -           | YES       |
| `/users/:id/settings` | `PUT`    | Update user settings by id | `id`       | -     | -           | YES       |
| `/users`              | `DELETE` | Delete all users           | -          | -     | -           | YES       |
| `/users/:id`          | `DELETE` | Delete user by id          | `id`       | -     | -           | YES       |

### Items

| Endpoint       | Method   | Description        | Params | Query | Headers | Available |
| -------------- | -------- | ------------------ | ------ | ----- | ------- | --------- |
| `/items`       | `GET`    | Get all items      | -      | -     | -       | YES       |
| `/items/seed`  | `POST`   | Seed initial items | -      | -     | -       | YES       |
| `/items/:slug` | `GET`    | Get item by slug   | `slug` | -     | -       | YES       |
| `/items`       | `DELETE` | Delete all items   | -      | -     | -       | YES       |

### Images

| Endpoint         | Method | Description      | Params | Query | Headers         | Available |
| ---------------- | ------ | ---------------- | ------ | ----- | --------------- | --------- |
| `/images`        | `GET`  | Get all images   | -      | -     | -               | -         |
| `/images/upload` | `POST` | Upload new image | -      | -     | `Authorization` | YES       |

### Search

| Endpoint        | Method | Description           | Params | Query     | Headers | Available |
| --------------- | ------ | --------------------- | ------ | --------- | ------- | --------- |
| `/search`       | `GET`  | Get root of search    | -      | -         | -       | -         |
| `/search/items` | `GET`  | Search items by query | -      | `keyword` | -       | YES       |

## Data Structure

### Users

```json
{
  "id": 0,
  "_id": "abc",
  "createdAt": "",
  "updatedAt": "",
  "roles": ["user", "admin"],
  "avatarUrl": "https://api.template.azobu.com/uploads/mhaidarhanif_123.jpg",
  "name": "M Haidar Hanif",
  "username": "mhaidarhanif",
  "email": "name@example.com",
  "bio": "Educator, Engineer, Explorer. Write everything education and tech.",
  "links": [
    {
      "title": "Website",
      "url": "https://mhaidarhanif.com"
    },
    {
      "title": "Twitter",
      "url": "https://twitter.com"
    }
  ]
}
```

### Items

```json
{
  "id": 0,
  "_id": "abc",
  "createdAt": "",
  "updatedAt": ""
}
```

### Images

```json
{
  "id": 0,
  "_id": "abc",
  "createdAt": "",
  "updatedAt": "",
  "url": "",
  "path": ""
}
```
