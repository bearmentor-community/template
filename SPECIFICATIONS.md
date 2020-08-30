# Template Spec

Specifications for all of the web application and API.

## Web Pages

Pages are configured using React Router.

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

Endpoints are configured using Express middlewares.

| Endpoint | Method | Description         | Query | Headers |
| -------- | ------ | ------------------- | ----- | ------- |
| `/`      | `GET`  | Get root of the API | -     | -       |

### Auth

| Endpoint         | Method | Description       | Query | Headers         |
| ---------------- | ------ | ----------------- | ----- | --------------- |
| `/auth/register` | `POST` | Register new user | -     | -               |
| `/auth/login`    | `POST` | Login to user     | -     | -               |
| `/auth/logout`   | `GET`  | Logout from user  | -     | `Authorization` |

### Users

| Endpoint | Method | Description   | Query | Headers |
| -------- | ------ | ------------- | ----- | ------- |
| `/users` | `GET`  | Get all users | -     | -       |

### Items

| Endpoint | Method | Description   | Query | Headers |
| -------- | ------ | ------------- | ----- | ------- |
| `/items` | `GET`  | Get all items | -     | -       |

### Images

| Endpoint  | Method | Description    | Query | Headers |
| --------- | ------ | -------------- | ----- | ------- |
| `/images` | `GET`  | Get all images |       | -       |

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
  "bio": "Educator, Engineer, Explorer. Write everything education and tech.",,
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
