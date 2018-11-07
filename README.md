# Making CoffeeShop

First: Generate a Rails project and set it up for git and GitHub

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

Second: Add Welcome page

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