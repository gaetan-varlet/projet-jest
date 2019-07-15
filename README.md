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
-   fichier de configuration **.eslintrc.json**

```
npm install eslint --save-dev
./node_modules/.bin/eslint --init
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

## ESLint avec les règles de Prettier et les règles Airbnb

```
npm install -D eslint prettier
npx install-peerdeps --dev eslint-config-airbnb
npm install -D eslint-config-prettier eslint-plugin-prettier
```

dans le fichier **.eslintrc.json** :

```json
{
    "extends": ["airbnb", "prettier"],
    "plugins": ["prettier"],
    "rules": {
        "prettier/prettier": ["error"]
    }
}
```
