This is a [Next.js](https://nextjs.org/) project bootstrapped with [`create-next-app`](https://github.com/vercel/next.js/tree/canary/packages/create-next-app).

## Getting Started

First, run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

Open [http://localhost:3000](http://localhost:3000) with your browser to see the result.

You can start editing the page by modifying `app/page.tsx`. The page auto-updates as you edit the file.

This project uses [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) to automatically optimize and load Inter, a custom Google Font.

## Learn More

To learn more about Next.js, take a look at the following resources:

- [Next.js Documentation](https://nextjs.org/docs) - learn about Next.js features and API.
- [Learn Next.js](https://nextjs.org/learn) - an interactive Next.js tutorial.

You can check out [the Next.js GitHub repository](https://github.com/vercel/next.js/) - your feedback and contributions are welcome!

## Deploy on Vercel

The easiest way to deploy your Next.js app is to use the [Vercel Platform](https://vercel.com/new?utm_medium=default-template&filter=next.js&utm_source=create-next-app&utm_campaign=create-next-app-readme) from the creators of Next.js.

Check out our [Next.js deployment documentation](https://nextjs.org/docs/deployment) for more details.

# nextjs13-template

# only yarn work this object use package.json

```bash
"engines": {
"node": ">=14.0.0",
"yarn": ">=1.22.0",
"npm": "please-use-yarn"
}
```

## setup prettier

```bash
yarn add -D prettier
create two file
  -- .prettierignore
        .yarn
        .next
        dist
        node_modules
  -- .prettierrc
      {
        "trailingComma": "es5",
        "tabWidth": 2,
        "semi": true,
        "singleQuote": true
      }
prettier run first add package json script line
    "scripts": {
        "prettier": "prettier --write ."
     },

```

yarn add -D husky
npx husky install
npx husky add .husky/pre-commit "yarn lint"
npx husky add .husky/pre-push "yarn build"
npx husky add .husky/commit-msg 'npx --no -- commitlint --edit "$1"'
yarn add -D @commitlint/config-conventional @commitlint/cli
