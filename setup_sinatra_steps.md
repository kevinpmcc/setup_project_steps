create your project folder
```
$ mkdir project_name
```
navigate into folder
```
$ cd project_name
```

create gemfile
```
$ bundle init
```

<i>Gemfile</i>
```

gem 'rack'
gem 'sinatra'
gem 'thin'
gem 'sinatra-rspec'

group :development, :test do
  gem 'pry'
end

group :test do
  gem 'capybara'
  gem 'rspec'
end
```

```
$ rspec-sinatra init --app ProjectName app.rb
```

```
$ touch .rspec
```

<i>.rspec</i>
```
--color
--require spec_helper
-f d

```

<i>spec/feature_spec</i>
```
require 'capybara/rspec'

feature 'welcome message' do
  scenario 'user visits website and see welcome to Blackjack' do
    visit '/'
    expect(page).to have_content 'Welcome to Blackjack!'
  end
end
```

