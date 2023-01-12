# Set-Up for a React Project

### Resources
- [Tailwind CSS Cheat Sheet](https://nerdcave.com/tailwind-cheat-sheet)
***
## Building a React App

### Create your project
1. cd to location you want to set up your project in and run the command:  
  __Note__ : *project name cannot contain capital letters*<br><br>
      ```
      npx create-react-app project-name
      ```
2. Step into your project: <br><br>
      ```
      cd project-name
      ```

### Install [Tailwind CSS](https://tailwindcss.com/)
3. Install `tailwindcss` via npm, and create your `tailwind.config.js` file.<br><br>
      ```
      npm install -D tailwindcss
      npx tailwindcss init
      ```
4. Add the paths to all of your template files in your `tailwind.config.js` file.<br><br>
      **tailwind.config.js**
      ```
      /** @type {import('tailwindcss').Config} */
      module.exports = {
        content: [
          "./src/**/*.{js,jsx,ts,tsx}",
        ],
        theme: {
          extend: {},
        },
        plugins: [],
      }
      ```
5. Add the `@tailwind` directives for each of Tailwind’s layers to your `./src/index.css` file.<br><br>
      **index.css**
      ```
      @tailwind base;
      @tailwind components;
      @tailwind utilities;
      ```

### Install [DaisyUI](https://daisyui.com/)
6. Install `daisyui` via npm:<br><br>
      ```
      npm install daisyui
      ```
7. Add daisyUI to your `tailwind.config.js` files:<br><br>
      **tailwind.config.js**
      ```
      module.exports = {
        //...
        plugins: [require("daisyui")],
      }
      ```

### Start your build process
8. Run either of these commands to start your project:<br><br>
      ```
      npm start             // refreshes tab upon saving
      npx nodemon           // creates new tab upon saving
      ```