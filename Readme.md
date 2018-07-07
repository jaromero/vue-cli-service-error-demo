# vue-cli-service error demo

**How to reproduce:**

1. `yarn` or `npm install` or `pnpm install --shamefully-flatten`
2. Wait for it
3. `yarn run serve` or `npm run serve` or `pnpm run serve`

And you should see this exception being thrown:

~~~
/home/<your-home-dir>/test/vue-cli/my-app/node_modules/hosted-git-info/index.js:73
      if (!(ex instanceof URIError)) throw ex
                                     ^

TypeError: Cannot read property 'replace' of null
    at /home/<your-home-dir>/test/vue-cli/my-app/node_modules/hosted-git-info/index.js:61:63
    at Array.map (<anonymous>)
    at fromUrl (/home/<your-home-dir>/test/vue-cli/my-app/node_modules/hosted-git-info/index.js:45:39)
    at Function.module.exports.fromUrl (/home/<your-home-dir>/test/vue-cli/my-app/node_modules/hosted-git-info/index.js:32:18)
    at Object.<anonymous> (/home/<your-home-dir>/test/vue-cli/my-app/node_modules/normalize-package-data/lib/fixer.js:150:36)
    at Array.forEach (<anonymous>)
    at Object.<anonymous> (/home/<your-home-dir>/test/vue-cli/my-app/node_modules/normalize-package-data/lib/fixer.js:144:31)
    at Array.forEach (<anonymous>)
    at Object.fixDependencies (/home/<your-home-dir>/test/vue-cli/my-app/node_modules/normalize-package-data/lib/fixer.js:137:41)
    at /home/<your-home-dir>/test/vue-cli/my-app/node_modules/normalize-package-data/lib/normalize.js:32:38
~~~

Also: `npx vue-cli-service serve` or `pnpx vue-cli-service serve` or any vue-cli-service command simply results in the following output:

~~~
Cannot read property 'replace' of null
~~~
