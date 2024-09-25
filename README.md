# npm-double-install-bug

Tested on Windows 10, NPM `10.8.3`, NodeJS `20.17.0`

## Error for `npm ci`

```sh
npm error `npm ci` can only install packages when your package.json and package-lock.json or npm-shrinkwrap.json are in sync. Please update your lock file with `npm install` before continuing.
npm error
npm error Invalid: lock file's yaml@1.10.2 does not satisfy yaml@2.5.1
npm error Missing: yaml@1.10.2 from lock file
```

## Steps

1. `npm install`
2. `npm ci`

### Building with current lock file and `npm ci`

[![Check NPM](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm.yml/badge.svg)](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm.yml)

### Building with fresh lock file, `npm install` and then `npm ci`

[![Check NPM with new lock file](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-new-lock.yml/badge.svg)](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-new-lock.yml)

## Annoying workaround

### Workaround v1

[![Check NPM with workaround](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-workaround.yml/badge.svg)](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-workaround.yml)

1. `npm install`
2. Delete `node_modules`
3. `npm install`
4. `npm ci`

### Workaround v2

Just run `npm install` twice, no need to delete `node_modules`.

[![Check NPM with workaround](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-workaround.yml/badge.svg)](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-workaround.yml)

1. `npm install`
2. `npm install`
3. `npm ci`
