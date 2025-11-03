# Nuxt Supabase Minimal Starter

This project is the result of:

- Making sure the local system has Node 24.x per Nuxt recommendation.

and following following:

- [Nuxt instructions to create a new project](https://nuxt.com/docs/4.x/getting-started/installation)
- [Nuxt instructions to enable pages feature](https://nuxt.com/docs/4.x/getting-started/views)
- [Supabase Nuxt module instructions to integrate Supabase login](https://supabase.nuxtjs.org/getting-started/introduction)

You will need to copy _.env.example_ to _.env_ and fill in the values for your Supabase.

As of 2025-11-03 following those instructions does not work.

- Going to http://localhost:3000/ redirects to http://localhost:3000/login and there is a button and an email input box but they don't do anything.
- Sending an email invite from Supabase and clicking the link doesn't work (we don't even have the feature implemented to do the set-password flow you'd need for that)
- There is a console log about a problem with the cookie module.

## Cookie Module Issue

```
Uncaught (in promise) SyntaxError: The requested module '/_nuxt/@fs/.../nuxt-supabase-starter/node_modules/cookie/dist/index.js?v=2618301e' does not provide an export named 'parse' (at helpers.js?v=2618301e:1:10)
```

This is a known issue with the Supabase module, [but the solution from the issue comments](https://github.com/nuxt-modules/supabase/issues/488#issuecomment-2812541474) does not work.

## Setup

Make sure to install dependencies:

```bash
# npm
npm install

# pnpm
pnpm install

# yarn
yarn install

# bun
bun install
```

## Development Server

Start the development server on `http://localhost:3000`:

```bash
# npm
npm run dev

# pnpm
pnpm dev

# yarn
yarn dev

# bun
bun run dev
```

## Production

Build the application for production:

```bash
# npm
npm run build

# pnpm
pnpm build

# yarn
yarn build

# bun
bun run build
```

Locally preview production build:

```bash
# npm
npm run preview

# pnpm
pnpm preview

# yarn
yarn preview

# bun
bun run preview
```

Check out the [deployment documentation](https://nuxt.com/docs/getting-started/deployment) for more information.
