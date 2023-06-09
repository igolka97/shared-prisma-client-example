# Shared Prisma Client Example

This package uses prisma client as peer dependency and exports a generated prisma client.
So you need to install `@prisma/client` and `prisma` as dependencies to each project that uses this package.

Client generation executed on `postinstall` hook on each project that uses this package.

Example:

`yarn add @your-npm-scope/prisma-client @prisma/client prisma`

or

`npm install @your-npm-scope/prisma-client @prisma/client prisma`
