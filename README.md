# PHP E-commerce Store

A small online store written in plain PHP with MySQL (PDO). Shoppers can browse and search products, add them to a cart, and check out. Admins can add, edit, and delete products, including image uploads.

## Features

- User registration and login, with hashed passwords and `User`/`Admin` roles
- Product search
- Cart tied to a cookie, with quantity updates and checkout
- Admin pages to manage products
- Prepared statements for all database queries
- Shared components (navbar, footer, product card, alerts) included across pages

## Structure

```
index.php, search_products.php, shopping_cart.php, checkout.php
admin.php, add_product.php, edit.php, delete.php     Admin product management
components/       Shared layout pieces and the DB connection (connect.php)
users/            Login, register, logout
css/, images/     Styles and site images
uploaded_files/   Product images uploaded through the admin page
```

## Running it

Needs PHP 7+ and MySQL, e.g. XAMPP or MAMP.

1. Put the project in your web root.
2. Create a MySQL database named `ecommerceupdated`. Connection settings are in `components/connect.php`.
3. Create the tables the app uses:
   - `users`: `username`, `email`, `pass`, `userRole`
   - `products`: `id`, `name`, `price`, `image`, `description`, `category`
   - `cart`: `id`, `user_id`, `product_id`, `price`, `qty`
4. Open `index.php` in the browser.
