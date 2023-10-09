# Eslint & Prettier Setup For Node.js

Eslint is a popular linter for javascript & Prettier is a popular code formatter

## Setup Eslint with airbnb-base 

Open your terminal & initialize `package.json` using npm or yarn:

```bash
npm init -y

# or

yarn init -y
```

Now install eslint by using 

```bash
npm install eslint --save-dev

# or

yarn add -D eslint
```
Now install additional packages

```bash
npm install eslint-config-airbnb eslint-config-prettier eslint-plugin-prettier eslint-plugin-import prettier --save-dev

#or

yarn add -D eslint-config-airbnb eslint-config-prettier eslint-plugin-prettier eslint-plugin-import prettier 
```



Here is an example of `package.json` after installing these packages

```json
{
    "name": "chat-application",
    "version": "1.0.0",
    "description": "",
    "main": "index.js",
    "scripts": {
        "start": "nodemon app.js",
        "test": "echo \"Error: no test specified\" && exit 1"
    },
    "keywords": [],
    "author": "",
    "license": "ISC",
    
    "devDependencies": {
        "eslint": "^7.32.0 || ^8.2.0",
        "eslint-config-airbnb-base": "^15.0.0",
        "eslint-config-prettier": "^8.5.0",
        "eslint-plugin-import": "^2.25.2",
        "eslint-plugin-prettier": "^4.0.0",
        "prettier": "^2.6.2"
    }
}


```

Again open your terminal and install dependencies with npm or yarn


Now create a file named `.eslintrc.json` in your root folder.

copy the code from below and save `.eslintrc.json`

```json

{
    "extends": [
        "airbnb-base",
        "prettier"
    ],
    "parserOptions": {
        "ecmaVersion": 12
    },
    "env": {
        "commonjs": true,
        "node": true
    },
    "rules": {
        "no-console": 0,
        "indent": 0,
        "linebreak-style": 0,
        "no-underscore-dangle": 0,
        "prettier/prettier": [
            "error",
            {
                "trailingComma": "all",
                "singleQuote": true,
                "printWidth": 100,
                "tabWidth": 4,
                "semi": true
            }
        ]
    },
    "plugins": [
        "prettier"
    ]
}

```

You are ready to go with Eslint.

