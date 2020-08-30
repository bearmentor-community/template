# ⭕ Template

> Template is a quick starter kit project to build a complete web app and API.

You can access the production version of the applications here:

- [Template Web](https://template.azobu.com)
- [Template API](https://api.template.azobu.com)
- (Later) Template Android
- (Later) Template iOS

## Table of Contents

- Introduction
- [Highlighted Features](#highlighted-features)
- [Repositories](#repositories)
- [Inspirations](#inspirations)
- [Designs](#designs)
- [Authors](#authors)
- [License](#license)

## Highlighted Features

- Highly opiniated structure to start a project faster
  - Focused on JavaScript, Node.js, and React ecosystem. Maybe later with TypeScript too
- Communication with popular and standard HTTP-based API
  - Powered by REST API. Maybe later by GraphQL API too
- Simple UI and quick UX with expressive states
  - Powered by React Router and Redux
- Frontend and backend documentations
  - Leveraged by simple table for web pages and API endpoints
- Optimized developer experience (DX) through npm/yarn scripts
  - Leveraged by `package.json` and PM2 with `ecosystem.config.js`
  - Automated deployment by Netlify and Circle CI
- Watch changes with hot reload for React and auto restart for Node.js
  - Powered by React Scripts (Webpack and Babel), Nodemon, and PM2
- Flexible customizable interface with color theme, especially dark mode
  - Powered by `xstyled` and Emotion
  - Not using premade design from Bootstrap or Material Design
- Better debugging experience for global app state and local form state
  - Powered by Redux Logger, Redux DevTools Extension, and React Hook Form
  - (Alternative) Added by Formik or React Final Form
- Get and display data resources such as users and items
  - Powered by Axios, Redux Thunk, and `async`/`await` for asynchronous handling
- Adaptive page title based on location path and data condition
  - Powered by React Helmet Async and nice favicons
- Search items with adapted browser URL query
  - Powered by combination of Redux, React Router, and `query-string`
- Authentic and cool-looking initial seed users and items
  - Sourced from Marvel universe's characters and items
- Log HTTP API requests
  - Powered by `morgan` Express middleware
- Easy to use database technologies
  - Powered by MongoDB with Mongoose or PostgreSQL with Sequelize
- Simple user authentication and authorization flow with basic security
  - Powered by Web Storage API, Express, `bcrypt`, and JSON Web Token (JWT), Express CORS, and Helmet
  - Not using Passport for basic email and password
- Proper response of message and error
  - Using Express middlewares with advised HTTP response status
- Edit user profile and upload pictures
  - Powered by `multer` Express middleware using `FormData`
  - (Alternative) Separated storage engine for static assets:
    - Google Storage Engine
    - Cloudinary
- Multi environment configurations and variables for development, test, and production
  - Powered by React Scripts and `dotenv-flow` to manage `.env` files
- Vibrant utilities for various case of other features:
  - `dayjs` date parser
  - HTML string parser
  - Image or component lazy loader
  - WYSIWYG editor
  - (Later) Markdown editor
  - (Later) Code syntax highlighter
- Helpful analytical data
  - Powered by Google Analytics and React-GA
- Static test with linter and code formatter
  - Powered by ESLint, Prettier, and Standard
- Automated test suite with end-to-end test, integration test, unit test, and test coverage
  - (Later) Powered by Cypress, Jest, Sinon, React Testing Library, and `supertest`/`supertest-fetch`
- Send email for account confirmation and password reset link
  - Powered by Nodemailer and Mailgun
- Interactive documentation of the API endpoints
  - (Later) Powered by Postman/`newman`, Swagger, or API Blueprint
- Reliable secure server hosting and configuration
  - Powered by Netlify, Google Cloud Platform, Nginx, Let's Encrypt, Cloudflare, and Uniregistry
- Intuitive CI/CD (Continuous Integration and Deployment) tools
  - Powered by Netlify CI and Circle CI
- (Later) Dedicated administrator dashboard for data management and visualization
  - Powered by D3.js
- (Later) Periodic dependency cleaning and vulnerability monitoring by Greenkeeper and Snyk
- (Later) Offline-first mode powered by Progressive Web App (PWA)
- (Later) Consultation with the developers
- (Later) Explanation with videos

Some stack alternatives are listed in each repository's documentation.

## Repositories

- [`template`](https://github.com/azobu-projects/template)
- [`template-web`](https://github.com/azobu-projects/template-web)
- [`template-api`](https://github.com/azobu-projects/template-api)

[See the spefications here](./SPECIFICATIONS.md).

## Inspirations

This project is inspired by:

- [Material Design Kit](https://materialdesignkit.com)
- [RealWorld.io](https://github.com/gothinkster/realworld)
  - [`react-redux-realworld`](https://github.com/gothinkster/react-redux-realworld-example-app)
  - [`node-express-realworld`](https://github.com/gothinkster/node-express-realworld-example-app)
- [React.js Boilerplate](https://reactboilerplate.com)
- [Express application generator](https://expressjs.com/en/starter/generator.html)

But instead of taking different programming ecosystem at once, Template is made to be highly opiniated for just around JavaScript and Node.js because the main goal is to be a quick starter kit.

Ultimately this base application is adapted into other apps:

- [The Galactic News](https://thegalacticnews.azobu.com) news portal
- [Earthling](https://earthling.azobu.com) social media
- [Planetary](https://planetary.azobu.com) job board
- [Jankenpon](https://jankenpon.azobu.com) rock-paper-scissors game

Actively updated too during 2020, unlike the others which already stopped more than 2 years.

## Designs

Access the original assets on Figma:

- Design: https://figma.com/file/gyEXMrNXwVEBfdrSkJlJYV/Template?node-id=450%3A2
- Prototype: https://figma.com/proto/gyEXMrNXwVEBfdrSkJlJYV/Template?node-id=452%3A2&scaling=min-zoom

### Preview of the Pages

| Name           | Screenshots                                  |
| -------------- | -------------------------------------------- |
| Home           | ![](screenshots/template-home.jpg)           |
| Home Dark      | ![](screenshots/template-home-dark.jpg)      |
| About          | ![](screenshots/template-about.jpg)          |
| Not Found      | ![](screenshots/template-not-found.jpg)      |
| Users          | ![](screenshots/template-users.jpg)          |
| User Profile   | ![](screenshots/template-user-profile.jpg)   |
| Items          | ![](screenshots/template-items.jpg)          |
| Item           | ![](screenshots/template-item.jpg)           |
| Search Results | ![](screenshots/template-search-results.jpg) |
| Login          | ![](screenshots/template-login.jpg)          |
| User Settings  | ![](screenshots/template-user-settings.jpg)  |
| Logout         | ![](screenshots/template-logout.jpg)         |

## Authors

- [M Haidar Hanif](https://mhaidarhanif.com) ([@mhaidarh](https://github.com/mhaidarh))
- [Azobu Team](https://azobu.com) ([@azobu](https://github.com/azobu))

## License

See [LICENSE](./LICENSE)
