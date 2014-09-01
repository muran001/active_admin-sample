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


4. Add Custom Pages

See. https://github.com/activeadmin/activeadmin/blob/master/docs/10-custom-pages.md 





