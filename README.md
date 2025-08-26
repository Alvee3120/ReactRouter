React Router is a standard library used in React applications to handle routing—that means switching between different views or pages without reloading the entire page. It makes your React app behave like a multi-page app, while actually running as a Single Page Application (SPA). 

## Step by step way to create a simple project using React Router

### Step-1: Create React-Vite Project 
For Creating React Project using Vite , first we need to 

```js
npm create vite@latest <YourProjectName>
```

after that go to your directory then

```bash
npm install
```

Then if you want to configure tailwind run this command

```bash
npm install tailwindcss @tailwindcss/vite
```

After that configure your vite.config.js file like this

```js
import { defineConfig } from 'vite'
import tailwindcss from '@tailwindcss/vite'
export default defineConfig({
  plugins: [
    tailwindcss(),
  ],
})
```
Add an @import to your CSS file that imports Tailwind CSS.

```css
@import "tailwindcss";
```

Start your build process
```bash
npm run dev
```

### Step-2: Create Components and install required Packages

Install the react router dom 

```bash
npm install react-router-dom
```


Create a components folder under src folder to create UI

### Step-3: Create a layout for our project (Optional)

Here we always wants the header and footer in the all pages , that's why we first define Header and at last we define Footer and we Dynamically push the component in between them using Outlet

![layout](image.png)

### Step-4: Create Router in main.jsx

We will create a router using CreateBrowserRouter that will contains a object. The object basically contains two things , path and element

![Create Router](image-1.png) 

As We used Layout and we push the components dynamically we will add another things to that object which is "Children"
that children contains another Array of Object which actually refers to each page 
![Whole router](image-2.png)

### Step-4: Create a RouterProvider and then pass the Router 

![RouterProvider](image-3.png)


Till now we've completed the routing things , now we need to define this in Header's Navlink
![alt text](image-5.png)
That's how we can easily handle the routing in our project



### Param
In React Router, a param (short for parameter) is a dynamic part of the URL that you can capture and use inside your components. 

```
/user/:id
```