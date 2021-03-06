source 'https://rubygems.org'
git_source(:github) do |repo_name|
  repo_name = "#{repo_name}/#{repo_name}" unless repo_name.include?("/")
  "https://github.com/#{repo_name}.git"
end

install_if -> { RbConfig::CONFIG['target_os'] =~ /(?i-mx:bsd|dragonfly)/ } do
  gem 'rb-kqueue', ">= 0.2", platforms: :ruby
end


if ENV['CUSTOM_RUBY_VERSION']
  ruby ENV['CUSTOM_RUBY_VERSION'] # i.e.: '2.3'
end

gem 'rails', '~> 5.1.0'

# Use SCSS for stylesheets
gem 'sass-rails'
# Use Uglifier as compressor for JavaScript assets
gem 'uglifier'
# Use CoffeeScript for .coffee assets and views
gem 'coffee-rails'

gem 'mysql2', group: :mysql
gem 'pg', group: :postgresql
gem 'sqlite3', group: :sqlite3

# Use Puma as the app server
gem 'puma'

# Capistrano for deployment
group :capistrano do
  gem 'capistrano', '3.8.2', require: false
  gem 'capistrano-rails',   require: false
  gem 'capistrano-bundler', require: false
  gem 'capistrano-rvm',     require: false
  gem 'capistrano3-puma',   require: false
end

# Use jquery as the JavaScript library
gem 'jquery-rails'
gem 'jquery-migrate-rails'
gem 'jquery-ui-rails'

# Build JSON APIs with ease. Read more: https://github.com/rails/jbuilder
gem 'jbuilder'

gem 'activemodel-serializers-xml'
gem 'activeresource', github: 'rails/activeresource', branch: 'master'
gem 'acts_as_commentable'
gem 'bcrypt'
gem 'cocoon'
gem 'devise'
gem 'dotenv-rails'
gem 'github-markdown'
gem 'haml'
gem 'localized_language_select', github: 'frab/localized_language_select', branch: 'master'
gem 'nokogiri'
gem 'paperclip'
gem 'paper_trail'
gem 'prawn', '< 1.0'
gem 'prawn_rails'
gem 'pundit', github: 'elabs/pundit', branch: 'master'
gem 'ransack'
gem 'redcarpet'
gem 'ri_cal'
gem 'roust'
gem 'rqrcode'
gem 'simple_form'
gem 'sucker_punch'
gem 'transitions', require: ['transitions', 'active_record/transitions']
gem 'will_paginate'
gem 'yard'

group :production do
  gem 'exception_notification'
end

group :development, :test do
  gem 'listen'
  gem 'bullet'
  gem 'pry-rails'
  gem 'pry-byebug'
  gem 'letter_opener'
  gem 'faker'
end

group :test do
  gem 'database_cleaner'
  gem 'factory_girl_rails', '~> 4.0'
  gem 'shoulda'
  gem 'rails-controller-testing'
  gem 'minitest-rails-capybara'
  gem 'poltergeist'
end

group :doc do
  # gem 'rails-erd'      # graph
  # gem 'ruby-graphviz', require: 'graphviz' # Optional: only required for graphing
end
