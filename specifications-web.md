# Template Web Specifications

Web pages are configured using React Router and integrated into Redux with Connected React Router.

The designs are

## Public Pages

| Path           | Component         | Description         | Environment   |
| -------------- | ----------------- | ------------------- | ------------- |
| `/`            | `PageHome`        | Home                | -             |
| `/about`       | `PageAbout`       | About               | -             |
| `/users`       | `PageUsers`       | All users           | -             |
| `/:slug`       | `PageUserProfile` | Single user profile | -             |
| `/items`       | `PageItems`       | All items           | -             |
| `/items/:slug` | `PageItem`        | Single item detail  | -             |
| `/register`    | `PageRegister`    | Register new user   | -             |
| `/login`       | `PageLogin`       | Login user          | -             |
| `/logout`      | `PageLogout`      | Logout user         | -             |
| `/settings`    | `PageSettings`    | User settings       | -             |
| `/404`         | `PageNotFound`    | Not found           | `development` |
| `/upload`      | `PageUpload`      | Upload mode         | `development` |
| `/debug`       | `PageDebug`       | Debug mode          | `development` |

## Admin Pages

| Path               | Component      | Description       | Environment |
| ------------------ | -------------- | ----------------- | ----------- |
| `/`                | `PageHome`     | Home              | -           |
| `/404`             | `PageNotFound` | Not found         | -           |
| `/users`           | `PageUsers`    | All users         | -           |
| `/users/:username` | `PageUser`     | Single user info  | -           |
| `/items`           | `PageItems`    | All items         | -           |
| `/items/:slug`     | `PageItem`     | Single item info  | -           |
| `/images`          | `PageImages`   | All images        | -           |
| `/images/:slug`    | `PageImage`    | Single image info | -           |
| `/login`           | `PageLogin`    | Login user        | -           |
| `/logout`          | `PageLogout`   | Logout user       | -           |
