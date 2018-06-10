# Fn.js

## Usage
### > Import as a single file
1.Download the file  
2.Create a script tag and insert it in the HTML file,just like:
```html
<script src="fn.js">
<!-- or umd-->
<script src="fn.umd.js">
```

### > Import as a es6/node module
1.Get it by npm/cnpm
```shell
npm install webfn
```
2.import it in the file
```javascript
const fn = require('fn')
//or
import fn from 'fn.cjs.js'
```

## Sample
The default namespace is "fn",you can use the function as this example
```javascript
var ua = fn.ua()
//return an object whihc contains some user agent info
{
    isPC:false,         
    isMobile:true,      
    platform:'iphone',  //pc | iphone | ipad ..
    browser:'wx',       //browser name
    version:6           //browser version
}
```

When you use it as a single file,if the "fn" is existed,or you just wanna change another name,you can do like this:
```javascript
var ___ = fn.conflict()
__.ua()
```

## Reference

+ **ua()**   
    return a ojbect which contains the user agent info,and add some classes to html element  

+ **response([opts])**  
    define the response rules for window size,add some classes to the html element by the custom option

+ **resetREM([designSize])**   
    rewrite the REM base size(modify the html font-size) refer to the design size

+ **param(key)**   
    get the value of the specified key in the url

+ **randomColor()**   
    return a random color string by hexadecimal code,just like"#00CCFF"

+ **preLoadImage(srcArr,[cb])**   
    load some images and exec a callback function

+ **typeOf(o)**   
    judge the type of the target,return a string,just like "string"
