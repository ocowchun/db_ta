#Development Tools

##[gulp](http://gulpjs.com/)
>Automate and enhance your workflow
協助前端開發的工具,例如live reload,compile sass...etc

###安裝gulp
```bash
$ npm install gulp -g
```

##[bower](http://bower.io/)
>A package manager for the web
用來管理前端package的工具

###安裝bower
```bash
$ npm install bower -g
```

###常用指令
```bash
#建立bower.json,記錄你安裝的package
$ bower init

#在你的資料夾安裝jquery
$ bower install jquery 

#在你的資料夾安裝jquery,將相關資訊記錄到bower.json
$ bower install jquery --save

#搜尋包含`jquery`這個關鍵字的packages
$ bower search jquery

#移除jquery
$ bower uninstall jquery
```

<iframe width="640" height="480" src="https://www.youtube.com/embed/-XYdwttET4w" frameborder="0" allowfullscreen></iframe>

##建立一個簡單的網頁專案
###1. create project and install package 
```sh
$ mkdir project-name
$ cd project-name
$ npm init
$ npm install gulp --save-dev
$ npm install browser-sync --save-dev
```

###2. 在專案資料夾加入`gulpfile.js`
```js
'use strict';
var gulp = require('gulp');
var browserSync = require('browser-sync');
 
gulp.task('browser-sync', function() {
    browserSync({
        server: {
            routes: {
                '/bower_components': 'bower_components'
            }
        }
    });
});

// Reload all Browsers
gulp.task('bs-reload', function() {
    browserSync.reload();
});


gulp.task('default', ['browser-sync'], function() {
    gulp.watch('*', ['bs-reload']);
    // body...
});
```

###3. 在專案資料夾加入`index.html`
```html
<!DOCTYPE html>
<html lang="en">
<head>
	<meta charset="UTF-8">
	<title>Hello HTML</title>
</head>
<body>
Hello HTML
</body>
</html>
```

###4. 執行`gulp`
```bash
$ gulp
```

####大功告成,你完成了你的第一個html!!