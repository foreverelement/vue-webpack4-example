# vue webpack4 example

This is example of Vue project with webpack4 

## Usage

start use webpack4 by clone this repertory.

## Migrate

### my webpack3 project

```bash
vue-init webpack vue-project
cd vue-project
npm install
```

### migrate to webpack4

`npm-check-updates` can automatically upgrade to the latest version without `^` rule.

```bash
npm install -g npm-check-updates
ncu -u
npm install extract-text-webpack-plugin@4.0.0-beta.0
npm install --force
```

## Performance

### webpack 3, split

```
Hash: 4cdb19b01343f490b110
Version: webpack 3.11.0
Time: 5680ms
                                                  Asset       Size  Chunks             Chunk Names
                  static/js/app.22682dd45c784aee5b30.js    11.5 kB       0  [emitted]  app
               static/js/vendor.e5e7ecee6f957e2703de.js    62.2 kB       1  [emitted]  vendor
             static/js/manifest.2ae2e69a05c33dfc65f8.js  857 bytes       2  [emitted]  manifest
    static/css/app.30790115300ab27614ce176899523b62.css  432 bytes       0  [emitted]  app
static/css/app.30790115300ab27614ce176899523b62.css.map  828 bytes          [emitted]
              static/js/app.22682dd45c784aee5b30.js.map    21.4 kB       0  [emitted]  app
           static/js/vendor.e5e7ecee6f957e2703de.js.map     324 kB       1  [emitted]  vendor
         static/js/manifest.2ae2e69a05c33dfc65f8.js.map    4.97 kB       2  [emitted]  manifest
                                             index.html  502 bytes          [emitted]

  Build complete.
```

### webpack 4, without split

```
Hash: 21e1e548df22fab35345
Version: webpack 4.1.1
Time: 3226ms
                                                  Asset       Size  Chunks             Chunk Names
                  static/js/app.0aaa39d04aa9d2dcf1b4.js   72.2 KiB       0  [emitted]  app
    static/css/app.30790115300ab27614ce176899523b62.css  432 bytes       0  [emitted]  app
static/css/app.30790115300ab27614ce176899523b62.css.map  828 bytes          [emitted]
              static/js/app.0aaa39d04aa9d2dcf1b4.js.map    338 KiB       0  [emitted]  app
                                             index.html  332 bytes          [emitted]
Entrypoint app = static/js/app.0aaa39d04aa9d2dcf1b4.js static/css/app.30790115300ab27614ce176899523b62.css static/js/app.0aaa39d04aa9d2dcf1b4.js.map
```
