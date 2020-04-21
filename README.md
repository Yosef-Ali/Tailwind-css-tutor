# Tailwind-css-tutor best practice

1. npm init -y
2. npm install tailwindcss postcss-cli autoprefixer
3. create css/tailwind.css file and pest this codes

```
@tailwind base;

@tailwind components;

@tailwind utilities;
```

4. Run npx tailwindcss init

5. create postcss.config.js file in the root folder pest

```
module.exports = {
  plugins: [
    // ...
    require('tailwindcss'),
    require('autoprefixer'),
    // ...
  ]
}
```

6. change the scripe in the packege.json

```
"scripts": {
		"build": "postcss css/tailwind.css -o public/build/tailwind.css "
	},
```

7. run npm build

### important responsive utility tags

mx-auto, max-w-md, sm:max-w-xl

##
{
  "name": "my-tailwind-project",
  "version": "1.0.0",
  "description": "",
  "main": "index.js",
  "scripts": {
    "build": "postcss css/tailwind.css -o public/build/tailwind.css",
    "watch": "postcss css/tailwind.css -o public/build/tailwind.css --watch"
  },
  "repository": {
    "type": "git",
    "url": "git+https://github.com/adamwathan/my-tailwind-project.git"
  },
  "keywords": [],
  "author": "",
  "license": "ISC",
  "bugs": {
    "url": "https://github.com/adamwathan/my-tailwind-project/issues"
  },
  "homepage": "https://github.com/adamwathan/my-tailwind-project#readme",
  "dependencies": {
    "autoprefixer": "^9.6.1",
    "postcss-cli": "^6.1.2",
    "tailwindcss": "^1.0.4"
  }
}

## extracting-reusable-components
1. change package.json
```
{
  "name": "my-tailwind-project",
  "version": "0.1.0",
  "private": true,
  "scripts": {
    "serve": "vue-cli-service serve",
    "build": "vue-cli-service build",
    "lint": "vue-cli-service lint"
  },
  "dependencies": {
    "autoprefixer": "^9.6.1",
    "core-js": "^2.6.5",
    "tailwindcss": "^1.0.4",
    "vue": "^2.6.10"
  },
  "devDependencies": {
    "@vue/cli-plugin-babel": "^3.9.0",
    "@vue/cli-plugin-eslint": "^3.9.0",
    "@vue/cli-service": "^3.9.0",
    "babel-eslint": "^10.0.1",
    "eslint": "^5.16.0",
    "eslint-plugin-vue": "^5.0.0",
    "vue-template-compiler": "^2.6.10"
  },
  "eslintConfig": {
    "root": true,
    "env": {
      "node": true
    },
    "extends": [
      "plugin:vue/essential",
      "eslint:recommended"
    ],
    "rules": {},
    "parserOptions": {
      "parser": "babel-eslint"
    }
  },
  "browserslist": [
    "> 1%",
    "last 2 versions"
  ]
}
```
