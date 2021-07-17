# Eslint configuration "Standard" (+Semiestandar) for NodeJS

## Description

Some rules with Standard + Semiestandar:

```
const obj = { id: 5, }; // ERROR, "comma-dangle"
const obj = {id: 5}; // ERROR, "object-curly-spacing"
const obj = { id: 5 } // ERROR, "Missing semicolon"
const obj = { id: 5 }; // CORRECT
```

## Installation

To install Eslint and its plugins/config:

### `yarn add eslint @babel/eslint-parser eslint-config-standard eslint-config-semistandard eslint-plugin-import eslint-plugin-node eslint-plugin-promise eslint-plugin-import-length eslint-plugin-simple-import-sort --dev`

## Configuration

Create an `.eslintrc` file at the root of your project with:

```
{
  "env": {
	"jest": true,
    "mongo": true,
	"node": true,
  },
  "extends": [
    "eslint:recommended",
    "semistandard"
  ],
  "ignorePatterns": [
    "build/*"
  ],
  "plugins": [
    "import",
    "import-length",
    "simple-import-sort"
  ],
  "parserOptions": {
    "ecmaVersion": 2021
  },
  "rules": {
    "import-length/import-length": "error",
    "import/newline-after-import": "error",
    "import/no-anonymous-default-export": "error",
    "import/no-useless-path-segments": "error",
    "import/order": "error",
    "simple-import-sort/imports": "error"
  }
}
```
