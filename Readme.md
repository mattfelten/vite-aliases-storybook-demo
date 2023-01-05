## Demo of `vite-aliases` and Storybook errors

## Setup

Both Storybook versions are set up in this repo. `cd` to the version you want to see and

-   `npm i`
-   `npm run dev` to verify aliases work
-   `npm run storybook` to see Storybook not resolving aliases

## Storybook 6

Storybook 6 does not use the root vite.config.js so it is recommended to import it to `.storybook/main.cjs` to make sure resolvers match. But the vite configs resolvers is empty, since that's handled by `vite-aliases`.

## Storybook 7 (pre-release)

Storybook 7 _does_ lookup the root vite.config.js, so I assumed it might detect `vite-aliases` in the plugin array and use it as well. It doesn't.
