##week7-Ruby and OOP
####上課日期:4/9
##Active Record 遷移
如何新增欄位,刪除欄位,變更欄位

##route
[Rails 路由：深入淺出](http://rails.ruby.tw/routing.html)
資源式路由
單數資源
命名空間與路由
新增更多資源式路由

##params
http://rails.ruby.tw/action_controller_overview.html#%E5%8F%83%E6%95%B8

##controller
####render text
使用不同的檔案格式回應(html,json,text..etc)

####before_action
http://rails.ruby.tw/action_controller_overview.html#%E6%BF%BE%E5%8B%95%E5%99%A8
透過`before_action`,來減少重複的程式碼

####application_controller,concern
將多個controller都會用到的funtion move到controller,或是concern
如果全部controller或幾乎全部都會用到=> application_controller
少數幾個controller會用到=>concern

##view helper
用來協助html開發

###bulitin helper
* form_for
* form_tag
* link_to

####custom helper
覺得內建的不夠,那你也可以自己針對需求客製化專門的helper function

##active record callback
####before_save
####before_create
####after_update


##validation

##協助開發用app
```ruby
  gem 'pry-rails'
  gem 'better_errors'
  gem 'binding_of_caller'
  gem 'quiet_assets'
```

##作業
todo app

##devise(考慮中)

####how to create user model
####how to add facebook login

