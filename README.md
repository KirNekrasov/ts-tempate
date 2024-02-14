# ts-tempate

- Install [NVM](https://github.com/nvm-sh/nvm?tab=readme-ov-file#installing-and-updating).

- Install Node 18 and use:

```
nvm install 18
```

```
nvm use 18
```

- Install [yarn](https://yarnpkg.com/getting-started/install):

```
corepack enable
```

- Init yarn project:

```
yarn init -2
```

- Install:
  - [typescript](https://www.typescriptlang.org/docs/handbook/typescript-from-scratch.html),
  - [eslint](https://eslint.org/docs/latest/use/getting-started),
  - [prettier](https://prettier.io/docs/en/install),
  - [jest](https://jestjs.io/docs/getting-started),
  - All types

```
yarn add -D @types/eslint @types/jest @types/node @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint eslint-config-prettier jest prettier ts-jest typescript
```

- Copy and modify if required config files:

  - Typescript: `tsconfig.json`, `tsconfig.cjs.json`, `tsconfig.esm.json`
  - ESLint: `.eslintrc.js`
  - Prettier: `.prettierignore`, `.prettierrc`
  - Jest: `jest.config.js`

- Install `ts-node` if you need to run `.ts` modules:

```
yarn add -D ts-node
```

- Configure vscode workspace (yes, you should run it AFTER you install all packages):

```
yarn dlx @yarnpkg/sdks vscode
```

- Copy `.vscode/extensions.json` to your project and install all recommendations.

- For safety reason VSCode requires you to explicitly activate the custom TS settings:

  - Press `ctrl+shift+p` in a TypeScript file
  - Choose `Select TypeScript Version`
  - Pick `Use Workspace Version`

- If you do not have `Select TypeScript Version` option, create `src/index.ts` file, open it and try again, or try to reload VSCode.

- Copy `editor` settings from `.vscode/settings.json` to your project.

- Copy scripts from `package.json` to your project.

- Run `prepare` script to check that everything is working fine.

```
yarn prepare
```

- Copy to `package.json` entry points and set up version:

```json
"version": "1.0.0",
"main": "./dist/cjs/index.js",
"module": "./dist/esm/index.js",
"types": "./dist/esm/index.d.ts",
```

- Try to build your project:

```
yarn build
```

- You're welcome.
