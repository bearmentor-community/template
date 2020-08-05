# Specifications

## Web Pages

| Path        | Component  | Description          |
| ----------- | ---------- | -------------------- |
| `/`         | `Home`     | Homepage             |
| `/404`      | `NotFound` | Page not found       |
| `/about`    | `About`    | About                |
| `/register` | `Register` | Register as new user |
| `/login`    | `Login`    | Login to user        |
| `/logout`   | `Logout`   | Logout from user     |

## API Endpoints

| Endpoint         | Method | Description       | Query       | Headers         |
| ---------------- | ------ | ----------------- | ----------- | --------------- |
| `/`              | `GET`  | Get index         | -           | -               |
| `/auth/register` | `POST` | Register new user | -           | -               |
| `/auth/login`    | `POST` | Login to user     | -           | -               |
| `/auth/logout`   | `GET`  | Logout from user  | -           | `Authorization` |
| `/users`         | `GET`  | Get all users     | `paginated` | -               |

## Data Structure

### Users

```json
{
  "id": 0,
  "_id": "abc",
  "createdAt": "",
  "updatedAt": "",
  "avatarUrl": "https://api.template.azobu.com/uploads/mhaidarhanif_123.jpg",
  "name": "M Haidar Hanif",
  "username": "mhaidarhanif",
  "email": "name@example.com",
  "roles": ["user", "admin"],
  "bio": {
    "short": "Educator, Engineer, Explorer. Write everything education and tech.",
    "long": "Haidar is a seasoned tech educator and engineer in the world of software engineering and web development. Currently he focuses on helping people to start and grow their career in the modern software industry."
  },
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
