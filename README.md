## Jest

-   installation de Jest et du plugin **babel-plugin-transform-es2015-modules-commonjs** pour pouvoir utiliser les modules ES6 avec node, ce qui crée un fichier de configuration **.babelrc**
-   inscription dans le fichier package.json de jest dans test : `"scripts": {"test": "jest"}`

```
npm install --save-dev jest
npm install --save-dev babel-plugin-transform-es2015-modules-commonjs
```

```js
{
    "env": {
      "test": {
        "plugins": ["transform-es2015-modules-commonjs"]
      }
    }
  }
```

## ESLint

-   installalation de la dépendance et création d'un fichier de configuration pour définir les règles

```
npm install eslint --save-dev
./node_modules/.bin/eslint --init
```

fichier de configuration **.eslintrc.yml** :

```yml
env:
    es6: true
    node: true
extends: 'eslint:recommended'
globals:
    Atomics: readonly
    SharedArrayBuffer: readonly
parserOptions:
    ecmaVersion: 2018
    sourceType: module
rules:
    indent:
        - error
        - 4
    linebreak-style:
        - error
        - unix
    quotes:
        - error
        - single
    semi:
        - error
        - never
```

## Prettier

-   pour le formataga du code
-   ajout de l'extension VS Code
-   activer le formatage automatique lors de la sauvegarde

fichier de configuration **.prettierrc.yaml** :

```yml
trailingComma: 'es5'
tabWidth: 4
semi: false
singleQuote: true
printWidth: 120
```
