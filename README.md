https://www.youtube.com/watch?v=A63UxsQsEbU&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw

npx create-next-app nextninja

pages=>different page will be created here
index.js=>for homepage
\_app.js=>kinda root component, different page components are rendered here
api=>for api endpoints
public=>images, assets

# delete all the code inside index.js

https://www.youtube.com/watch?v=zktJ8-k0JDc&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=2

pages&routes
index pages goes to root address, other files like below about page, goe to rootaddress/about
create a file called about.js inside pages
sfc
then you can directly go to /about address

create ninjas folder inside pages
create test.js inside ninjas folder

if we create index.js inside ninjas folder,
by this index we can directly goto /ninjas page

===================================
https://www.youtube.com/watch?v=MJT_WXdSPjE&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=3

Adding other components

we create components inside another folder,
not inside pages folder,
because we can use these components in all pages.
create comps inside root
then create a file Navbar.js
import it from index.js
test it in the browser
create the footer.js as same as navbar.js
====================================
https://www.youtube.com/watch?v=u8vaAc3ivcY&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=4

Linking between pages

# wrap <a> tags with <Link> tags and add href's

=======================================
https://www.youtube.com/watch?v=DGn25s42NvQ&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=5

Layout file

if we want to show e.g. navbar,footer etc components in every page, instead of importing these components from every page we have,
we create a layout file and import it fro \_app.js, because all pages are rendered here.

import this file from \_app.js and
wrap code with layout.

inside layout be careful with the structure.
now, we can delete the Navbar and footer inside index.js.
==============================================
https://www.youtube.com/watch?v=qKwnlTVAGnA&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=6

Adding styles

we have global.css in the styles folder.
delete all the code within and copy some from repo.it is already imported in the \_app.js
we can create css files for interested components.e.g. Home.module.css is created for index.js. module keyword should be in the naming.so we can use it in th code like className={styles.container}.
delete everything inside Home.module.css and paste from repo.
create Ninjas.module.css inside styles directory.
inside css files, you should have class selectors not element selectors.
=============================================
https://www.youtube.com/watch?v=dlee0ESZvlc&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=7

404 pages
for custom 404 pages, go pages folderand create a file called 404.js page.
==============================================
https://www.youtube.com/watch?v=O3yKwz4wRHc&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=8

Redirecting Users
we use useEffect hook.
useEffect is take place when component is mounted. in 404.hs use it.
================================================
https://www.youtube.com/watch?v=rHncMH1CfCU&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=9

Images and metadata

static assets placed inside public directory.
so change the navbar icon accordingly.

for metadata,
index.js,about.js inside pages,
place Head component above div.
================================================
https://www.youtube.com/watch?v=zueyEdRZQlk&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=10

Fetching data
we will use https://jsonplaceholder.typicode.com
we prefer /users

when we goto /ninjas address,
we gonna use special function,
because in next we use prerendering,
so we will get data before rendering.
we will use getStaticProps.
This function only runs in the build time,
does not run in the browser.

apply css from Ninjas.module.css file, first import it.

=============================================
https://www.youtube.com/watch?v=WPdJaBFquNc&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=11

Dynamic Routes (part 1)

we will go to detail pages for each ninja
structure would be /ninjas/id
create [id].js inside ninjas folder
then change the div inside index.js to Link
and add href to it.
============================================
https://www.youtube.com/watch?v=mAHqpdVzJmA&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=12

Dynamic Routes (part 2)

export getStaticPaths inside [id].js

https://www.youtube.com/watch?v=2zRHlqc0_yw&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=13

Fetching a Single Item

export getStaticProps inside [id].js

=======================================
https://www.youtube.com/watch?v=_8wkKL0LKks&list=PL4cUxeGkcC9g9gP2onazU5-2M-AzA8eBw&index=14

Deploying to Vercel

npm run build
you can see pages created inside
.next/server/pages/ninjas/

vercel deoployment can be easily done via github.
