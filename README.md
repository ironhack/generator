![Ironhack logo](https://i.imgur.com/1QgrNNw.png)

# [Ironhack](https://www.ironhack.com) [Express](https://www.npmjs.com/package/express) application generator.

![NodeJS Logo](https://user-images.githubusercontent.com/970858/33016149-421633aa-cde5-11e7-9c09-5d5d670964ff.png)
![MongoDB Logo](https://user-images.githubusercontent.com/970858/33016120-2435a6d6-cde5-11e7-874d-ef8b18e97472.png)
[![Express Logo](https://i.cloudup.com/zfY6lL7eFa-3000x3000.png)](http://expressjs.com/)
![Mongoose Logo](https://user-images.githubusercontent.com/970858/33016063-f66b535e-cde4-11e7-8088-5df48a048d46.png)

![HandleBars Logo](https://user-images.githubusercontent.com/970858/33016171-58b9cc0c-cde5-11e7-9252-d3a8c5d349ab.png)

## Introduction

`iron-generator` is Ironhack's NPM package that allows students to quickly create express projects. The `Iron-generator` is strongly opinionated:

- Follows industry best practices
- Predefined directory structure:
    - `public`: Public Assets folder (css, js, images)
    - `models`: Mongoose Schemas and models
    - `routes`: Project routes
    - `views`: Project views and layouts
- **Views Template**: [Handlebars](http://handlebarsjs.com/)
- **CSS Engine**: [SCSS](http://sass-lang.com/) - [Node-sass-middleware]()
- **ORM**: Mongoose
- Comes prepopulated with popular, useful Express middlewares
  - **Logger**: morgan
  - **Favicon**: serve-favicon
  - **HTTP POST Params**: body-parser
  - **Cookies**: cookie-parser
- **Error handling**: 404 (Not found), 500 (Internal Server Error)
- Creates project `.gitignore` - *removes `node_modules`, etc*
- **Environment variables** loaded from `.env` configuration file
- **Server monitoring**: nodemon

## Installation

Install `iron-generator` as a global NPM package, so you can run it from anywhere in your computer:

```sh
$ npm install -g iron-generator
```

## Quick Start

The quickest way to get started with express is to utilize the executable `irongenerate(1)` to generate an application as shown below:

Create the app:

```bash
$ irongenerate awesome-project/
$ cd awesome-project/
```

This will generate the following directory structure:

```
awesome-project/
├── app.js
├── package.json
├── models
├── routes
│   └── index.js
├── views
│    ├── error.hbs
│    ├── index.hbs
│    └── layout.hbs
├── public
│   ├── images
│   ├── javascripts
│   │   └── script.js
│   └── stylesheets
│       └── styles.sass
```

Install all dependencies described in `package.json`:

```bash
$ npm install
```

Start your Express.js app at `http://localhost:3000/`:

```bash
$ npm start
```

## Command Line Options

This generator can also be further configured with the following command line flags.

    -h, --help           output usage information
        --version        output the version number
    -c, --css <engine>   add stylesheet <engine> support (plain|less|sass|scss) (defaults to scss)
    -f, --force          force on non-empty directory

## License

[MIT](LICENSE)
