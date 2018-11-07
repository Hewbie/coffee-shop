# Making CoffeeShop

### First: Generate a Rails project and set it up for git and GitHub

```bash
rails new coffee_shop
cd coffee_shop
subl .
git init
git add .
git commit -m "first commit"
git remote add origin <url>
git push origin master
```

### Second: Add Welcome page

```bash
rails g controller Welcome index
```

In config/routes.rb alter index route to

`root 'welcome#index'`

In app/views/welcome/index.html.erb replace existing code

```html
<h1>Welcome</h1>
<p>Lorem Ipsum</p>
```

Save to git and GitHub in terminal

```bash
git add .
git commit -m "added landing page"
git push origin master
```

### Third: Add Drinks

```bash
rails g scaffold Drink name:string size:integer price:decimal
rails db:migrate
rails s
```

(In class, our database messed up because we had a property called 'type' which is reserved. We had to go back to the master in git to fix it.)

In browser go to http://0.0.0.0:3000/drinks to add several drinks to the database.

Close server by ctrl+C in terminal
Save to git and GitHub in terminal

```bash
git add .
git commit -m "added drinks scaffold"
git push origin master
```