#Markdown
>Markdown的目標是實現「易讀易寫」。

在網路上，很流行使用Markdown來編寫文件，因為可以用非常簡單的語法完成基本的文件編輯。
這個教學文件就是使用Markdown完成的

##常用語法
###標題
在行首插入1到6個`#`,會把該行文字變為標題(字體大小與插入的`#`數成反比)
例如:
```md
#Hello World
##大家好
###今天天氣真好
```

#Hello World
##大家好
###今天天氣真好

###區塊引言
在引言的第一行行首加上`>`
```md
>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
```

>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,

###清單
Markdown支援有序清單和無序清單。

無序清單使用星號、加號或是減號作為清單標記：
```md
*   Red
*   Green
*   Blue
```
會產生
*   Red
*   Green
*   Blue

有序清單則使用數字接著一個英文句點：
```md
1.  Bird
2.  McHale
3.  Parish
```

1.  Bird
2.  McHale
3.  Parish


###分隔線

```md
大俠愛吃漢堡包
---
你不是大俠，你吃香蕉
```

大俠愛吃漢堡包
---
你不是大俠，你吃香蕉

###連結
```md
[facebook](www.facebook.com)
```
[facebook](www.facebook.com)


###圖片
```md
![Alt text](/path/to/img.jpg)
```
![Alt text](/path/to/img.jpg)

##GFM
>GitHub uses "GitHub Flavored Markdown," or GFM, across the site--in issues, comments, and pull requests. It differs from standard Markdown (SM) in a few significant ways, and adds some additional functionality.

###Syntax highlighting

Code blocks can be taken a step further by adding syntax highlighting. In your fenced block, add an optional language identifier and we'll run it through syntax highlighting. For example, to syntax highlight Ruby code:

```ruby
require 'redcarpet'
markdown = Redcarpet.new("Hello World!")
puts markdown.to_html
```

###reference
[Markdown文件](http://markdown.tw/)
[GitHub Flavored Markdown](https://help.github.com/articles/github-flavored-markdown/)
[five-minutes-to-markdown-mastery](http://www.remarq.io/articles/five-minutes-to-markdown-mastery/)