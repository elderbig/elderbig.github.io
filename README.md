# 简介

> An awesome project.

* Installation

```
npm i docsify-cli -g
# yarn global add docsify-cli

```

* init docsify

```
docsify init <path> [--local false] [--theme vue] [--plugins false]

# docsify i <path> [-l false] [-t vue] [--plugins false]

```

* start serve

```
docsify generate <path> [--sidebar _sidebar.md]

# docsify g <path> [-s _sidebar.md]

```

* docsify generate

```
docsify generate <path> [--sidebar _sidebar.md]

# docsify g <path> [-s _sidebar.md]

```

* docsify-pdf-converter

```
npm install --save-dev docsify-pdf-converter

```

* .docsifytopdfrc.js

```
module.exports = {
  contents: [ "docs/_sidebar.md" ], // array of "table of contents" files path
  pathToPublic: "pdf/readme.pdf", // path where pdf will stored
  pdfOptions: "<options for puppeteer.pdf()>", // reference: https://github.com/GoogleChrome/puppeteer/blob/master/docs/api.md#pagepdfoptions
  removeTemp: true, // remove generated .md and .html or not
  emulateMedia: "screen", // mediaType, emulating by puppeteer for rendering pdf, 'print' by default (reference: https://github.com/GoogleChrome/puppeteer/blob/master/docs/api.md#pageemulatemediamediatype)
}
```

* Add script into package.json

```
{
  "scripts": {
    "convert": "node_modules/.bin/docsify-pdf-converter"
  }
}
```

* convert

```
npm run convert
```

## deploy docs on nginx

```
# nginx.conf
server {
  listen 80;
  server_name  your.domain.com;

  location / {
    alias /path/to/dir/of/docs/;
    index index.html;
  }
}
```

