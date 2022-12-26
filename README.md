Using tools like deno-npm and deno_npm to use npm packages in Deno may introduce some inefficiencies compared to using native Deno modules. These tools work by resolving the dependencies of the npm packages and generating a Deno-compatible module map, which can add additional overhead to the module loading process. In addition, using third-party tools like these may introduce additional dependencies and complexity to your project, which can make it more difficult to understand and maintain.

Many npm packages have been adapted to work with Deno directly, either through direct porting or by using a compatibility layer. In many cases, it may be more efficient and straightforward to use a native Deno module instead of a jerry-rigged workaround.

While tools like specificers, CDNs and adapters may be a good option. Using native Deno modules, or limiting to a few npm packages, is more efficient and straightforward.


# List of npm packages adapted for Deno

| Deno                         | npm/Node                 | Status |
|------------------------------|--------------------------|--------|
| `fs` (Deno standard library) | `fs` (Node.js file system API) | ✔ (adapted to work with Deno) |
| `http` (Deno standard library) | `http` (Node.js HTTP API) | ✔ (adapted to work with Deno) |
| `path` (Deno standard library) | `path` (Node.js path manipulation library) | ✔ (adapted to work with Deno) |
| `util` (Deno standard library) | `util` (Node.js utility library) | ✔ (adapted to work with Deno) |
| `lodash` (Deno module)         | `lodash` (JavaScript utility library) | ✔ (adapted to work with Deno) |
| `moment` (Deno module)         | `moment` (JavaScript date and time library) | ✔ (adapted to work with Deno) |
| `isomorphic-fetch` (Deno module) | `request` (HTTP request library) | ✔ (adapted to work with Deno) |
|`faker` ([Deno module](https://deno.land/x/deno_faker@v1.0.0/build/src/docs.md?source=))| `faker` (fake data generator) | ✔ ( adapted to work with Deno)  |
| `axiod` ([Deno module](https://deno.land/x/axiod@0.26.2))          | `axios` (HTTP request library) | ✔ (adapted to work with Deno)  |
| `pg` (Deno module)             | `pg` (PostgreSQL client library) | ✔ (adapted to work with Deno) |
| `mongo` (Deno module)          | `mongodb` (MongoDB driver library) | ✔ (adapted to work with Deno)  |
| `react` (Deno module)          | `react` (JavaScript library for building user interfaces) | 🍋 (use FreshJS or AlephJS to work with Deno) |
| `redis` (Deno module)          | `redis` (Redis client library) | ❌ (not yet adapted to work with Deno) |
| `bcrypt` (Deno module)         | `bcrypt` (password hashing library) | ❌ (not yet adapted to work with Den
| `crypto` (Deno module)    | `crypto` (cryptographic library) | ❌ (not yet adapted to work with Deno) |
| `dotenv` (Deno module)    | `dotenv` (environment variable library) | ❌ (not yet adapted to work with Deno) |
| `express` (Deno module)   | `express` (web framework) | ❌ (not yet adapted to work with Deno) |
| `jest` (Deno module)      | `jest` (testing framework) | ❌ (not yet adapted to work with Deno) |
| `knex` (Deno module)      | `knex` (SQL query builder) | ❌ (not yet adapted to work with Deno) |
| `mocha` (Deno module)     | `mocha` (testing framework) | ❌ (not yet adapted to work with Deno) |
| `mysql2` (Deno module)    | `mysql2` (MySQL client library) | ❌ (not yet adapted to work with Deno) |
| `passport` (Deno module)  | `passport` (authentication middleware) | ❌ (not yet adapted to work with Deno) |
| `redux` (Deno module)     | `redux` (JavaScript library for managing | ❓ (not clear)
| `express-graphql` (Deno module)| `express-graphql` (GraphQL middleware for Express) | ❌ (not yet adapted to work with Deno) |
| `next` (Deno module)           | `next` (web framework for server-rendered React apps) | ❌ (not yet adapted to work with Deno) |
| `react-router` (Deno module)   | `react-router` (routing library for React) | ❌ (not yet adapted to work with Deno) |
| `chai` (Deno module)           | `chai` (assertion library) | ❌ (not yet adapted to work with Deno) |
| `sinon` (Deno module)          | `sinon` (spy, stub, and mock library) | ❌ (not yet adapted to work with Deno) |
| `supertest` (Deno module)      | `supertest` (HTTP assertion library) | ❌ (not yet adapted to work with Deno) |
| `tape` (Deno module)           | `tape` (test runner) | ❌ (not yet adapted to work with Deno) |
| `winston` (Deno module)        | `winston` (logging library) | ❌ (not yet adapted to work with Deno) 
| `yarn` (Deno module)        | `yarn` (package manager) | ❌ (not yet adapted to work with Deno) |
| `webpack` (Deno module)     | `webpack` (module bundler) | ❌ (not yet adapted to work with Deno) |
| `babel` (Deno module)       | `babel` (JavaScript compiler) | ❌ (not yet adapted to work with Deno) |
| `eslint` (Deno module)      | `eslint` (linter) | ❌ (not yet adapted to work with Deno) |
| `prettier` (Deno module)    | `prettier` (code formatter) | ❌ (not yet adapted to work with Deno) |
| `nodemon` (Deno module)     | `nodemon` (development utility) | ❌ (not yet adapted to work with Deno) |
| `chokidar` (Deno module)    | `chokidar` (file watcher) | ❌ (not yet adapted to work with Deno) |
| `cross-env` (Deno module)   | `cross-env` (environment variable library) | ❌ (not yet adapted to work with Deno) |
| `mock-fs` (Deno module)     | `mock-fs` (file system mocking library) | ❌ (not yet adapted to work with Deno) |
| `nock` (Deno module)        | `nock` (HTTP mocking library) | ❌ (not yet adapted to work with Deno) |
| `rimraf` (Deno module)      | `rimraf` (directory deletion utility) | ❌ (not yet adapted to work with Deno) |
| `sinon-chai` (Deno module)  | `sinon-chai` (Sinon/Chai integration) | ❌ (not yet adapted to work with Deno) |
| `supertest-as-promised` (Deno module) | `supertest-as-promised` (SuperTest/Promises integration) | ❌ (not yet adapted to work with Deno) |
| `nyc` (Deno module)         | `nyc` (test coverage tool) | ❌ (not yet adapted to work with Deno) |

# How to turn an npm module to a package adapted for deno

check out [denoify](https://github.com/garronej/denoify) and [DNT-Oak](https://deno.com/blog/dnt-oak)

# Experimental solution


Npm specifiers are a new feature in Deno that allows you to import npm packages directly from the npm registry using the import statement. To use an npm package with a specifier, you can use a special syntax that includes the package name and version, such as import { readFileSync } from "https://deno.land/x/fs@v0.12.0/mod.ts".

Using npm specifiers has several advantages. It allows you to use npm packages in Deno without having to install them locally or use a package manager, and it allows you to easily manage the version of the package that you are using. However, **npm specifiers are still a work in progress and may not be fully stable yet.**

Another option for using npm packages in Deno is to use CDNs, or content delivery networks. Many npm packages are available on CDNs, and you can import them into Deno by specifying the URL of the package on the CDN. For example, you can use the import statement to import the lodash package from the unpkg CDN like this: 

> import { map } from "https://unpkg.com/lodash@4.17.15/map.js".

Using CDNs to import npm packages is a more established approach, but it has some drawbacks compared to using npm specifiers. CDN URLs can change over time, which can break your imports, and it can be more difficult to manage the version of the package that you are using.
