# KLocalStorage

enhanced localStorage(加强版 localStorage)

# INSTALL(安装)

```bash
npm install KLocalStorage
```

# USAGE(使用)

For Vue Project in main.js add

```js
import 'KLocalStorage'
```

create a `storage.config.js`

```js
module.exports = {
	storagePrefix: '',
	localStorageWhiteList: [],
}
```

`storagePrefix`: addPrefix (在普通 key 上添加前缀)
`localStorageWhiteList`: localStorage.clean() will skip array (使用 localStorage.clean()时会跳过里面的值)

then you can use it as native localStorage

```js
localStorage.a = '1'
localStorage.setItem('a', '2')
localStorage.a
localStorage.getItem('a')
localStorage.removeItem('a')
localStorage.clean() // only clean add storagePrefix and skip localStorageWhiteList (只会清除添加了storagePrefix值的前缀,会跳过localStorageWhiteList白名单里的值)
```
