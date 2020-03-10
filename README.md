# charliechocolat-project

Repository for backend/frontend and services for CharlieChocolat Website (onGoing)

## Built With

### Backend

- Nodejs + ExpressJS + Webpack + MongoDB(Atlas);

- dependencies:

  - `accesscontrol`: defines roles and access permissions;
  - `axios`: connection to Google API;
  - `bcryptjs`: password encription;
  - `body-parser`: parses incoming request bodies in a middleware before the handlers (JSON);
  - `dotenv`: used to define environment variables;
  - `express`: define routes and route logic;
  - `express-validator`: validates body params in requests;
  - `helmet`: sets various HTTP headers for security;
  - `jsonwebtoken`: creates and validates tokens;
  - `mongoose`: connects to MongoDB database;
  - `mongoose-unique-validator`: adds pre-save validation for unique fields within a Mongoose schema;
  - `morgan`: HTTP request logger middleware;
  - `multer`: Group of middlewares to handle file data;
  - `uuid`: Generate ids;

- devDependencies:

  - `babel`: compiles javascript code to adapt to browsers;
  - `eslint`: lints all javascript code;
  - `file-loader`: resolves `import` and `required()` into a url;
  - `jest`: javascript testing;
  - `nodemon`: automatically restarts node application when file changes in the directory are detected;
  - `webpack`: bundles production files;
  - `webpack-node-externals`: avoid error when working with Express;

  - File Structure:
    ```bash
    ├── controllers               # Reducers for routes
    │   ├── shared                # Functions shared in reducers
    │       ├──  ...
    │   ├── ...
    ├── middleware                # middleware called in each request which is used
    │   ├── ...
    ├── models                    # Database Schema files
    │   ├── helpers               # Helper classes (ex- HttpError extends Error)
    │       ├──  ...
    │   ├── ...
    ├── routes                    # Express Route definition
    │   ├── ...
    ├── tests                     # Automated tests (alternatively `spec` or `tests`)
    │   ├── ...
    ├── uploads                   # Files served to the frontend
    │   ├── images
    │       ├── ...
    ├── utils                     # Helper functions
    │   ├── ...
    ├── .babelrc                  # Config file for babel
    ├── .env                      # Global environment variables
    ├── apidoc.json               # Config for apidoc documentation package
    ├── app.js                    # API main file
    ├── package.json              # Config file for npm
    ├── webpack.config.js         # Config file for webpack (dev)
    └── webpack.config.prod.js    # Config file for webpack (prod)
    ```

### Frontend

- React;

- dependencies:

  - `@fortawesome`: icon library;
  - `axios`: connects react app to API;
  - `react-bootstrap`: import certain html components;
  - `core-js`: compiles javascript to adapt to brwosers;
  - `dotenv`: enables environment variables;
  - `prop-types`: forces props type checking;
  - `react`: javascript framework used for building the website interface;
  - `react-dom`: virtual DOM for React;
  - `react-redux`: Redux store (app global state management), dispatch actions to the store to update data;
  - `react-router-dom`: react app routing;
  - `react-transition-group`: react library for css animations;
  - `redux-saga`: makes application side effects easier to manage, more efficient to execute, easy to test, and better at handling failures;

- devDependencies:

  - `babel`: compiles javascript code to adapt to browsers;
  - `eslint`: lints all javascript code;
  - `css-loader`: compiles css code in project;
  - `style-loader`: injects CSS into the DOM;
  - `html-webpack-plugin`: simplifies creation of HTML files to serve webpack bundles;
  - `url-loader`: transforms files into base64 URIs;
  - `file-loader`: resolves `import` and `required()` into a url;
  - `jest`: javascript testing;
  - `enzyme`: test react components;
  - `webpack-dev-server`: automatically restarts node application when file changes in the directory are detected;
  - `webpack`: bundles production files;
  - `webpack-node-externals`: avoid error when working with Express;

  - File Structure:
    ```bash
    .
    ├── src                       # Source files
    │   ├── __tests__             # Automated test files
    │       ├──  ...
    │   ├── animations            # CSS styles used for animations
    │       ├──  ...
    │   ├── assets                # Image and Video files
    │       ├──  ...
    │   ├── components            # Components that only use props
    │       ├──  ...
    │   ├── containers            # Components that manipulate state
    │       ├──  ...
    │   ├── hoc                   # Higher Order Components
    │       ├──  ...
    │   ├── hooks                 # Customized hooks to be shared throughout the app
    │       ├──  ...
    │   ├── public                # Root HTML
    │       ├──  ...
    │   ├── shared                # Global functions
    │       ├──  ...
    │   ├── store                 # Redux actions, reducers and sagas
    │       ├──  ...
    │   ├── App.js                # Root Component
    │   ├── axios.js              # Global axios config
    │   ├── index.css             # Global css styling
    │   ├── index.js              # React, Redux (Saga Reducers), Routing, Bootstrap, etc initialization
    │   ├── setupTests.js         # Config to use enzyme with jest tests
    ├── .babelrc                  # Config file for babel
    ├── .eslintrc.json            # Config file for eslint
    ├── jest.config.js            # Config file for jest tests
    ├── package.json              # Config file for npm
    ├── webpack.config.js         # Config file for webpack (dev)
    └── webpack.config.prod.js    # Config file for webpack (prod)
    ```

### Security

- User password is hashed in database;
- Autorizathion headers required;
- Endpoints protected by Role-based-access and authorization;
- User authentication based on tokens (userId + role) and roles:

  - `basic`: shops and orders chocolates;
  - `supervisor`: manages orders;
  - `admin`: manages users and website content;

### Installing

Open terminal in both `/frontend` and `/backend`

`$ npm install` to install all dependencies

Change `.env` file (API keys, mongodb URL, USER and PASSWORD)

`$ npm start` to start backend API and react app

API - http://localhost:5000 (default)

React-App - http://localhost:9000 (default)

(included postman project file in `/backend` for endpoint testing)

## Deployment

Open terminal in both `/frontend` and `/backend`

`$ npm run buildProd` to build `/dist` folders in each parent folder

## Versioning

Apidoc used for versioning. (can be accessed in the backend API after installed and started at http://localhost:5000/api (default)).

## Authors

- **Pedro Dias** - [pedroHdias](https://github.com/pedroHdias)

## License

This project is licensed under the MIT License.

## Future Work

- Multi Language Support;
- Sorting;
- E2E testing: https://nightwatchjs.org/;
- Credit card payments;
- Typescript;
- Redis;
- NextJS;
- Clustering;
- Logging Files;
