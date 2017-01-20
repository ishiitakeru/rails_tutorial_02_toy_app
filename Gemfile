source 'https://rubygems.org'

#railsチュートリアルに書いてある内容をそのままコピペするとローカルのrails serverコマンドが動かなくなる
#ディフォルトのままだとherokuでデプロイ出来ない
#基本的にはディフォルトにしておいて、一部変える

git_source(:github) do |repo_name|
  repo_name = "#{repo_name}/#{repo_name}" unless repo_name.include?("/")
  "https://github.com/#{repo_name}.git"
end


gem 'rails',        '~> 5.0.1'
gem 'puma',         '~> 3.0'
gem 'sass-rails',   '~> 5.0'
gem 'uglifier',     '>= 1.3.0'
gem 'coffee-rails', '~> 4.2'
gem 'jquery-rails'
gem 'turbolinks',   '~> 5'
gem 'jbuilder',     '~> 2.5'

group :development, :test do
  #SQLiteはherokuで利用できないのでテスト環境限定の指定に入れる
  gem 'sqlite3'
  gem 'byebug', platform: :mri
end

group :development do
  gem 'web-console',           '3.1.1'
  gem 'listen',                '3.0.8'
  gem 'spring',                '1.7.2'
  gem 'spring-watcher-listen', '2.0.0'
end

#heroku環境は本番扱いなのでここに書く。PostgreSQLを使う指定とする。
group :production do
  gem 'pg', '0.18.4'
end

gem 'tzinfo-data', platforms: [:mingw, :mswin, :x64_mingw, :jruby]
