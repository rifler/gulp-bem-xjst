# gulp-bem-xjst

> Compile [bemhtml](http://en.bem.info/technology/bemhtml/v2/reference/) templates into JavaScript


## Install

```sh
$ npm install gulp-bem-xjst
```


## Usage

```js
var gulp = require('gulp');
var bemhtml = require('gulp-bem-xjst').bemhtml;

gulp.task('default', function () {
  return gulp.src('page.bemhtml')
    .pipe(bemhtml())
    .pipe(gulp.dest('dist'));
});
```

```sh
$ node -p "require('./dist/page.bemhtml.js').apply({block: 'page'});"
```


## API

bem-xjst engines accesible via properties `bemhtml` and `bemtree`:
```
var engine = require('gulp-bem-xjst')[engine];
```
### engine([options])

#### options

* *String* **exportName** — Engine handler's variable name. Default — `BEMHTML`.
* *String* **engine** — Engine's name. Default — `BEMHTML`.
* *String* **extension** — extension for file. Default — `.${engine}.js`.
* For the rest options' entries see [bem-xjst docs](https://github.com/bem/bem-xjst/blob/master/docs/en/3-api.md#settings)

### License

[MIT](./LICENSE)
