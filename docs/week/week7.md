#week7-Ruby on Rails part 2
####上課日期:4/9
>本週一樣是學習Ruby on Rails,會解決controller如何回應不同的請求,與使用Filter來處理重複的程式碼,如何使用view helper來設計頁面,還有談到ActiveRecord的資料驗證。

##controller
####render text
使用不同的檔案格式回應(html,json,text..etc)

####before_action
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
  gem 'sqlite3'
  gem "awesome_print", require:"ap"
  gem 'meta_request'
  gem 'brakeman', :require => false
  gem 'immigrant'
  gem 'pry-rails'
  gem 'better_errors'
  gem 'binding_of_caller'
  gem 'rubocop', require: false
  gem 'quiet_assets'
  gem "teaspoon"
```

##devise(考慮中)

####how to create user model
####how to add facebook login
