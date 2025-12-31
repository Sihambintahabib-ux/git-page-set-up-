<!-- ![](./NextJS.drawio.svg) -->

<!-- https://nextjs.org/docs/app/api-reference/file-conventions/src-folder
https://nextjs.org/learn/dashboard-app/navigating-between-pages
https://nextjs.org/docs/app/guides/caching
https://nextjs.org/docs/pages/api-reference/components/image#props
https://nextjs.org/docs/app/getting-started/project-structure#routing-files -->

---

ROADMAP:

1. [Instalation](https://nextjs.org/docs/app/getting-started/installation#quick-start)
2. [File structure explain](https://nextjs.org/docs/app/getting-started/project-structure)
3. [Routing Files](https://nextjs.org/docs/app/getting-started/project-structure#routing-files)

- [Nested routes](https://nextjs.org/docs/app/getting-started/project-structure#nested-routes)
- [Dynamic routes](https://nextjs.org/docs/app/getting-started/project-structure#dynamic-routes)

6. [linking-and-navigating](https://nextjs.org/docs/app/getting-started/linking-and-navigating)

- [How navigation works](https://nextjs.org/docs/app/getting-started/linking-and-navigating#how-navigation-works)

7. [Nested routes](https://nextjs.org/docs/app/getting-started/project-structure#nested-routes)
8. [useRouter](https://nextjs.org/docs/app/api-reference/functions/use-router#userouter)

---

QUERYIES:

1. File name first alphabet capital or small letter

2. Should I use JS or JSX for my pages, components and layout files in Next JS 12?

- https://www.reddit.com/r/nextjs/comments/rgu35x/should_i_use_js_or_jsx_for_my_pages_components/
- https://www.geeksforgeeks.org/reactjs/what-is-the-difference-between-a-js-and-jsx-file-in-react/

3. [useRouter()](https://nextjs.org/docs/app/api-reference/functions/use-router#userouter:~:text=%7D-,useRouter(),-router.push(href)

- router.push('/dashboard')
- router.replace('/dashboard')
- router.refresh()
- router.prefetch('/dashboard')
- router.back()
- router.forward()

4.

---

# Module 69.1

## React in a Nutshell: The Core Principles

1. Component-Based UI : Building complex Uls from small, isolated, and readability - reusable pieces.
2. Hool API : Enabling state and lifecycle features within functional components, simplifying logic reuse.
3. Virtual DOM : An efficient update mechanism that minimises direct manipulation of the browser's DOM for performance gains.
4. SPA Benefits : Delivering dynamic, app-like experiences with seamless transitions and responsive interactions.

## Why We Choose React Over Vanilla JavaScript

1. Component Reusability : React's modular structure promotes efficient code reuse across different parts of an application.
2. Faster Rendering : The Virtual DOM optimises Ul updates, leading to a smoother and more performant user experience.
3. Vast Ecosystem : A rich array of libraries, tools, and a large community support React development, offering solutions for almost any problem.
4. Simplified State Management : React provides clear patterns for managing Ul state, making complex applications easier to dev

## React's Limitations: Challenges in Isolation

1. SEO Challenges : Clint-Side Rendering can hinder search engine optimisation, as content is not immediately available to crawlers.
2. Client-Side Only :Primarily focused on client-side rendering, which can impact initial load times and overall performance.
3. Slow First Contentful Paint : Users often experience a blank page while JavaScript loads, leading to a poorer initial user experience.

---

![](./NextJS.drawio.svg)

---

## React's Limitations: Challenges in Isolation

1. No Built-in Routing : Requires external libraries like React Router for navigation, adding to project setup complexity.
2. Performance Heavy on Client : Heavy reliance on client-side processing can strain device resources, especially on less powerful hardware.
3. Reliance on External Libraries : Projects often depend on numerous third-party libraries for essential functionalities, increasing bundle size and maintenance overhead.
   - TanStack : to fetch data
   - Firebase : for authentication
   - Axios - to fetch data
   - React Router - for page routing
   - Express JS - backend
   - npm - npm is the default package manager for the JavaScript runtime environment Node.js.

## Client-Side Rendering (CSR): The Traditional Flow

In CSR, the browser receives a minimal HTML document and then fetches and executes JavaScript to render the full content.

Empty HTML
Load JS
Fetch Data
Render Content

```mermaid
    flowchart LR;
    A[Empty HTML] --> B[Load JS];
    B --> C[Fetch Data];
    C --> D[Render Content];
    D --> E[End];


```

This model can lead to slower initial page loads and SEO issues as search engines might struggle to index dynamic content.

## Next.js to the Rescue: Overcoming React's Limitations

Next.js was created to address the inherent challenges of pure Client-Side Rendered React applications.

1. SEO Friendly : Utilises Server-Side Rendering (SSR) and Static Site Generation (SSG) for better search engine indexing.
2. Faster Initial Load : Pre-rendering strategies deliver fully formed HTML to the browser, significantly improving First Contentful Paint.
3. Built-in Routing : Offers an intuitive file-system based routing solution, simplifying navigation setup.
4. API Routes & Optimisation : Provides API routes for backend functionalities and optimisations for images and fonts out-of-the-box.

---

| React Limitation         | Next.js Solution                  | Benefit                                                                                 |
| ------------------------ | --------------------------------- | --------------------------------------------------------------------------------------- |
| SEO Issues               | SSR / SSG                         | Improved search engine visibility and ranking.                                          |
| No Built-in Routing      | File-Based Routing                | Simplified, intuitive navigation and URL management.                                    |
| Complex Data Fetching    | Server Components, 'fetch' API    | Streamlined data access directly on the server, reducing client-side load.              |
| Slow Initial Performance | Pre-rendering, Image Optimisation | Faster page loads, better user experience, and improved Core Web Vitals.                |
| No Backend               | API Routes, Middleware            | Full-stack capabilities within a single codebase, eliminating separate backend servers. |

---

## From Fragmented Ecosystem to Unified Framework

Before Next.js, building a full-stack React application required integrating numerous disparate libraries and tools.

- React Ecosystem (Before Next.js)
  1. React Router for navigation
  2. React Router
  3. Express.js for backend
  4. Axios/Fetch for data requests
  5. TanStack Query for state management
  6. Firebase for database/auth
  7. Manual SEO solutions
  8. Complex deployment strategies
  9. Firebase
  10. ExpressJS
  11. TanStack Query
  12. axios
- Next.js All-in-One Approach
  1. Built-in Router
  2. Integrated API Routes
  3. Middleware for request handling
  4. Incremental Static Regeneration (ISR)
  5. Automated Image Optimisation
  6. Full-stack development capabilities

---

Framework vs. Library: A Clear Distinction

**Next.js: The Full Framework**

- Routing
- Authentication
- Caching
- Optimization
- API Dev.
- Built-in features

Offers a comprehensive structure and opinionated solutions for building production-ready React applications. It integrates routing, data fetching and build optimization

**React: The UI Library**

- Built-in Functions
- UI management
- Flexibility

Provides tools for building user interfaces. It's a foundation that allows developers immense flexibility but requires ... for a complete application.

---

**Next.js: The Modern Choice for Production-Grade Applications**

By embracing Next.js, we leverage a powerful tool that transforms React into a full-stack, high-performance platform.

- **Enhanced SEO**

Achieve higher search engine rankings with server-side rendering and static site generation.

- **Superior Performance**

Deliver lightning-fast load times and smooth user experiences through advanced optimisations.

- **Full-Stack Capabilities**

**Develop both frontend and backend within a single, cohesive framework.**

- **Industry Standard**

Align with current industry best practices and a thriving developer ecosystem.

---

# Module 69.2 + 69.3 File explaine

## [Instalation](https://nextjs.org/docs/app/getting-started/installation#quick-start) ❌

1. Create a new Next.js app named my-app
2. cd my-app and start the dev server.
3. Visit http://localhost:3000.

```
npx create-next-app@latest my-app --yes
cd my-app
npm run dev
```

--yes skips prompts using saved preferences or defaults. The default setup enables TypeScript, Tailwind, ESLint, App Router, and Turbopack, with import alias @/\*.

- Type `node -v` to node.js version [Minimum Node.js version: 20.9]

## Create with the CLI ✅

The quickest way to create a new Next.js app is using create-next-app, which sets up everything automatically for you. To create a project, run:

```
npx create-next-app@latest
```

- then press `y`
- file name : `my-app` or path define `.`
- choose `No, customize settings`
- Would you like to use TypeScript? - `no`
- Which linter would you like to use? `ESLint`
- Would you like to use React Compiler? » `No` / Yes
- √ Would you like to use Tailwind CSS? ... No / `Yes`
- √ Would you like your code inside a `src/` directory? ... No / `Yes`
- √ Would you like to use App Router? (recommended) ... No / `Yes`
- √ Would you like to customize the import alias (`@/*` by default)? ... `No` / Yes

## Manual installation

To manually create a new Next.js app, install the required packages: [not recomended]

```
npm i next@latest react@latest react-dom@latest

```

---

## after intalation run the code :

1. To start the code : `npm run dev`

![next.js run ](image.png)

2. search localhost in chrome , then it will start compiling : http://localhost:3000
3. it is ready :
   ![alt text](image-1.png)

## File structure explain :

- [src floder](https://nextjs.org/docs/app/api-reference/file-conventions/src-folder#:~:text=Copy%20page-,src%20Folder,-Last%20updated%20October)
  - favicon
  - globalcss.css - all required css
  - layout.js - root file
  - page.js - childern of root file

---

## [File structure explain](https://nextjs.org/docs/app/getting-started/project-structure) :

When you create a new **Next.js** project with `npx create-next-app@latest` (Next.js 15+ as of late 2025) and select **no TypeScript** (while keeping other defaults like ESLint, Tailwind CSS, src/ directory if chosen, and App Router), the structure is very similar to the TypeScript version but uses plain JavaScript files.

The main differences are:

- Files in `app/` use `.js` (or `.jsx` if needed) instead of `.tsx`.
- No `tsconfig.json`.
- Includes `jsconfig.json` for better editor support (like path aliases and IntelliSense in VS Code).
- Tailwind config remains `.ts` (or `.js` in some setups), but it's compatible.

Here's the typical default structure (assuming you selected the optional `src/` directory, as many do for organization; if not, `app/` and `public/` are directly in the root).

```
my-next-app/
├── app/                  # Core routing and UI (App Router)
│   ├── layout.js         # Root layout (required, wraps all pages with <html> and <body>)
│   ├── page.js           # Home page (renders at /)
│   ├── globals.css       # Global styles (includes Tailwind base if selected)
│   └── favicon.ico       # Default favicon
├── public/               # Static assets (served as-is)
│   └── vercel.svg        # Example image (or similar placeholder)
├── src/                  # Optional: All application code (if selected; otherwise app/ is at root)
│   └── (app/ moves here as src/app/ if chosen)
├── .gitignore
├── jsconfig.json         # JavaScript config for editor features (replaces tsconfig.json)
├── next.config.js        # Next.js configuration
├── package.json          # All installed package and dependency file denote here
├── tailwind.config.ts    # Tailwind config (often .ts even in JS projects; works fine)
├── postcss.config.js     # For Tailwind/PostCSS
├── eslint.config.mjs     # ESLint config (if selected) (define all error and how )
└── README.md
```

### Key Folders Explained (Same as TypeScript Version)

- **app/** → Defines routes via folder structure.

  - Nested folders = nested routes (e.g., `app/blog/page.js` → `/blog`).
  - Special files: `layout.js`, `page.js`, `loading.js`, `error.js`, etc.
  - Root `app/layout.js` is required for the whole app.
  - Root `app/page.js` is your homepage.

- **public/** → Static files like images, fonts, etc. (e.g., `/public/logo.png` → accessible at `/logo.png`).

- **src/** (optional) → Keeps your code separate from config files. Highly recommended for medium+ projects.

### Other Notes

- You can still add JSX in `.js` files (Next.js handles it).
- If you later want TypeScript, just rename files to `.tsx` and add `tsconfig.json`—Next.js supports it seamlessly.
- As you build, common additions: `proxy.ts` (private route secure by navigate unregister user to login page ) or `middleware.js` , `components/` folder, `lib/` or `utils/` for helpers.
- `@/` import alias

### type of folder :

- [Top level folder](https://nextjs.org/docs/app/getting-started/project-structure#top-level-folders) :
  - [top level files](https://nextjs.org/docs/app/getting-started/project-structure#top-level-files)
- [Route folder](https://nextjs.org/docs/app/getting-started/project-structure#routing-files) :

This setup leverages React Server Components by default, just like the TypeScript version. For the absolute latest details, refer to the official Next.js docs at nextjs.org/docs/getting-started/project-structure. Start building—it's straightforward in plain JS!

# Module 69.4 Route

[Next JS FILE](./Next%20JS%20_%20Practice%20Sheet%20.pdf)
[Next JS \_ Practice Sheet .pdf](https://github.com/user-attachments/files/24365304/Next.JS._.Practice.Sheet.pdf)

---

### Routing & Nested Routes in Next.js App Router (Next.js 16+, December 2025)

Next.js uses **file-system-based routing** in the `app/` directory. The folder structure directly defines your app's URL routes. Nested routes are created simply by nesting folders — no extra configuration needed.

#### Basic Routing Example

**Folder Structure**:

```
app/
├── page.tsx              → Route: /
├── about/
│   └── page.tsx          → Route: /about
├── contact/
│   └── page.tsx          → Route: /contact
└── blog/
    └── page.tsx          → Route: /blog
```

**Explanation**:

- Every folder inside `app/` represents a **route segment**.
- A folder only becomes a public route when it contains a `page.tsx` file.
- The root `app/page.tsx` is the homepage (`/`).
- `app/about/page.tsx` creates the `/about` page.
- `app/about/page.tsx` here `/page.tsx` is the route render page as child of app page.

#### Nested Routes Example

Nested routes allow you to create deeper URLs like `/dashboard/settings/profile`.

**Folder Structure**:

```
app/
├── page.tsx                          → /
├── dashboard/
│   ├── page.tsx                      → /dashboard
│   ├── layout.tsx                    → Shared layout for all /dashboard/* routes
│   ├── settings/
│   │   ├── page.tsx                  → /dashboard/settings
│   │   └── profile/
│   │       └── page.tsx              → /dashboard/settings/profile
│   └── analytics/
│       └── page.tsx                  → /dashboard/analytics
```

**Explanation**:

- `app/dashboard/page.tsx` → `/dashboard` (main dashboard page)
- `app/dashboard/settings/page.tsx` → `/dashboard/settings`
- `app/dashboard/settings/profile/page.tsx` → `/dashboard/settings/profile`
- The URL path mirrors the folder nesting exactly.

---

# Module 69.5 - nented route with nav link + useRouter()

## Type of linking and navigating

[Server Rendering](https://nextjs.org/docs/app/getting-started/linking-and-navigating#server-rendering:~:text=the%20following%20concepts%3A-,Server%20Rendering,-Prefetching)
[Prefetching](https://nextjs.org/docs/app/getting-started/linking-and-navigating#prefetching)
[Streaming](https://nextjs.org/docs/app/getting-started/linking-and-navigating#streaming)
[Client-side transitions](https://nextjs.org/docs/app/getting-started/linking-and-navigating#client-side-transitions)

## Server Rendering

Next.js automatically prefetches routes linked with the `<Link>` component when they enter the user's viewport. [Page doesent reload to fetch the data]

```
import Link from 'next/link'

export default function Layout() {
  return (
    <html>
      <body>
        <nav>
          {/* Prefetched when the link is hovered or enters the viewport */}
          <Link href="/blog">Blog</Link>
          {/* No prefetching */}
          <a href="/contact">Contact</a>
        </nav>
        {children}
      </body>
    </html>
  )
}
```

## Prefetching

## Streaming

## Client-side transitions

#### How Layouts Work with Nested Routes (Key Benefit)

Layouts are automatically nested too, which is perfect for shared UI.

**Example Files**:

1. **Root Layout** (`app/layout.tsx`) – wraps **everything**:

```tsx
export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```

2. **Dashboard Layout** (`app/dashboard/layout.tsx`) – wraps all routes under `/dashboard/*`:

```tsx
export default function DashboardLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <div className="flex min-h-screen">
      <aside className="w-64 bg-gray-800 text-white p-4">
        <h2>Dashboard Sidebar</h2>
        <nav>
          <Link href="/dashboard">Overview</Link>
          <Link href="/dashboard/settings">Settings</Link>
          <Link href="/dashboard/analytics">Analytics</Link>
        </nav>
      </aside>
      <main className="flex-1 p-8">{children}</main>
    </div>
  );
}
```

**Result When Visiting `/dashboard/settings/profile`**:

- The page content comes from `app/dashboard/settings/profile/page.tsx`.
- It is wrapped by:
  1. Dashboard Layout (`app/dashboard/layout.tsx`) → adds sidebar
  2. Root Layout (`app/layout.tsx`) → adds `<html>` and `<body>`
- When navigating between `/dashboard/analytics` and `/dashboard/settings`, the **sidebar stays intact** (no re-render or flicker) because only the changing segment (the page) updates. This is called **partial rendering** — a huge performance and UX win.

#### Dynamic Nested Routes (Bonus Example)

You can combine nesting with dynamic segments:

```
app/
└── blog/
    ├── page.tsx                  → /blog (list of posts)
    └── [slug]/
        └── page.tsx              → /blog/my-first-post (individual post)
```

- `[slug]` captures the dynamic part of the URL.
- Params are available via `{ params: { slug: string } }` in the page component.

#### Summary Table

| Folder Path                               | URL Route                     | Purpose                       |
| ----------------------------------------- | ----------------------------- | ----------------------------- |
| `app/page.tsx`                            | `/`                           | Homepage                      |
| `app/about/page.tsx`                      | `/about`                      | Static page                   |
| `app/dashboard/page.tsx`                  | `/dashboard`                  | Dashboard root                |
| `app/dashboard/settings/page.tsx`         | `/dashboard/settings`         | Nested page                   |
| `app/dashboard/settings/profile/page.tsx` | `/dashboard/settings/profile` | Deeply nested page            |
| `app/dashboard/layout.tsx`                | (all /dashboard/\*)           | Shared layout (e.g., sidebar) |

Nested routes + nested layouts make building complex apps (dashboards, admin panels, multi-step forms) clean, performant, and intuitive. No need for complex routing libraries!

For a live example, check the tutorial repo: https://github.com/learnwithsumit/next14-crash-course (look in the `app/` folder).

---

## convert server site rendering to client site rendering

- add these at line 1/ first line to any components to make ssr to csr : `use client`

## [useRouter](https://nextjs.org/docs/app/api-reference/functions/use-router#userouter) hook

- how to import :

```
import { useRouter) from "next/navigation";

const router useRouter();
```

- example :

```
'use client' <!-- conver to ssr -> csr -->

import { useRouter } from 'next/navigation' <!-- import useRouter -->

export default function Page() {
  const router = useRouter()   <!-- call hook -->

  return (
    <button type="button"
    onClick={() => router.push('/dashboard')    <!-- navigate to /dashboad page -->
    }>
      Dashboard
    </button>
  )
}
```

## useRouter() = router

- router.push('/dashboard')
- router.replace('/dashboard')
- router.refresh()
- router.prefetch('/dashboard')
- router.back()
- router.forward()
-

# Module 69.6

---

# Module 69.7

---

# Module 69.8

---

# Module 69.9

---
