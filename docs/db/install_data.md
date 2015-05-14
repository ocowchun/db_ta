#輸入資料至MySQL
>示範如何安裝專案資料到MySQL

##1. 請先安裝好MySQL
在mac安裝MySQL可以參考[ihower-進階開發環境安裝](https://ihower.tw/rails4/advanced-installation.html#mac-os-x)

在ubuntu安裝MySQL可以看下列影片
<iframe width="640" height="480" src="https://www.youtube.com/embed/y2cGcyNhWVY" frameborder="0" allowfullscreen></iframe>

##2. 建立新的資料庫用戶

>通常我們不會直接使用root來操作資料庫,我們會建立新的使用者來操作。

```bash
#以root身份,登入MySQL
$ mysql -u root -p 
#輸入密碼後會進入MySQL command line

#建立新帳號
GRANT ALL ON *.* TO 'username'@'localhost' IDENTIFIED BY 'passowrd';

#離開MySQL command line
quit

#以username身份,登入MySQL
$ mysql -u username -p 
#輸入密碼後會進入MySQL command line

#建立database
create database your-database-name;
```
##3. 建立好資料庫後,打開對應的資料庫資料夾 

####ubuntu user
```bash
sudo apt-get install libgnome2-bin.
$ sudo su
$ cd /var/lib/mysql/your-database-name
$ gnome-open .
```

###mac user
```bash
$ cd /usr/local/var/mysql/your-database-name
$ open .
```

##4. 把檔案解壓縮放進該資料夾

這樣就完成了。

##5. 驗證是否成功輸入資料

```bash
$ mysql -u username -p 
use your-database-name;
show tables;
#如果有看到資料表就表示安裝成功
```

##補充說明
其實像這樣子備份MySQL的資料其實不太好,比較好的做法是使用mysqldump
有興趣的同學可以參考下面的連結
[FUNMING基地--利用MYSQLDUMP備份](https://fmbase.tw/blog/2013/01/23/mysql%E5%88%A9%E7%94%A8mysqldump%E5%82%99%E4%BB%BD/)

##GUI
>除了command line之外,也可以使用GUI的方式來操作MySQL

####for all platforms
[https://www.mysql.com/products/workbench/](https://www.mysql.com/products/workbench/)
####for mac
[http://www.sequelpro.com/](http://www.sequelpro.com/)
