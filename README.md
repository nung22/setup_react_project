# Set-Up for a React Project

### Resources
- [Tailwind CSS Cheat Sheet](https://nerdcave.com/tailwind-cheat-sheet)
***
## Building a React App

### Create your project
- [ ] cd to location you want to set up your project in and run the command:  
  __Note__ : *project name cannot contain capital letters*<br><br>
      ```
      npx create-react-app project-name
      ```
- [ ] Step into your project: <br><br>
      ```
      cd project-name
      ```

### Install [Tailwind CSS](https://tailwindcss.com/)
- [ ] Install `tailwindcss` via npm, and create your `tailwind.config.js` file.<br><br>
      ```
      npm install -D tailwindcss
      npx tailwindcss init
      ```
- [ ] Add the paths to all of your template files in your `tailwind.config.js` file.<br><br>
      **tailwind.config.js**
      ```
      /** @type {import('tailwindcss').Config} */
      module.exports = {
        mode: 'jit',
        content: ['./src/**/*.{js,jsx,ts,tsx}'],
        purge: ['./src/**/*.{js,jsx,ts,tsx}','./public/index.html'],
        theme: {
          extend: {},
        },
        plugins: [],
      }
      ```
- [ ] Add the `@tailwind` directives for each of Tailwind’s layers to your `./src/index.css` file.<br><br>
      **index.css**
      ```
      @tailwind base;
      @tailwind components;
      @tailwind utilities;
      ```

### Install [DaisyUI](https://daisyui.com/)
- [ ] Install `daisyui` via npm:<br><br>
      ```
      npm install daisyui
      ```
- [ ] Add daisyUI to your `tailwind.config.js` files:<br><br>
      **tailwind.config.js**
      ```
      module.exports = {
        //...
        plugins: [require("daisyui")],
      }
      ```

### Start your build process
- [ ] Run either of these commands to start your project:<br><br>
      ```
      npm start             // refreshes tab upon saving
      npx nodemon           // creates new tab upon saving
      ```
