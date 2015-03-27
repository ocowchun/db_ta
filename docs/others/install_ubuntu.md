如果安裝VM有問題的同學,可以試著用我包裝的這個ubuntu,目前我只有先做64bit的版本。

####1. 使用ftp下載 `db ta.ova`

####2. 然後打開VirtualBox選擇`匯入應用裝置`
[圖示](https://www.evernote.com/shard/s145/sh/05871dea-fd64-4d90-91d0-3eaeb049ec17/f89c2f9d9bea80c660ca0c27116f66c8)

####3. 對VM按右鍵選`設定值`然後取消USB2.0
[圖示](https://www.evernote.com/shard/s145/sh/fe8930ba-f1dc-4117-b26c-9149a540af9f/261eaf9061c1016d59b188f0558ada10)

####4. 執行ubuntu

####5. 在ubuntu打開terminal,先執行下面兩行指令
```
$ /bin/bash --login
$ rvm use 2.1.5
```

接著就可以開始開發rails了
