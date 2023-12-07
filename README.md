# Introduction to NextJS - Training Course

## miguel-posada

### Routing

\_Routing is based on folder and a parent and children structure. is delimited by slashes
first the domain and later
\_is important understand that there is two ways of create routes in a NextJS App

- using App Router structure
- using Pages Router structure

**Static Routing:**
_creating folders and inside them a page.tsx or page.jsx page. is posible to avoid type in the URL the name of the
folders in the route using parenthesis '()' in folders_
**Dinamic Routing**
is posible to create dynamic routes usig the [] keys wrapping the folder (e.g [id]) where i want to use dynamic routes
when you need to get the value just pass 'params' and get the value inside the component like 'params.id'

**Rendering**

_server component_

aloows to write UI that can be cached on the server based on route segments. by default NextJS Uses Server Components.
this is importatnt because:

- 'Data Fetching' performance
- 'caching' results and
- 'streaming' by split in chunks the loading info
- 'Initial page Load' FCP First Contentfull Paint
  generally Server components are rendered adapting to the Server Component Payload (RSC Payload) and client components to render HTML

  +Static Rendering\*

  - Routes are rendered at _build Time_ data is cached and pushed to a Content Delivery Network (CDN)
  - used to data that is not personalized to the user like staic blog post or a product page

  _*Dynamic Rendering*_

  - Routes are rendered for each user at _request time_
  - data personalized to the user like cookies or UrL's search params.
  - uses Dynamics functions like cookies() or HEaders()

by default developer doesn't need to know about rendering strategy. that is calculated by NextJs

_*Client Components*_

    - can use state, effects and event listeners
    - client Components have acces to Browsers API's like geolocalization and LocalStorage
    - is necessary to use the 'use client' directive

_*Composition Pattern*_

Client component Vs Server component
add interactivity and event listeners || Fetch data
use state and lifecycle effects || access backend resources
use browser only-API's and custom Hooks || Keep sensitive information(tokens, api keys)

**Layouts and Templates**
is very important to have a Layout file inside of every folder to share between different folder pages.
they wrap a page usefull for navigation UI elements. Layout are rendered once and by convention it must be named as 'Layout.(tsx,jsx,ts)'

**Nvigation**
that was created in the root layout and using best HTML semantics principle
also React <Link> tag

**Styling**
there are many ways to add styling to every folder component. it depends of the needs
but is recommended to use _Tailwind or .module.css extension_ (e.g. styles.module.css)
+-.module.css-+
inside component:
import styles from './styles.module.css' and with this class defined inside component
.dashboard {
padding: 24px;
}
to call inside component is like:
className={styles.dashboard} and
+-Tailwind-+
to use this framework check this guideline https://nextjs.org/docs/app/building-your-application/styling/tailwind-css

another way is using
_Saas_
https://nextjs.org/docs/app/building-your-application/styling/sass
and
_Css-in-JS_
https://nextjs.org/docs/app/building-your-application/styling/css-in-js
_Connecting with a DB Prisma_
is very simple and is necesary to use an Actions File
_Loading And error pages_
only create both pages with same name and wrap inside a Promise
to resolve for 'Loading' and eject for 'Error'
_Server Mutation_

**Server Action Mutation and Forms**
https://nextjs.org/docs/app/building-your-application/data-fetching/forms-and-mutations

<form action={create}> takes the FormData based on actions defined in actions.ts file

**API Routes**
create a file called 'api' and define const GET,POST,UPDATE and some others needed

**Middleware**
create middleware file and follow best NextJS practices and conventions
https://nextjs.org/docs/app/building-your-application/routing/middleware

**Deployment**
finally the solution was deployed in veicel and URL is https://next-js-introduction-course.vercel.app/heroku
