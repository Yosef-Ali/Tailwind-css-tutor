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

## composing-utilities-with-apply
```
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
```

