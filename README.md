# stack

## Overview

![Image of stack](.github/images/stack.png)

## Devops

### Git and GitHub

### Yarn – JavaScript package management

Yarn is a JavaScript dependency manager, which allows for easily adding and removing dependencies (such as React and Express). Yarn also has a feature called `yarn workspaces`, which makes it easy to manage dependencies in a monorepo (a monorepo is a repository containing multiple applications/packages, e.g. packages/frontend and packages/backend). Running the install command anywhere within the project installs all the dependencies for all the packages in the project.

#### Usage

To install all packages listen in the various `package.json`s, run

```sh
yarn # short for yarn install
```

Add a dependency

```sh
yarn add <package names>...
# Example:
yarn add react express
```

Add a development dependency

```sh
yarn add --dev <package names>...
# or
yarn add -D <package names>...
# Example
yarn add -D @types/react
```

Remove a dependency

```sh
yarn remove <package names>...
# Example
yarn remove react express @types/react
```

Adding a dependency to the root of a monorepo project requires the use of the `-W` flag. E.g.

```sh
yarn add -W -D typescript
```

#### Documentation

The documentation for Yarn can found [here](https://classic.yarnpkg.com/en/docs/).

### Jest – JavaScript testing framework

Jest is a testing framework for JavaScript with easy syntax and good support for different libraries, such as React.

#### Usage

To run all tests in a package run

```sh
yarn test
```

in the package directory (e.g. packages/frontend).

To run all tests for all packages in a project run the same command in the root of the project.

#### Documentation

The documentation for Jest can be found [here](https://jestjs.io/docs/en/getting-started).

#### Tutorials

- [Jest Tutorial for Beginners](https://www.valentinog.com/blog/jest/)
- [Testing React Apps](https://jestjs.io/docs/en/tutorial-react)

### ESLint – JavaScript linting

ESLint is a very configurable linting tool for JavaScript. Helps maintain high code quality in an easy way.

#### Usage

To lint all files in a package run

```sh
yarn lint
# or
yarn lint:fix
# to fix issues if found
```

in the package directory (e.g. packages/frontend).

To lint all the files for all packages in a project run the same command in the root of the project.

The configuration for ESLint can be found in `.eslintrc.js` file found in the root and in each package directory.

#### IDE integration

Some IDE's can automatically report on found issues in current files, and fix problems that can be fixed when saving files.

##### Visual Studio Code

1. Install the `dbaeumer.vscode-eslint` extension
2. Add the following to your VSCode `settings.json`
   ```json
   "editor.codeActionsOnSave": {
     "source.fixAll.eslint": true
   }
   ```
   Adding the following prevents VSCode from automatically formatting using its own formatter on save (if using Prettier through ESLint)
   ```json
   "[javascript]": {
     "editor.formatOnSave": false,
   },
   "[javascriptreact]": {
     "editor.formatOnSave": false,
   },
   "[typescript]": {
     "editor.formatOnSave": false,
   },
   "[typescriptreact]": {
     "editor.formatOnSave": false,
   }
   ```

#### Documentation

You can read the documentation for ESLint [here](https://eslint.org/docs/user-guide/getting-started).

### Prettier – Formatting code (JavaScript etc.)

Prettier is an opinionated code formatter that integrates well with ESLint.

#### Usage

Usage is integrated with ESLint so it is automatically run when using `yarn lint:fix`, which can be configured to be executed when saving a file.

#### Documentation

You can read the documentation for Prettier [here](https://prettier.io/docs/en/install.html).

#### Tutorials

- [ESLint + Prettier](https://medium.com/javascript-scene/streamline-code-reviews-with-eslint-prettier-6fb817a6b51d)

### TravisCI – continuous integration

#### Documentation

You can read the documentation for TravisCI [here](https://docs.travis-ci.com/user/tutorial/).

#### Tutorials

- [TravisCI for JavaScript (NodeJS)](https://docs.travis-ci.com/user/languages/javascript-with-nodejs/)

### Docker – consistent environment

#### Documentation

You can read the documentation for Docker here.

### TypeScript – less painful JavaScript

#### Documentation

You can read the documentation for TypeScript [here](https://www.typescriptlang.org/docs/home.html).

## Frontend

### React – framework for building *react*ive web applications

#### Documentation

You can read the documentation for React [here](https://reactjs.org/docs/getting-started.html).

### Apollo Client – library to make working with GraphQL API’s easy

#### Documentation

You can read the documentation for Apollo Client [here](https://www.apollographql.com/docs/react/v3.0-beta).

### React Router – different url, different content

#### Documentation

You can read the documentation for Router Router here.

## Backend

### Express – HTTP library

#### Documentation

You can read the documentation for Express [here](https://expressjs.com/).

### TypeORM – abstraction layer over the database

#### Documentation

You can read the documentation for TypeORM [here](https://typeorm.io/#/).

### Apollo Server – GraphQL server

#### Documentation

You can read the documentation for Apollo Server [here](https://www.apollographql.com/docs/apollo-server/).

### TypeGraphQL – easily build GraphQL API’s using TypeScript

#### Documentation

You can read the documentation for TypeGraphQL [here](https://typegraphql.com/).

## Database

### PostgreSQL

A free and open source relational database. Currently one of the most popular databases.

Will be used to store data, such as users and tournaments.

## Other resources

VSCode setttings

Template project: https://github.com/rosengrenen/react-node-graphql-postgres-typescript-template

YARN
Package management
