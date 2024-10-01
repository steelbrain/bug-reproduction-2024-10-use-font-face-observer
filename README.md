# Bug Reproduction

```sh
$ yarn
$ yarn tsc -p tsconfig.json --noEmit
index.ts:1:33 - error TS7016: Could not find a declaration file for module 'use-font-face-observer'. '/Users/aneesiqbal/Projects/steelbrain/bug-reproduction-2024-10-use-font-face-observer/node_modules/use-font-face-observer/dist/index.modern.js' implicitly has an 'any' type.
  There are types at '/Users/aneesiqbal/Projects/steelbrain/bug-reproduction-2024-10-use-font-face-observer/node_modules/use-font-face-observer/dist/index.d.ts', but this result could not be resolved when respecting package.json "exports". The 'use-font-face-observer' library may need to update its package.json or typings.

1 import useFontFaceObserver from 'use-font-face-observer'
                                  ~~~~~~~~~~~~~~~~~~~~~~~~


Found 1 error in index.ts:1

error Command failed with exit code 2.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.
```


As evident from the error message, the "exports" config in package.json is incorrect.
