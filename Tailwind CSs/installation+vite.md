To install Tailwind CSS with vite:

1.Install Vite (if you haven’t already):
```bash
npm create vite@latest
cd your-project-name
npm install
```
2.Install Tailwind CSS and dependencies:
```bash
npm install -D tailwindcss postcss autoprefixer
npx tailwindcss init -p
```
3.Configure tailwind.config.js: Update the content array to include your source files:
```js
// tailwind.config.js
module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{js,ts,jsx,tsx,vue}"
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```
4.Add Tailwind to your CSS: In your main CSS file (e.g., src/index.css), add:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

5.Import the CSS in your main entry file:
```css
// main.js or main.ts
import './index.css';
```
Run your Vite dev server:
```bash
npm run dev
```