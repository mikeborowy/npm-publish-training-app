## Init NPM

```
npm init -y
git init
```

## Further setup

```
npm i typescript express @types/express eslint
```

## Init TS

```
npx tsc --init
```

## Configure project

> tsconfig.ts

```
{ declaration: true, outDir: './dist' }
```

> package.json

Make sure name is not available at https://www.npmjs.com/

```
{
  "name": "npm-publish-training-app",
  "publishConfig": {
    "access": "public"
  },
  "files": [
    "./dist"
  ],
  "bin": "./dist/index.js",
  "scripts": {
    "build": "tsc",
    "prepublishOnly": "npm run build"
  },
}
```

`#!/user/bin/env node` - added to `index.ts` allows to execute directly instead of `project/dist/node index.js`

Split `dependencies` and `devDependencies`

## Publish to NPM

```
  npm login
  npm publish
```
