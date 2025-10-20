## INSTRUCTION OF DEPLOY WEBSITE ON SURGE (DONT USE POWERSHALL 💣✂)

- DOWNLOAD SURGE :

### 1st way :

`npm install --global surge `
`cd dist`
`surge`

### 2nd way :
normal : 
`npm install --global surge `
`npm run build`
`surge dist`
react : 
- `npm install --global surge `
-  public : `_redirects` file in `dist` folder
- `npm run build`
- copy `index.html` code and paste to `200.html` in `dist` folder
- `surge dist`

- First install surge, if you haven’t already : `npm install --global surge `
- Run `npm run build`.
- Deploy to surge by typing `surge dist`.
- You can also deploy to a custom domain by adding surge dist yourdomain.com.
- custom domain create process :
  - create a folder in public folder and name it : `CNAME` , put the url : `sihambintahabib-assairment.surge.sh`
- for **_react_** add a `_redirects` file in public folder , write this : `/* /index.html 200`
- Run `npm run build` to add the `_redirects` file in `dist` folder
- copy `index.html` code and paste to `200.html` in `dist` folder

Visit the website for more information :
`https://vite.dev/guide/static-deploy.html#surge:~:text=firebase%20deploy.-,Surge,to%20a%20custom%20domain%20by%20adding%20surge%20dist%20yourdomain.com.,-Azure%20Static%20Web`

## ## INSTRUCTION OF DEPLOY WEBSITE ON netlify / cloudflare

ড্র্যাগ এন্ড ড্রপ করে netlify / cloudflare এ রিলিজ দিলে react রাউটার সরাসরি কাজ করবে না। সেটা করার জন্য তোমার dist ফোল্ডার ড্র্যাগ করে ড্রপ করার আগে একটা ফাইল তৈরি করে নিতে হবে। সেই ফাইল এর নাম হবে: `_redirects` আর তারমধ্যে জাস্ট এক লাইন থাকবে। সেখানে লেখা থাকবে:
`/* /index.html 200`

## React code clone from react

- clone from github : `git clone url`
- run `npm i`

## INSTRUCTION OF VITE FOR REACT

### 1st process :

- Download vite for react: `npm create vite@latest my-react-project -- --template react`
- Type for conformation : `y`
- `cd my-project`
- `npm install`
- ` npm run dev`
- Local: http://localhost:5173/
- Press ctrl+c to stop the live server
- press `y then enter` to conform

### 2nd process :

- type : `npm create vite@latest`
- choose filename : `my-project`
- choose language : `javascript `
- npm install :
- `cd my-project`
- `npm install`
- ` npm run dev`

## INSTRUCTION OF Install Tailwind

- Install Tailwind CSS : `npm install tailwindcss @tailwindcss/vite`
- Configure the Vite plugin into `vite.config.js file` :  
  `import tailwindcss from '@tailwindcss/vite'`
- add this pluging to vite.config.js into pluging : `tailwindcss()`
- file import in index.css : `@import "tailwindcss";`
- Visit the website for more information :
  `https://tailwindcss.com/docs/installation/using-vite`

## INSTRUCTION OF Install daisy

- download : `npm i -D daisyui@latest`
- file import in index.css : `@plugin "daisyui";`

## INSTRUCTION OF Install Toastify

- download : `npm i react-toastify@11.0.0-0`
- import into app.jsx : `import { ToastContainer, toast } from 'react-toastify';`
- import into app.jsx : `import { ToastContainer, toast } from 'react-toastify';`
- Place the `<ToastContainer />` component at the root level of your application (e.g., inside your App.JSX component's return statement) where you want the toasts to appear.
- ADD THE ALERT : `toast ('YOUR COMMENT')` ALSO IMPORT THE toast from the react `import { toast) from "react-toastify";`

- Visit the website for more information :
  `https://www.npmjs.com/package/react-toastify/v/11.0.0-0`

## INSTRUCTION OF Install React-router

- Downoad : `npm i react-router`
- Create ROUTER and RENDER : add these code into `main.jsx`

```
import React from "react";
import ReactDOM from "react-dom/client";

 import { createBrowserRouter } from "react-router";
import { RouterProvider } from "react-router/dom";



const router = createBrowserRouter([
  {
    path: "/",
    element: <div>Hello World</div>,
  },
]);

const root = document.getElementById("root");

ReactDOM.createRoot(root).render(
  <RouterProvider router={router} />,
);
```

- ![alt text](image.png)

## INSTRUCTION OF Install React-icons

downloads : `npm i react-icons`

## INSTRUCTION OF Install axios

downloads : `  npm i axios`

---

problem :

1. daisy ui
   2.how to learn react
2. props
3. use
4. usestate
