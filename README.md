== README

1. Installation

You can get Rails 4 and 4.1 support by tracking master.
And you need to install devise.

```
gem 'activeadmin', github: 'activeadmin'
gem 'devise'
```

2. Setting up

After installing the gem, you need to run the generator.

```
# create AdminUser class
$ rails g active_admin:install

# creates existing User model in devise
$ rails g active_admin:install User
```

Now, migrate your database and start the server.

```
$ rake db:migrate
$ rails s
```

3. Visit URL

Visit http://localhost:3000/admin and log in as the default user.

* User: admin@example.com
* Password: password


4. Working with Resources

* create a model for a active_admin resource

You have to create models in order to manage at active_admin.

```
$ rails g model Genre name:string
$ rails g model Author first_name:string last_name:string
$ rails g model Book name:string price:decimal author:references genre:references
$ rake db:migrate
```

and also, you can define association between models such as has_many.

* create a resource

Now, you can create a resource.

```
$ rails g active_admin:resource Genre
$ rails g active_admin:resource Author
$ rails g active_admin:resource Book
```

5. Change the columns that are displayed

You can change the columns at Active Admin screen.

```
# app/admin/book.rb
index do
  column :name
  column :author
  column :genre
  column :price
  actions
end
```

Active Admin will detect the belongs_to relationship.
And the 'actions' method adds the "View", "Edit" and "Destroy" links.


6. Add filter to search

A filter is useful insearching through records.

```
filter :name
filter :author, as: :check_boxes
filter :genre, as: :check_boxes
filter :price
```















4. Add Custom Pages

See. https://github.com/activeadmin/activeadmin/blob/master/docs/10-custom-pages.md 





