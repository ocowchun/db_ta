#[Github Pages](https://pages.github.com/)
>在github上建立你的個人網站

##usage

###1. 在github上新增repository,repo名稱為`your-name.github.io`的repo(`your-name`是你的github帳號)

###2. clone repo到你的電腦上
```bash
$ git clone https://github.com/your-name/your-name.github.io
```
####注意`your-name`要換成你的github帳號

###3. 建立一個`index.html`在該repo的根目錄,內容如下:

```html
<!DOCTYPE html>
<html>
<body>
<h1>Hello World</h1>
<p>I'm hosted with GitHub Pages.</p>
</body>
</html>
```

###4. commit&sync

```bash
$ git add --all
$ git commit -m "Initial commit"
$ git push -u origin master
```

###5. 前往 `http://your-name.github.io.`瀏覽你的新網站!
####注意`your-name`要換成你的github帳號
