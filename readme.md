# Shared Prisma Client Example

You have to publish it to your private (or not?) npm registry and install it as dependency to each project that uses it.
Also, you need to install `@prisma/client` and `prisma` as dependencies since they are peer dependencies of this package.

Client generation executed on `postinstall` hook on each project that uses this package, not on publish.

Example:

`yarn add @your-npm-scope/prisma-client @prisma/client prisma`

or

`npm install @your-npm-scope/prisma-client @prisma/client prisma`

Another possible way to install it without publishing to npm registry, is to use git url, instead of npm package name:
`yarn add git+https://github.com/igolka97/shared-prisma-client-example.git` with `#tagnameOrCommitSHA` if needed.

In your code at some microservice:

```ts
import { PrismaClient } from '@your-npm-scope/prisma-client'
const db = new PrismaClient()
```
