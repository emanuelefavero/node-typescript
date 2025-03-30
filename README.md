# Node.js TypeScript Quick Start Boilerplate

This is a boilerplate and quick start guide for building Node.js applications using TypeScript. It includes a basic project structure, configuration files, and linting rules to help you get started quickly.

## Features

- Node.js TypeScript support
- ESLint for linting

## Installation

- Clone the repository
- Run `npm install` to install dependencies
- Run `npm run dev` to start the development server
- Edit the `index.ts` file to start building your application

> Tip: You can also use `npm run build` to build the project for production and `npm start` to run the built project
>
> BEWARE: If you use `prettier`, make sure the `eslint` rules do not conflict with it

## Quick Setup for a new Node.js TypeScript project

- Create an `npm` project

  ```bash
  npm init -y
  ```

- Add a `.gitignore` file (use `.gitignore` from this repo)
- Create an `index.ts` file in the root directory
- Install TypeScript, ts-node and nodemon

  ```bash
  npm install --save-dev typescript ts-node @types/node nodemon
  ```

- Add a `tsconfig.json` file

  ```json
  {
    "compilerOptions": {
      "target": "es2016",
      "module": "commonjs",
      "esModuleInterop": true,
      "forceConsistentCasingInFileNames": true,
      "strict": true,
      "skipLibCheck": true
      // "outDir": "./dist",
      // "rootDir": "./src"
    }
  }
  ```

  > Note: you can also generate one using the `npx tsc --init` command

- Add these scripts to your `package.json` file

  ```json
  "scripts": {
    "dev": "nodemon --watch src --exec ts-node index.ts",
    "build": "npx tsc",
    "start": "node index.js",
    "lint": "eslint --ext .ts ."
  },
  ```

### Optional ESLint Setup

- Install ESLint for TypeScript

  ```bash
  npm install --save-dev eslint @typescript-eslint/parser @typescript-eslint/eslint-plugin
  ```

- Setup ESLint

  ```bash
  npx eslint --init
  ```

  > Note: During the ESlint setup process, remember to also turn on `node` besides `browser` using the `space` bar when selecting the environment
