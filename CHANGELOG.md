# ts-nextjs-tailwind-starter changelog

## 0.2.1

Uses BetterComments and adds TailwindCSS to the local settings.json

This changelog is manually generated and not accurate with the package.json, only to show the changes since the last release.

## 1.0.0 - 2023-07-17

### New Features

- #### Next.js App Router

    Now uses the new app directory structure.

### Improvements & Bug Fixes

- #### Rename `clsxm` to `cn`

    For better support with shadcn/ui

- #### Faster Lint Actions

    Lint jobs is now merged into one for faster performance, also updated the concurrency rule

## 0.5.4 - 2022-07-22

### New Features

- #### Release Please

    Standard Version is now deprecated, and ts-nextjs-tailwind-starter is now using release please. Activate them on `.github/workflows/release-please`

### Improvements & Bug Fixes

- #### More Efficient Lint Actions

    Lint workflow is now cached and will cancel previous run if there are 2 concurrent runs.

## 0.5.3 - 2022-02-27

### New Features

- #### Shimmer for NextImage and Skeleton

    Addition of shimmer & blur placeholder for NextImage, and new Skeleton Component with shimmer effect.

    <https://user-images.githubusercontent.com/55318172/155867729-8c3176ad-ede4-4443-b42b-780517615e5a.mp4>

- #### Support for SVGR

    You can directly import SVG like

    ```tsx
    import Vercel from '~/svg/Vercel.svg';

    <Vercel className='text-5xl' />
    ```

- #### Public Folder Path Mapping

    Easily access public folder with `~/` prefix.

- #### Tailwind CSS Prettier Sorter

    ts-nextjs-tailwind-starter now use first-party plugin `prettier-plugin-tailwindcss`

### Improvements & Bug Fixes

- #### Layout Declared Twice

    Fix issue where adding elements to Layout ends up rendering them twice

- #### ESLint Curly Brace Rule

    New autofixable rule

    ```tsx
    props={'hi'}

    will become

    props='hi'
    ```

## 0.5.2 - 2021-12-30

### New Features

- #### New Component: PrimaryLink

    Add a link component with accent color on top of UnstyledLink.

### Improvements & Bug Fixes

- #### Unused Import ESlint Autofix

    Unused import will automatically be removed by the ESlint autofix.

- #### Renamed CustomLink to UnderlineLink

    This is to compensate the new PrimaryLink component

#### Region Comment

It is really useful when we need to group code. It is also collapsible in VSCode

Snippets: `reg`

```tsx
//#region  //*============== FORM SUBMIT
//#endregion  //*============== FORM SUBMIT
```

You should also use [Better Comments](https://marketplace.visualstudio.com/items?itemName=aaron-bond.better-comments) extension.
