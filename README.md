# An example of tsc-alias package issue

Extending a **tsconfig installed via Yarn 2 (plug n play)** results in a File not found error.

```json
"extends": "@tsconfig/recommended/tsconfig.json",
  "compilerOptions": {
    "target": "es2018",
    "module": "commonjs",
    "outDir": "dist",
    "sourceMap": true,
    "types": ["node"]
  },
  "include": ["src/**/*.ts", "__tests__/**/*"],
  "exclude": ["node_modules"]

```

```sh
> yarn build
> tsc-alias error: File undefined not found
```