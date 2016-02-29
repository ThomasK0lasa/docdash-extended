# Docdash

[![npm](https://img.shields.io/npm/v/docdash.svg)](docdash on npm) [![npm](https://img.shields.io/npm/l/docdash.svg)](license MIT)

A clean, responsive documentation template theme for JSDoc 3.

![docdash-screenshot](https://cloud.githubusercontent.com/assets/447956/13398144/4dde7f36-defd-11e5-8909-1a9013302cb9.png)

![docdash-screenshot-2](https://cloud.githubusercontent.com/assets/447956/13401057/e30effd8-df0a-11e5-9f51-66257ac38e94.jpg)

## Install

```bash
$ npm install --save-dev docdash
```

## Simple usage with cli

Clone repository to your designated `jsdoc` template directory, then:

```bash
$ jsdoc entry-file.js -t path/to/docdash
```

## Usage with build process

In your projects `package.json` file add a generate script:

```json
"script": {
  "generate-docs": "node_modules/.bin/jsdoc --configure .jsdoc.json"
}
```

In your `.jsdoc.json` file, add a template option.

```json
"opts": {
  "template": "node_modules/dodash"
}
```

## Sample `.jsdoc.json`

```json
{
    "tags": {
        "allowUnknownTags": false
    },
    "source": {
        "include": "../js",
        "includePattern": ".js$",
        "excludePattern": "(node_modules/|docs)"
    },
    "plugins": [
        "plugins/markdown"
    ],
    "opts": {
        "template": "assets/template/minami-master/",
        "encoding": "utf8",
        "destination": "docs/",
        "recurse": true,
        "verbose": true
    },
    "templates": {
        "cleverLinks": false,
        "monospaceLinks": false
    }
}
```

## Thanks

Thanks to [lodash](https://lodash.com/docs) and [minami](https://github.com/nijikokun/minami).

## License

Licensed under the Apache2 license. (see [license](LICENSE.md)).