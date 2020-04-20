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
