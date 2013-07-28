
== The way

update gemfile ,add gem s
===========================

		gem "json2-rails"
		gem "spine-rails"
		gem 'eco'

scaffold
===========================

		rails new spine.rails
		cd spine.rails
		rake db:create
		rails g post title content
		rake db:migrate
		rails g spine:new
		rails g spine:scaffold post title content

modify the json api if rails > 4
============================

		cd app/view/posts/
		vi *.jbuilder
			json.extract! post, :id, :title, :content

add stack controller css 
============================
        vi app/assets/stylesheets/applications.css

	        .stack > *:not(.active) {
			  display: none;
			}

start server
=============================
		rails s
