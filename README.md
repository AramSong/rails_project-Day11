config/environments/development.rb



**config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }** 추가

=> 이메일 가입시 확인 메일을 보내준다.



```ruby
                  Prefix Verb   URI Pattern                    Controller#Action
        new_user_session GET    /users/sign_in(.:format)       devise/sessions#new
            user_session POST   /users/sign_in(.:format)       devise/sessions#create
    destroy_user_session DELETE /users/sign_out(.:format)      devise/sessions#destroy
       new_user_password GET    /users/password/new(.:format)  devise/passwords#new
      edit_user_password GET    /users/password/edit(.:format) devise/passwords#edit
           user_password PATCH  /users/password(.:format)      devise/passwords#update
                         PUT    /users/password(.:format)      devise/passwords#update
                         POST   /users/password(.:format)      devise/passwords#create
cancel_user_registration GET    /users/cancel(.:format)        devise/registrations#cancel
   new_user_registration GET    /users/sign_up(.:format)       devise/registrations#new
  edit_user_registration GET    /users/edit(.:format)          devise/registrations#edit
       user_registration PATCH  /users(.:format)               devise/registrations#update
                         PUT    /users(.:format)               devise/registrations#update
                         DELETE /users(.:format)               devise/registrations#destroy
                         POST   /users(.:format)               devise/registrations#create
                    root GET    /                              home#index
```

`new.html.erb`

```
form_for(resource,...)=> resource에는 User.new
```

`controller_name`=>  params[:controller_name]

```
<% %> : Executes the ruby code within the brackets.
```

```
<%= %> : Prints something into erb file.
```

```
<% -%> : Avoids line break after expression.(줄바꿈)
```

```
<%# %> : Comments out code within brackets; not sent to client (as opposed to HTML comments).
```

```ruby
rails g devise:controllers
```

우리가 만들어 놓은 내용에 대해서 컨트롤러 명을 정확하게 명시해줘야 한다.

```ruby
Running via Spring preloader in process 2434

Usage:

  rails generate devise:controllers SCOPE [options]

```

=>rails g devise:controllers users 라고 쳐야함

`omniauth_callbacks_cotroller.rb`: github, 페이스북 등등 다른 이메일 사용시 필요한 정보들을 실제 모델에 저장

