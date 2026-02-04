# PHP_Laravel10_Bagisto

## Description:

PHP_Laravel10_Bagisto is an e-commerce web application built using Bagisto, which is based on Laravel 10.
This project allows users to browse products, add items to cart, and place orders, while administrators can manage products, categories, customers, and orders from the admin panel.

## Project Objective

The main objective of this project is to:

Learn Laravel 10 framework

Understand Bagisto eCommerce architecture

Implement a ready-made eCommerce system

Practice admin & frontend flow

Use MySQL database with Laravel


## User Roles
###  Customer (Frontend User)

View products

View product details

Add products to cart

Checkout and place orders

### Admin (Backend User)

Login to admin panel

Manage products

Manage categories

Manage customers

Manage orders

Configure store settings


## Requirements

- PHP >= 8.1
- Composer
- MySQL
- XAMPP / WAMP / Laragon
- Node.js (optional, for frontend assets)



---



# Project SetUp

---



## STEP 1: Create New Bagisto (Laravel 10) Project


### Run Command :

```
composer create-project bagisto/bagisto PHP_Laravel10_Bagisto

```

### Go inside project:

```
cd PHP_Laravel10_Bagisto

```

This command installs Bagisto with Laravel 10 automatically.





## STEP 2: Create Database (VERY IMPORTANT)

### Open browser → go to:

```
http://localhost/phpmyadmin

```

1. Click New

2. Database name (TYPE EXACT):

```
bagisto_laravel10

```
3. Click Create


 Database must exist before install



## STEP 3: Open .env file (CRITICAL)

### Open file:

```
D:\xampp\htdocs\PHP_Laravel10_Bagisto\.env

```

### Set EXACTLY like this:

```
DB_CONNECTION=mysql
DB_HOST=127.0.0.1
DB_PORT=3306
DB_DATABASE=bagisto_laravel10
DB_USERNAME=root
DB_PASSWORD=

```
DB_PASSWORD must be EMPTY (no space, no quotes)


## Step 4: NOW run installer (this WILL work)

### Run:

```
php artisan bagisto:install

```

You will see install questions


## STEP 5: Bagisto Installer – Step by Step (TYPE THIS)

### You are seeing:

```
Please enter the application name: [Bagisto]

```

### Step 5.1: Application Name

#### Just press ENTER

```
Bagisto

```

### Step 5.2: Application URL

#### You will see:

```
Please enter the application URL: [http://localhost]

```
#### Type:

```
http://127.0.0.1:8000

```

Press ENTER



### Step 5.3: Database Connection

#### You will see:

```
 Please select the database connection: [mysql]

```
#### Type:

```
mysql

```

Press ENTER



### Step 5.4: Database Host

#### You will see:

```
 Please enter the database host: [127.0.0.1]

```
#### Type:

```
127.0.0.1

```

Press ENTER





### Step 5.5: Database Port

#### You will see:

```
Please enter the database port: [3306]

```
#### Type:

```
3306

```

Press ENTER



### Step 5.6: Database Name

#### You will see:

```
Please enter the database name: [bagisto_laravel10]

```
#### Type:

```
bagisto_laravel10

```

Press ENTER




### Step 5.7: Database Prefix

#### You will see:

```
Please enter the database prefix:

```
#### Type:

```
(empty)

```

Press ENTER



### Step 5.8: Database Username

#### You will see:

```
Please enter your database username: [root]

```
#### Type:

```
root

```

Press ENTER




### Step 5.9: Database Password

#### You will see:

```
Please enter your database password:

```
#### Type:

```
(empty)

```

Press ENTER


### After follow this step you see Create admin credentials...


### Step 5.10: Admin User Name

#### You will see:

```
Enter the name of the admin user: [Example]

```
#### Type:

```
(UserName) Demo

```

Press ENTER   




### Step 5.11: Admin Email Address

#### You will see:

```
Enter the email address of the admin user: [admin@example.com]

```
#### Type:

```
User@gmail.com  (demo123@gmail.com)

```

Press ENTER 



### Step 5.12: Admin Password

#### You will see:

```
Configure the password for the admin user: [admin123]

```
#### Type:

```
Example: admin123


```

Press ENTER 





### Step 5.13: Sample Products Setup

#### You will see:

```
Please select if you want some sample products after installation. [false]
  true ............................................................................................................. 0
  false ............................................................................................................ 1

```
#### Type:

```
true  -> 0

```

Press ENTER 




### After You see:

```
Would you like to star our repo on GitHub? (yes/no) [no]:
>

```

#### What to type

Just press ENTER
(or type no and press ENTER)

```
no

```

### After this

#### Bagisto will:

- Finish installation

- Show success message

#### You should see something like:

```
Bagisto installed successfully!

```



## STEP 6: Start the project

### Run:

```
php artisan serve

```

### Open in Browser

#### Frontend (Store)

```
http://127.0.0.1:8000

```

#### Admin Panel

```
http://127.0.0.1:8000/admin

```

#### Admin Login

```
Email: User@gmail.com
Password: admin123



```

## So you can see this type Output:

### Admin Login Page:


<img width="1919" height="958" alt="Screenshot 2026-02-04 122542" src="https://github.com/user-attachments/assets/01161619-3289-4518-8f9f-e3c8540ebbd1" />


### Admin login page contains:


<img width="1919" height="965" alt="Screenshot 2026-02-04 122750" src="https://github.com/user-attachments/assets/e7100e11-a120-49bd-82b0-16320321c641" />



<img width="1912" height="944" alt="Screenshot 2026-02-04 122806" src="https://github.com/user-attachments/assets/aae5984f-56a1-49dd-80a0-f88ccd122236" />



<img width="1918" height="965" alt="Screenshot 2026-02-04 123013" src="https://github.com/user-attachments/assets/1b6e8e95-0da8-4dff-aa51-992372f71bce" />



<img width="1919" height="958" alt="Screenshot 2026-02-04 123032" src="https://github.com/user-attachments/assets/fcc3a2c5-c610-4745-9f00-ac58643c9e78" />


---



# Project Folder Structure:

```
PHP_Laravel10_Bagisto/
│
├── app/
│   ├── Console/
│   ├── Exceptions/
│   ├── Http/
│   │   ├── Controllers/
│   │   └── Middleware/
│   ├── Models/
│   └── Providers/
│
├── bootstrap/
│   └── app.php
│
├── config/
│   ├── app.php
│   ├── database.php
│   ├── bagisto.php
│   └── cache.php
│
├── database/
│   ├── migrations/
│   ├── seeders/
│   └── factories/
│
├── packages/
│   └── Webkul/
│       ├── Admin/
│       ├── Catalog/
│       ├── Customer/
│       ├── Sales/
│       └── Checkout/
│
├── public/
│   ├── index.php
│   ├── storage/
│   └── themes/
│
├── resources/
│   ├── views/
│   ├── lang/
│   ├── css/
│   └── js/
│
├── routes/
│   ├── web.php
│   └── api.php
│
├── storage/
│   ├── app/
│   ├── framework/
│   └── logs/
│
├── vendor/
│
├── .env
├── artisan
├── composer.json
└── README.md

```
