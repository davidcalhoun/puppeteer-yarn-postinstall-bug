# puppeteer-yarn-postinstall-bug

Minimal reproduction for Puppeteer bug ticket - see https://github.com/puppeteer/puppeteer/issues/9304

## Installation
1. Install [Node.js](https://nodejs.org/en/) which comes with npm.
1. `git clone git@github.com:davidcalhoun/puppeteer-yarn-postinstall-bug.git && cd puppeteer-yarn-postinstall-bug`
1. `yarn install`
1. `yarn node test.js`

Output error:

```
dcalhoun@Davids-MBP-2 puppeteer-yarn-postinstall-bug % yarn node test.js
file:///Users/dcalhoun/dev/puppeteer-yarn-postinstall-bug/.yarn/cache/puppeteer-core-npm-19.2.2-830fad0e0f-5d27545666.zip/node_modules/puppeteer-core/lib/esm/puppeteer/node/ProductLauncher.js:94
                    throw new Error(`Could not find Chromium (rev. ${this.puppeteer.browserRevision}). This can occur if either\n` +
                          ^

Error: Could not find Chromium (rev. 1056772). This can occur if either
 1. you did not perform an installation before running the script (e.g. `npm install`) or
 2. your cache path is incorrectly configured (which is: /Users/dcalhoun/dev/puppeteer-yarn-postinstall-bug/.cache/puppeteer).
For (2), check out our guide on configuring puppeteer at https://pptr.dev/guides/configuration.
    at ChromeLauncher.resolveExecutablePath (file:///Users/dcalhoun/dev/puppeteer-yarn-postinstall-bug/.yarn/cache/puppeteer-core-npm-19.2.2-830fad0e0f-5d27545666.zip/node_modules/puppeteer-core/lib/esm/puppeteer/node/ProductLauncher.js:94:27)
    at ChromeLauncher.executablePath (file:///Users/dcalhoun/dev/puppeteer-yarn-postinstall-bug/.yarn/cache/puppeteer-core-npm-19.2.2-830fad0e0f-5d27545666.zip/node_modules/puppeteer-core/lib/esm/puppeteer/node/ChromeLauncher.js:160:25)
    at ChromeLauncher.launch (file:///Users/dcalhoun/dev/puppeteer-yarn-postinstall-bug/.yarn/cache/puppeteer-core-npm-19.2.2-830fad0e0f-5d27545666.zip/node_modules/puppeteer-core/lib/esm/puppeteer/node/ChromeLauncher.js:64:37)
    at async file:///Users/dcalhoun/dev/puppeteer-yarn-postinstall-bug/test.js:4:19
```