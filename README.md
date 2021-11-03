![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)
# cmarketprice
Historical commodity prices visualized using Chart.js; submitted as part of Cloudflare's Developer challenge;
Cloudflare Workers code is here: https://github.com/jahabeebs/alphavantageworker 

## Getting Started

Client-side code build process:

```bash
# install dependencies
$ yarn install

# serve with hot reload at localhost:3000
$ yarn dev

# build for production and launch server
$ yarn build
$ yarn start

# generate static project
$ yarn generate
```
To implement the back-end of the project you must register for a free CommoPrices API account to be able to access their free data endpoint. Then, create a Workers KV namespace called PRICES_DB. Set up a Cron job trigger on Cloudflare to ensure new data is pulled into the KV namespace regularly (I recommend a daily trigger). Bind the Cloudflare Worker to the Workers KV using [these](https://developers.cloudflare.com/workers/runtime-apis/kv#kv-bindings) instructions.

## Build Snapshot
Visit https://cmarketprice.com for the production website

## Built With

Client-side code (HTML, Tailwind CSS, JS):
    
[Nuxt.js](https://nuxtjs.org/) - Front-end framework

[Tailwind CSS](https://tailwindcss.com/) - CSS framework

[Vue-chartjs](https://vue-chartjs.org/) - Vue/Nuxt adaptation of Chart.js

[nuxtjs/robots](https://www.npmjs.com/package/@nuxtjs/robots) - Middleware to generate a robots.txt for the website

[Cloudflare Pages](https://pages.cloudflare.com/) - Configured to automatically deploy this repo to production when a successful build is run and avoids CORS issues when working with Cloudflare Workers


Server-side code (Typescript): 

[Cloudflare Workers](https://workers.cloudflare.com/) - Coordinates Cron job and allows front-end to fetch commodity prices from a KV namespace

[Workers KV](https://developers.cloudflare.com/workers/runtime-apis/kv) - An eventually consistent DB that stores the commodity prices data

[Commoprices API](https://api.commoprices.com/) - API used to get free commodity data provided by the World Bank

General Tools:

[Jetbrains Webstorm](https://www.jetbrains.com/webstorm/) - IDE

[Yarn](https://yarnpkg.com/) - Package Manager



