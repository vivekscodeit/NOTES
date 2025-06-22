# Installation using vite
Follow the steps given in the documentation but before create a vite folder
using `npm create vite@latest`

# Installation using PostCSS tailwind version3

```bash
#This will install the binary of tailwind too which is missing in the latest download of tailwind v4
npm install -D tailwindcss@3 postcss autoprefixer vite
npx tailwindcss init -p
```
Then after in the tailwindcss.config.js modify the changes:
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["*"],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
Then after in package.json in the script write 
 ```json 
  "scripts": {
    "shery" : "vite"
  },
  ```
  You can write anything in place of shery
  
  Then after you have to run `npm run shery ` to open the vite server
  

