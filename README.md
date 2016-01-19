# vile-license

A [vile](http://vile.io) plugin for locking down
project dependency [licenses](https://tldrlegal.com).

## Supported Checks

- [npm](http://npmjs.org)
- [bower](http://bower.io)

## Requirements

- [nodejs](http://nodejs.org)
- [npm](http://npmjs.org)

## Installation

    npm i vile-license

## Config

You specify the license types you can have and can't have in your `.vile.yml`.

License strings are valid if the string **occurs** in the license name
being compared, so using both whitelisting and blacklisting are recommended.

## Whitelisting

```yml
license:
  config:
    allowed: MPL-2.0
```

or:

```yml
license:
  config:
    allowed: [
      "MIT",
      "MPL"
    ]
```

### Blacklisting

```yml
license:
  config:
    disallowed: [ "AGPL" ]
```

## Restrictions

Assumes files are in the `cwd`.

## Architecture

- `src` is es6+ syntax compiled with [babel](https://babeljs.io)
- `lib` generated js library

## Hacking

    cd vile-license
    npm install
    npm run dev
    npm test