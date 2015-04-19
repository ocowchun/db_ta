#使用devise實作會員功能
>devise是一套使用者認證(Authentication)套件，是Rails社群中最廣為使用的一套。

##安裝

###1. 加入下列程式碼到`Gemfile`

```
gem 'devise'
```
###2. 在專案目錄下執行bundle，安裝deivse
```
$ bundle
```

###3. 在專案目錄下執行devise generator，產生devise的設定檔
```
$ rails generate devise:install
```

###4. 建立你的會員model
通常會使用`User`，不過也可以根據你的需求調整。
```
$ rails generate devise User
$ rake db:migrate
```

###5. 設定url，主要是作為寄送驗證信用。如果你的會員功能不需要寄送驗證信，這個步驟可以省略。
```
config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }
```

###6. 產生會員基本的html樣板(註冊,登入,忘記密碼...)
```
$ rails generate devise:views
```

###7. 加入登入連結
通常我會在在`application.html.erb`加入登入連結的html
```
<% if user_signed_in? %>
<%=current_user.name%>你好
<%= link_to "登出", destroy_user_session_path,method:'delete' %>
<% else %>
<%= link_to "註冊", new_user_registration_path %>
<%= link_to "登入", new_user_session_path %>
<% end %>
```

##加上自訂欄位
如果你需要的欄位在預設的user model裡面不存在的話，可以透過migration加入，例如我們幫user model加入name這個欄位。
###1. 建立migration
```
$ rails g migration add_name_to_users 
```
###2. 新增你需要的欄位
在`migration`中加入
```ruby
add_column :users, :username, :string
```
###3. 執行`rake db:migrate`

###4. Strong Parameters
因為Rails4有`Strong Parameters`的關係，當model要取用表單資料的時候需要經過一些處理，在這邊我們使用filter的方式，允許model讀取額外的表單參數。
```rb
class ApplicationController < ActionController::Base
  before_action :configure_permitted_parameters, if: :devise_controller?

  protected

  def configure_permitted_parameters
    devise_parameter_sanitizer.for(:sign_up) << :name
  end
end
```

##reference
####[devise](https://github.com/plataformatec/devise)
####[ihower-使用者認證](https://ihower.tw/rails4/auth.html)
