#Git

##版本控制的原因
在專案的開發過程中，會不停地產生新的程式碼，而產生程式碼的過程很可能會遇到檔案被別人覆蓋，或是不知道誰改了某段程式碼，又或者想要復原回到前幾天的版本，因此我們需要一個版本控制系統來協助我們控制專案的版本，讓我們可以專心於開發程式。

##什麼是Git
Git是一個分布式版本控制／軟體配置管理軟體，原是Linux核心開發者林納斯·托瓦茲（Linus Torvalds）為更好地管理Linux核心開發而設計。具有分散式、效能好、本地存取、無痛分支的特性。

##術語
####檔案庫（Repository）
存儲檔案的新版本還有歷史資料的地方，通常是在伺服器上。
####提交（Commit）
將本地端的修改送回檔案庫。（由版本控制軟體處理「跟上次更動相比，哪個檔案又被更動」的事）
####變更（Change）
對一份文件作的特定更動。
####取出（Check-Out）
從檔案庫取出檔案到本地端（客戶端）
####更新（Update）
將檔案庫的修改送到本地端
####合併（Merge / Integration）
合併各個改變。


##Video
###[GitHub & Git Foundations](git_video.md)
收看由github錄製的教學影片，快速上手git

##基本指令
建立Git Repository
<pre>
$ git init
</pre>

檢視專案目前的狀態
<pre>
$ git status
</pre>

將檔案的變動加到staging area
<pre>
$ git add
</pre>

提交變動
<pre>
$ git commit
</pre>

查看之前的commit
<pre>
$ git log
</pre>

加入遠端repository,(主要的遠端repository會命名為origin)
<pre>
$ git remote add remote_name remote_url
</pre>

將本機的commit提交到遠端加入遠端repository(-u 告訴Git記住這組參數，所以下次你只需要執行git push,Git就知道要怎麼做)
<pre>
$ git push -u origin master
</pre>

將遠端repository的變動加入本機
<pre>
$ git pull origin master
</pre>

檢視自從最後一次commit之後的變動
<pre>
$ git diff HEAD
</pre>

移除staging area的檔案
<pre>
$ git reset file_name
 </pre>

將檔案變回最後一次commit時的狀態
<pre>
$ git checkout -- octocat.txt	
</pre>

當我們在開發新的功能或修改bug的時候，通常我們會建立一個新的分支。完成任務之後，將分支合併回去。
<pre>
$ git branch branch_name
</pre>

切換目前的所在分支
<pre>
$ git checkout branch_name 
</pre>

顯示本地分支
`$ git branch`

刪除檔案
<pre>
$ git rm file_name
</pre>

合併指定分支到目前分支
<pre>
$ git merge branch_name
</pre>

刪除分支
<pre>
$ git branch -d clean_up
</pre>

複製別人的Repository
<pre>
$ git clone remote_repo_url
</pre>

###Git基本操作
####建立Repository
<pre>
$ mkdir my_first_project
$ cd my_first_project
$ git init
</pre>
以上指令會產生一個`my_first_project`的資料夾，並建立Repository。
####提交Commit
<pre>
$ touch README.md
$ git add README.md
$ git status
$ git commit -m "First Commit"
</pre>
以上指令會產生一個`README.md`的檔案，並提交變更。

####檢視檔案差異,提交變更
<pre>
編輯 README 做些變更
$ git status
$ git diff
$ git add .  (一次加入所有變更跟新增檔案，但不包括刪除的檔案!)
$ git status
$ git diff --cached
$ git commit -m “Update README”
</pre>
以上指令會檢視readme檔案的變化，然後提交變更

####將本機Repository加入遠端Repository,並提交變更
<pre>
$ git remote add origin git@github.com:ocowchun/git_test.git
$ git push -u origin master
</pre>

####將遠端Repository的變動加入本機
<pre>
$ git pull origin master
</pre>

####複製別人的Repository
<pre>
$ git clone git@github.com:ocowchun/git_test.git
</pre>


##reference
1. [ihower-版本控制系統](http://ihower.tw/git/vcs.html)
2. [ihower-Git 簡介](http://ihower.tw/git/intro.html)
3. [littlebtc-寫給大家的git教學](http://www.slideshare.net/littlebtc/git-5528339)
4. [gogojimmy-Git 的基本使用](http://gogojimmy.net/2012/01/17/how-to-use-git-1-git-basic/)
5. [wiki-版本控制](http://zh.wikipedia.org/wiki/%E7%89%88%E6%9C%AC%E6%8E%A7%E5%88%B6)
6. [Github Mac](https://mac.github.com/)