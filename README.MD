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

- download :

```
npm i -D daisyui@latest
```

- file import in index.css : ` @plugin "daisyui";`
- turn off dark mode -

```
 @plugin "daisyui"{
themes: light-default;
};
```

website link : https://daisyui.com/docs/themes/?lang=en

## INSTRUCTION OF Install Toastify

- download : `npm i react-toastify@11.0.0-0`
- import into main.jsx : `import { ToastContainer } from 'react-toastify';`

- Place the `<ToastContainer />` component at the root level of your application (e.g., inside your main.JSX component's return statement) where you want the toasts to appear.
- ADD THE ALERT : `toast ('YOUR COMMENT')` ALSO IMPORT THE toast from the react `import { toast) from "react-toastify";`

- Visit the website for more information :
  `https://www.npmjs.com/package/react-toastify/v/11.0.0-0`

## INSTRUCTION OF Install React-router

- Downoad :

```
npm i react-router
```

- Create ROUTER and RENDER : add these code into `main.jsx`

```
import React from "react";
import ReactDOM from "react-dom/client";

<!-- ?
 import { createBrowserRouter } from "react-router";
import { RouterProvider } from "react-router/dom";
? -->


<!-- ?
const router = createBrowserRouter([
  {
    path: "/",
    element: <div>Hello World</div>,
  },
]);
? -->

const root = document.getElementById("root");

ReactDOM.createRoot(root).render(
  <RouterProvider router={router} />,
);
```

- ![alt text](image.png)

## INSTRUCTION OF DEPLOY WEBSITE ON SURGE - DOWNLOAD SURGE (DONT USE POWERSHALL 💣✂)

### 1st way : ❌

```
npm install --global surge
cd dist
surge
```

## 2nd way :

### Normal : ❌

---

- Run in the terminal :

```
npm install --global surge
npm run build
surge dist
```

### React : ❌

---

- Run in the terminal :

```
npm install --global surge
```

- public : Create `_redirects` file in `public` folder and transfer to `dist` folder

```
npm run build
```

- copy `index.html` code and paste to `200.html` in `dist` folder then :

```
surge dist

```

### Custom Domain name : ✅

---

- First install surge, if you haven’t already :

```
 npm install --global surge
```

- Run in the terminal :

```
npm run build
```

- Deploy to surge by typing

```
surge dist
```

- You can also deploy to a custom domain by adding surge dist yourdomain.com.<BR>
  **custom domain create process** :
  - create a folder in public folder and name it : `CNAME` , put the url : `sihambintahabib-assairment.surge.sh`

### React_route + Firebase : ✅✅

---

- `npm install --global surge`
- for **\_react_route + firebase**
- add a `_redirects` file in public folder , write this in the file : `/* /index.html 200`
- optional : create a folder in public folder and name it : `CNAME` , put the url : `sihambintahabib-assairment.surge.sh`
- Run `npm run build` to add the `_redirects` file in `dist` folder
- copy `index.html` code and paste to `200.html` in `dist` folder
- Deploy `surge dist`

## for 1st time deploy :
- `npm install --global surge`
- public : `_redirects` : `/* /index.html 200`
- public : `CNAME` : `sihambintahabib-assairment$.surge.sh`
- `npm run build`
- dist : `index.html` -> `200.html`
- `surge dist`

## for 2nd time deploy :
  1st : `npm run build`
  2nd : copy `index.html` code and paste to `200.html` in `dist` folder
  3rd : `surge dist`
  [ changer vercel client site domain url by surge url : https://vercel.com/sihams-projects-0a3f7554/assairment11/settings/environment-variables]

---

Visit the website for more information :
`https://vite.dev/guide/static-deploy.html#surge:~:text=firebase%20deploy.-,Surge,to%20a%20custom%20domain%20by%20adding%20surge%20dist%20yourdomain.com.,-Azure%20Static%20Web`

---

## INSTRUCTION OF DEPLOY WEBSITE ON netlify / cloudflare

ড্র্যাগ এন্ড ড্রপ করে netlify / cloudflare এ রিলিজ দিলে react রাউটার সরাসরি কাজ করবে না। সেটা করার জন্য তোমার dist ফোল্ডার ড্র্যাগ করে ড্রপ করার আগে একটা ফাইল তৈরি করে নিতে হবে। সেই ফাইল এর নাম হবে: `_redirects` আর তারমধ্যে জাস্ট এক লাইন থাকবে। সেখানে লেখা থাকবে:

```
/* /index.html 200
```

---

## firebase

1. run :

```
 npm install firebase
```

2. create a new folder > file (firebase-config.js) and paste it :

```
// Import the functions you need from the SDKs you need
import { initializeApp } from "firebase/app";
import { getAuth } from "firebase/auth";

// TODO: Add SDKs for Firebase products that you want to use
// https://firebase.google.com/docs/web/setup#available-libraries

// Your web app's Firebase configuration
const firebaseConfig = {

//generate firebase key -> add web then generate key :
<!-- //  https://console.firebase.google.com/u/0/project/assairment-11-ddac8/settings/general/web:MWM0YWVlMWQtMjk1Zi00MjI2LWE2OGUtNjQ5MzJkOWJjZjk4 -->

};

// Initialize Firebase
const app = initializeApp(firebaseConfig);
// Initialize Firebase Authentication and get a reference to the service
export const auth = getAuth(app);



```

---

## React Hook form

1. Install :

```
npm install react-hook-form
```

2. Import useForm and desturture required data :

```
 const {
    register,
    handleSubmit,
    watch,
    formState: { errors },
  } = useForm()
```

3.add `register` in inpurt field , Example :

```
                {...register("name" , {required : 'name is required'})}

```

```
<input {...register("name" , {required : 'Name is required'})}  />
```

4. diffeerent value of register :

- required:'' or required : true ✅
- min
- max
- minLength : number or { value : 6 , message : 'min length is 6 '}
- maxLength : number or { value : 20 , message : 'max length is 20 '}
- pattern :regex Code
- validate

5. add `handleSubmit` in form , Example :

```
 <form onSubmit={handleSubmit}>...</form>
```

6. create a variable `onSubmit`, Example :

```
const onSubmit= async data => console.log(data);

```

7. call onSubmit

```
 <form onSubmit={handleSubmit(onSubmit)}>...</form>
```

8. Show `error` :

```
{
  errors.name && (
<p className='text-red-500 text-xs mt-1'>
{errors.name.message}
</p>
)}
```

9. use data of user :

```
const onSubmit= async data => ;
    const { name, email, image, password } = data;
    try{}
    catch(){}....... other functionality

```

10. `watch` : help to see real time changes
    link : https://react-hook-form.com/docs/useform/watch

```
var name1 = watch('name')
console.log(namw1)
```

---

## React git code clone from react ❌

- clone from github : `git clone url`
- run `npm i`

## INSTRUCTION OF Install React-icons

downloads :

```
npm i react-icons
```

## INSTRUCTION OF Install axios

downloads :

```
npm i axios
```

---

## INSTRUCTION OF Install CustomTheam ❌

Install Yeoman and the VS Code Extension Generator:

```
npm install -g yo generator-code
```

Generate a New Theme Project.

```
yo code
```

Youtube Video : https://www.youtube.com/watch?v=i8zZ6rwItZ4&list=LL&index=10 <br>
Private Github link : https://github.com/Sihambintahabib-ux/vsCode-theme-change.git <br>
Website : https://themes.vscode.one/

---

## Github setup :

- Origin remote (remote repositories associated with the project) :

```
git remote -v
```

- change the remote URL

```
git remote set-url origin `URL : https://github.com/ferdouszihad/dragon-news-firebase.git`
```

- force push

```
git....push --force
```

---

## gitbash default name change :

Step 1: In your Git Bash terminal, type this and press Enter:
`notepad ~/.bashrc`
Step 2: Notepad will open. Add this line at the very bottom:

- for file name with user name:
  `xport PROMPT_DIRTRIM=2`
  or
  `PS1='\u@\h $MSYSTEM \[\033[36m\]\W\[\033[0m\]\n\$ '`

- for user name only with style :
  ` PS1="\[\033[32m\]\u@\h \[\033[35m\]$MSYSTEM \[\033[0m\]\$ "`

- for user name only , no-style :
  `PS1='\u@\h $MSYSTEM\n\$ '`
- for file name
  `PS1='\u@\h $MSYSTEM \[\033[36m\]\W\[\033[0m\]\n\$ '`
- for username and 2 folder name :
  ````PROMPT_COMMAND='SHORT_PATH=$(pwd | grep -o "[^/]*/[^/]*$")'
  PS1='\u@\h $MSYSTEM /\[\033[36m\]$SHORT_PATH\[\033[0m\]\n\$ ' ```
  ````
- for custom message :
  `parse_git_branch() {
  git branch 2>/dev/null | grep '*' | sed 's/* //'
}
PROMPT_COMMAND='SHORT_PATH=$(pwd | grep -o "[^/]*/[^/]*$")'
PS1='\[\033[35m\]⚡ Keep Coding\[\033[0m\] | \[\033[36m\]$SHORT_PATH\[\033[0m\] \[\033[33m\]$(parse_git_branch)\[\033[0m\] \$ '`

claude link : https://claude.ai/share/ac61623e-3a54-4617-9855-36f0692b6005

---

## sent img by imgdb img upload :

1. Get Your API Key

Go to https://api.imgbb.com/
Sign up or log in to your account
Navigate to your dashboard to get your API key
Copy and save your API key securely

2. Prepare Your Image

ImgBB accepts images in base64 format or as a direct file upload
Supported formats: JPG, PNG, BMP, GIF, TIF, WEBP
Maximum file size: 32 MB

3. Choose Your Upload Method
   Method A: Upload with Base64 (recommended for web apps)

```
 //* 1.imgfile set :
    var imgfile = image[0];
    // console.log(imgfile);
    const formData = new FormData();
    formData.append("image", imgfile);
    try {
      //* 2.imgfile set :
      const { data } = await axios.post(
        `https://api.imgbb.com/1/upload?key=${
          import.meta.env.VITE_IMGFILE_APIKEY
        }`,
        formData
      );
      console.log(data.data.display_url);
      const imgURL = data?.data?.display_url;
      console.log(imgURL);
      // return;
      //* imgfile set END
       } catch (err) {
      console.log(err);
      toast.error(err?.message);
    }

```

or create a new folder utiles>index.js :

```
import axios from "axios";

export const imageUpload = async (imageData) => {
  const formData = new FormData();
  formData.append("image", imageData);
  const { data } = await axios.post(
    `https://api.imgbb.com/1/upload?key=${import.meta.env.VITE_IMGFILE_APIKEY}`,
    formData
  );
  //   console.log(data.data.display_url);
  //   const imgURL = data?.data?.display_url;
  //   console.log(imgURL);
  return data?.data?.display_url;
};

```

2. then use imageUpload :

```
    const { name, email, image, password } = data;
    var imgfile = image[0];
      const imgURL = await imageUpload(imgfile);

```

---

## Tanstack quary :

1. Download :

```
npm i @tanstack/react-query

```

2. add this in `main.js` : https://tanstack.com/query/latest/docs/framework/react/quick-start

```
import {
  QueryClient,
  QueryClientProvider,
} from '@tanstack/react-query';

// Create a client
const queryClient = new QueryClient()

<QueryClientProvider client={queryClient}>
....
 </QueryClientProvider>

```

- useQuery - for data get : https://tanstack.com/query/latest/docs/framework/react/reference/useQuery
- useMutation - for POST || PATCH || PUT || DELETE - or any type of changes in data : https://tanstack.com/query/latest/docs/framework/react/reference/useMutation

3. useMutation

```
 const mutation = useMutation({
    mutationFn: async (data) => {
      return await axios.post(`${import.meta.env.VITE_API_URL}/clubs`, data);
    },
    onSuccess: (data) => {
      console.log(data);
      // Invalidate and refetch
      QueryClient.invalidateQueries({ queryKey: ["todos"] });
    },
    onError: (errors) => {
      console.log(errors);
    },
    onMutate: (data) => {
      console.log("I will post this data--->", data);
    },
    onSettled: (data, error) => {
      if (data) console.log(data);
      if (error) console.log(error);
    },
    retry: 5,

    //
  });
```

4. destructure useMutation data :

```
 const { isPending, isError, mutateAsync , data ,  reset: mutatereset} = useMutation({
    mutationFn: async (data) => {
      return await axios.post(`${import.meta.env.VITE_API_URL}/clubs`, data);
    },
    onSuccess: (data) => {
      console.log(data);
       mutatereset(),
      // Invalidate and refetch
      QueryClient.invalidateQueries({ queryKey: ["todos"] });
    },
    onError: (errors) => {
      console.log(errors);
    },
    onMutate: (data) => {
      console.log("I will post this data--->", data);
    },
    onSettled: (data, error) => {
      if (data) console.log(data);
      if (error) console.log(error);
    },
    retry: 5,

    //
  });
```

or using axios :

```
 // const { user } = useAuth();
  // const {
  //   isLoading,
  //   isError,
  //   data: adminClubs = [],
  //   // refetch,
  // } = useQuery({
  //   queryKey: ["adminClubs", user?.email],
  //   queryFn: async () => {
  //     const result = await axios(`${import.meta.env.VITE_API_URL}/admin-clubs`);
  //     return result.data;
  //   },
  // });

  // console.log("adminClubs", adminClubs);
  // if (isLoading) return <LoadingSpinner></LoadingSpinner>;
  // if (isError) return <ErrorPage></ErrorPage>;

```

or using axiosSecure for jwt

```
import useAxiosSecure from "../../../hooks/useAxiosSecure";

const { user } = useAuth();
  const axiosSecure = useAxiosSecure();

  const {
    isLoading,
    isError,
    data: adminClubs = [],
    // refetch,
  } = useQuery({
    queryKey: ["adminClubs", user?.email],
    queryFn: async () => {
      const result = await axiosSecure(`/admin-clubs`);
      return result.data;
    },
  });

  console.log("adminClubs", adminClubs);
  if (isLoading) return <LoadingSpinner></LoadingSpinner>;
  if (isError) return <ErrorPage></ErrorPage>;
```

5. use `mutateAsync`

```
 const clubData = {
        clubName: name,
        description,
        category,
        location,
        membershipFee: parseInt(price),
        status: "pending",
        // quantity,
        managerEmail: user.email,
        createAt: new Date(),
        updateAt: new Date(),
        bannerImage: imgURL,
      };

      await mutateAsync(clubData);

```

6. use `isPending`

```
  if (isPending) return <LoadingSpinner></LoadingSpinner>;

```

7. useQuery

```
 const {
    isLoading,
    isError,
    data: clubs = [],
    refetch,
  } = useQuery({
    queryKey: ["clubs"],
    queryFn: async () => {
      const result = await axios(`${import.meta.env.VITE_API_URL}/clubs`);
      return result.data;
    },
  });
```

or complete version

```
 const { user } = useAuth();
  const {
    isLoading,
    isError,
    data: myClubs = [],
    // refetch,
  } = useQuery({
    queryKey: ["myClubs", user?.email],
    queryFn: async () => {
      const result = await axios(
        `${import.meta.env.VITE_API_URL}/my-clubs/${user?.email}`
      );
      return result.data;
    },
  });
  console.log(myClubs);
  if (isLoading) return <LoadingSpinner></LoadingSpinner>;
  if (isError) return <ErrorPage></ErrorPage>;

```

## download tansstack quart :

1.

```
npm i @tanstack/react-query-devtools
```

2. add these line in main.jsx : ` <ReactQueryDevtools initialIsOpen={false} />`

```
import { ReactQueryDevtools } from '@tanstack/react-query-devtools'

function App() {
  return (
    <QueryClientProvider client={queryClient}>
      {/* The rest of your application */}
      <ReactQueryDevtools initialIsOpen={false} />
    </QueryClientProvider>
  )
}
```

---

## delete function :

```
// * delete :
  //* function handleReject
    const axiosSecure = useAxiosSecure(); // custom hook

  const handleDelete = async () => {
    try {
      await axiosSecure.delete(`/club/${_id}`, {
        data: {
          email: data.managerEmail,
          status: "reject",
          updateAt,
        },
      });
      toast.success("club delete");
      console.log(handleReject);
      refetch();
    } catch (error) {
      toast.error(error);
    }
  };
```

## live link :

ASSAIREMENT : 9
git repo link : https://github.com/Sihambintahabib-ux/assairment-9.git
<br>
live link : https://sihambintahabib-assairment-9.surge.sh/services

---

ASSAIREMENT : 10
code : Code For Counting Ass-10 on 60 Marks : (marks60)-ass10#inc-ExM25

client :
git repo link : https://github.com/Sihambintahabib-ux/assairment-10-client.git
<br>
live link : https://sihambintahabib-assairment10.surge.sh/
<br>
server :
git repo link : https://github.com/Sihambintahabib-ux/assairment-10-server.git
<br>
live link : https://assairment10.vercel.app/

## https://vercel.com/sihams-projects-0a3f7554/assairment10

client git repo: https://github.com/Sihambintahabib-ux/assairment-10-client.git
live link : https://sihambintahabib-assairment10.surge.sh/
server git repo: https://github.com/Sihambintahabib-ux/assairment-10-server.git

Code For Counting Ass-10 on 60 Marks : (marks60)-ass10#inc-ExM25

---

ASSAIREMENT : 11

Github serverSite : https://github.com/Sihambintahabib-ux/assairment-11-clientsite.git <br>
Github clientSite : https://github.com/Sihambintahabib-ux/assairment-11-clientsite.git <br>
live link : http://sihambintahabib-assairment11.surge.sh/ <br>
live link : https://graceful-mandazi-0fe39f.netlify.app/ <br>
Admin Gmail : admin@gmail.com <br>
Admin Password : admin@gmail.com <br>

---

## reaxt router queary data get: `useSearchParams`

## reaxt router id get: `useParams`
