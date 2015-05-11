##week9-Ruby on Rails part 4
####上課日期:4/23

##Devise
devise是一套使用者認證(Authentication)套件，是Rails社群中最廣為使用的一套。
####[Devise教學](../rails/user.md)

##view helper
>用來協助html開發

####[ihower-Action View - Helpers 方法](https://ihower.tw/rails4/actionview-helpers.html)

##Active Record 驗證
>在將資料存入資料庫前，驗證資料是否正確。

####[RailsGuide-Active Record 驗證](http://rails.ruby.tw/active_record_validations.html)
####[ihower-ActiveRecord - 資料驗證及回呼](https://ihower.tw/rails4/activerecord-lifecycle.html)

##Active Record回呼
>如何在Active Record的生命週期中回應特定事件。

####[RailsGuide-Active Record 回呼](http://rails.ruby.tw/active_record_callbacks.html)
####[ihower-ActiveRecord - 資料驗證及回呼](https://ihower.tw/rails4/activerecord-lifecycle.html)

##Ajax
>AJAX指的是一套綜合了多項技術的瀏覽器端網頁開發技術，AJAX應用可以僅向伺服器傳送並取回必須的資料，並在客戶端採用JavaScript處理來自伺服器的回應。因為在伺服器和瀏覽器之間交換的資料大量減少，伺服器回應更快了。很多的處理工作可以在發出請求的客戶端機器上完成，因此Web伺服器的負荷也減少了。(摘錄自維基百科)

####[RailsGuide-在 Rails 使用 JavaScript](http://rails.ruby.tw/working_with_javascript_in_rails.html)
####[ihower-Ajax 應用程式](https://ihower.tw/rails4/ajax.html)

##分頁
[kaminari](https://github.com/amatsuda/kaminari)

###Install
在`Gemfile`加入下面的程式碼
```
gem 'kaminari'
```

###Controller
```
@users = User.order(:name).page(params[:page]).per(10)
```

###View
```
<%= paginate @users %>
```


##期中考教室
4/30(四) 禮拜二的同學在商院101,禮拜三的同學在商院102

