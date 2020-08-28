# Specifications

## Web Pages

| Path           | Component         | Description         | Environment   |
| -------------- | ----------------- | ------------------- | ------------- |
| `/`            | `PageHome`        | Home                |               |
| `/404`         | `PageNotFound`    | Not found           |               |
| `/about`       | `PageAbout`       | About               |               |
| `/users`       | `PageUsers`       | All users           |               |
| `/:slug`       | `PageUserProfile` | Single user profile |               |
| `/items`       | `PageItems`       | All items           |               |
| `/items/:slug` | `PageItemDetail`  | Single item detail  |               |
| `/register`    | `PageRegister`    | Register new user   |               |
| `/login`       | `PageLogin`       | Login user          |               |
| `/logout`      | `PageLogout`      | Logout user         |               |
| `/settings`    | `PageSettings`    | User settings       |               |
| `/debug`       | `PageDebug`       | Debug mode          | `development` |
| `/upload`      | `PageUpload`      | Upload mode         | `development` |

## API Endpoints

| Endpoint | Method | Description | Query | Headers |
| -------- | ------ | ----------- | ----- | ------- |
| `/`      | `GET`  | Get index   | -     | -       |

### Auth

| Endpoint         | Method | Description       | Query | Headers         |
| ---------------- | ------ | ----------------- | ----- | --------------- |
| `/auth/register` | `POST` | Register new user | -     | -               |
| `/auth/login`    | `POST` | Login to user     | -     | -               |
| `/auth/logout`   | `GET`  | Logout from user  | -     | `Authorization` |

### Users

| Endpoint | Method | Description   | Query       | Headers |
| -------- | ------ | ------------- | ----------- | ------- |
| `/users` | `GET`  | Get all users | `paginated` | -       |

### Items

| Endpoint | Method | Description   | Query       | Headers |
| -------- | ------ | ------------- | ----------- | ------- |
| `/items` | `GET`  | Get all items | `paginated` | -       |

### Images

| Endpoint  | Method | Description    | Query       | Headers |
| --------- | ------ | -------------- | ----------- | ------- |
| `/images` | `GET`  | Get all images | `paginated` | -       |

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
