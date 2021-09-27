## Install Tailwind CSS v2.2 as a PostCSS plugin with JIT mode

This is a boilerplate for Tailwind CSS installed as a postCSS plugin and configured for two modes - Watching file changes for **development** and optimizing for **production**:

### How to use

**Step 1:**<br>
`npm install`<br>

**Step 2:**<br>
`npm run build`<br>

Watches files as you make changes to your `index.html` within `public` folder

**Step 3:**<br>
`npm run prod`<br>

Uses `cssnano` to minify the stylesheet for production

**Note to Windows users:**

Change the `build` script to<br>
`"build": "set TAILWIND_MODE=watch&postcss tailwind.css -o ./public/styles.css -w --verbose"`

On windows, if you face an error `"NODE_ENV is not recognised..."`, you must install `win-node-env`, so just run:<br>
`npm i win-node-env`

## Setup this boilerplate from scratch with `yarn`

`yarn init`<br>
`yarn add -D tailwindcss@latest postcss-cli@latest autoprefixer@latest`<br>
Create a new folder name **public** and inside it create file **index.html** and **styles.css**<br>
Create **tailwind.css** at root directory.<br>
`npx tailwindcss init -p`<br>
Change 'purge' of **tailwind.config.js** as tailwind documents.<br>
Add `mode: 'jit'` above of purge<br>
Change the **build** script to<br>
`"build": "set TAILWIND_MODE=watch&postcss tailwind.css -o ./public/styles.css -w --verbose"`<br>
Change the **prod** to<br>
`"propd": "NODE_ENV=production postcss tailwind.css -o ./public/styles.css"`<br>
Copy script from **postcss.config.js** and replace with it.<br>
