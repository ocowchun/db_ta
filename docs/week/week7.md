#week7-Ruby on Rails part 2
####上課日期:4/9
>本週一樣是學習Ruby on Rails,會解決controller如何回應不同的請求,與使用Filter來處理重複的程式碼,如何使用view helper來設計頁面,還有談到ActiveRecord的資料驗證。

##route
>路由是用來將request對應到正確的controller與action的設定

[Rails 路由：深入淺出](http://rails.ruby.tw/routing.html)
[ihower-路由(Routing)](https://ihower.tw/rails4/routing.html)


##controller
>controller負責處理請求，包含與Model溝通，做出正確的回應。

###params
[RailsGuide-參數](http://rails.ruby.tw/action_controller_overview.html#%E5%8F%83%E6%95%B8)

###filter
>透過filter,來減少controller中重複的程式碼。

[RailsGuide-濾動器](http://rails.ruby.tw/action_controller_overview.html#%E6%BF%BE%E5%8B%95%E5%99%A8)

##view helper
>用來協助html開發

[ihower-Action View - Helpers 方法](https://ihower.tw/rails4/actionview-helpers.html)

##Active Record回呼
>如何在Active Record的生命週期中回應特定事件。

[RailsGuide-Active Record 回呼](http://rails.ruby.tw/active_record_callbacks.html)
[ihower-ActiveRecord - 資料驗證及回呼](https://ihower.tw/rails4/activerecord-lifecycle.html)


##協助開發用app
```ruby
  gem 'pry-rails'
  gem 'better_errors'
  gem 'binding_of_caller'
  gem 'quiet_assets'
```

##作業
todo app
