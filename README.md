# ghost-jsdelivr

A simple helper to serve ghost theme CDN content that would be served trough jsdelivr GPDR compatible with your own "public" directory in `content/public/`.

## Install

### 1. Download and build this package in `content/public/`

```bash
pushd content/public/
git clone https://github.com/jochumdev/ghost-jsdelivr.git cdn
cd cdn
npm install && npm run build
popd
```

With [ncu](https://www.npmjs.com/package/npm-check-updates) installed:

```bash
pushd content/public/
git clone https://github.com/jochumdev/ghost-jsdelivr.git cdn
cd cdn
ncu -u && npm install && npm run build
popd
```


### 2. Adjust your config.production.json

```json
{
  "sodoSearch": {
    "url": "/public/cdn/sodo-search/umd/sodo-search.min.js",
    "styles": "/public/cdn/sodo-search/umd/main.css"
  },
  "portal": {
    "url": "/public/cdn/portal/umd/portal.min.js"
  },
  "comments": {
    "url": "/public/cdn/comments-ui/umd/comments-ui.min.js",
    "styles": false
  }
}
```

### 3. Restart ghost

Done :)

## License

MIT
