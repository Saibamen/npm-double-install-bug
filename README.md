# npm-double-install-bug

Tested on Windows 10, NPM `10.8.3`, NodeJS `20.17.0`

## Steps

1. `npm install`
2. `npm ci`

### Building with current lock file and `npm ci`

[![Check NPM](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm.yml/badge.svg)](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm.yml)

### Building with fresh lock file, `npm install` and then `npm ci`

[![Check NPM with new lock file](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-new-lock.yml/badge.svg)](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-new-lock.yml)

## Annoying workaround

[![Check NPM with workaround](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-workaround.yml/badge.svg)](https://github.com/Saibamen/npm-double-install-bug/actions/workflows/check-npm-workaround.yml)

1. Delete `node_modules`
2. `npm install`
3. `npm ci`
