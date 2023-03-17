# vite-ts-react-setup
My setup for react with vite + typescript

## Vite

- `npm create vite .` - for current folder
- `npm create vite {/path/to/my-project}` - for a "named" project
- Walk through the steps.
- `npm install`

## VSCode

- In the project folder create a folder named `.vscode`.
- Absolutely neccessary extensions: **ESLint**, **Prettier**!
- Create a file named `my-project.code-workspace`:

```JSON
{
  "folders": [
    {
      "path": "{/path/to/my-project}",
      "name": "{my-project}"
    }
  ],
  "settings": {
    "[typescript]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode",
      "editor.formatOnSave": true,
    },
    "[typescriptreact]": {
      "editor.defaultFormatter": "esbenp.prettier-vscode",
      "editor.formatOnSave": true,
    }
  }
}
```

## Prettier

- `npm i -D prettier` in the project folder.
- Create a file named `.pretterrc`:

```JSON
{
  "semi": true,
  "tabWidth": 2,
  "printWidth": 80,
  "singleQuote": true,
  "arrowParens": "always"
}
```

- Create a file named `.prettierignore`:

```
node_modules
dist
dist-ssr
*.local
```

## ESLint

- `npm i -D eslint @typescript-eslint/eslint-plugin @typescript-eslint/parser eslint-config-prettier eslint-plugin-prettier eslint-plugin-react eslint-plugin-react-hooks`
- Create a file named `.eslintrc`.

```JSON
{
  "env": {
    "browser": true,
    "es2021": true
  },
  "extends": [
    "eslint:recommended",
    "plugin:react/recommended",
    "plugin:@typescript-eslint/recommended",
    "plugin:react-hooks/recommended",
    "plugin:prettier/recommended"
  ],
  "overrides": [],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": [
    "react",
    "@typescript-eslint"
  ],
  "rules": {
    "indent": ["error", 2],
    "linebreak-style": ["error", "unix"],
    "quotes": ["error", "single"],
    "semi": ["error", "always"],
    "react/react-in-jsx-scope": "off"
  }
}
```

- Create a file named `.eslintignore`:

```
node_modules
dist
dist-ssr
*.local
```

**You should have a basic setup for working on a new project!**
