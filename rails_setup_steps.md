```
$ rails new app_name -d postgresql -T
```

sets up to use postgresql database and without Test Unit


<i>Gemfile</i>
```
group :test do
  gem 'rspec-rails'
  gem 'capybara'
end
```

```
$ rails generate rspec:install
```

<i>spec/rails_helper.rb</i>
```
require 'capybara/rails'
```

```
$mkdir spec/features/
```

```
$ touch spec/features/things_feature_spec.rb
```

<i>things_feature_spec.rb</i>
```
require 'rails_helper'

feature 'restaurants' do
  context 'no restaurants have been added' do
    scenario 'should display a prompt to add a restaurant' do
      visit '/restaurants'
      expect(page).to have_content 'No restaurants yet'
      expect(page).to have_link 'Add a restaurant'
    end
  end
end
```

<i>config/routes.rb</i>
```
resources :things
```

```
$ rake routes
```

```
$ rspec
```


```
$ rails g controller things
```
