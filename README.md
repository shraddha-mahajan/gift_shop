# Online Gift Shop

An Online Gift Shop web application built with PHP, MySQL, HTML, CSS, JavaScript, and Bootstrap**. It allows customers to explore gift categories, view products, create an account, book products, and track booking status. An admin area provides tools to manage products, categories, customers, bookings, and feedback.

## Features

### Customer
- Browse the home page and learn about the shop.
- Register and log in to an account.
- Browse gift categories and products.
- View product details and submit a product booking.
- View personal profile information and edit profile details.
- Check booking status.
- Send feedback.
- Change password and log out.

### Administrator
- Log in to the admin panel.
- Add and view product categories.
- Add, view, and delete products.
- View customer accounts.
- View and manage product bookings, including updating booking status.
- View and manage customer feedback.

## Technology Stack

- Frontend: HTML, CSS, JavaScript, Bootstrap, jQuery
- Backend: PHP
- Database: MySQL
- Local development environment: XAMPP or another PHP/MySQL environment
- Additional UI libraries: DataTables and Bootstrap components

## Project Structure

```text
giftshopphp/
├── admin/                 # Admin pages and product/category image uploads
├── css/                   # Stylesheets
├── myimages/              # Website images
├── myimages2/             # Additional gift/product images
├── index.php              # Website home page
├── about.php              # About page
├── registration.php        # Customer registration
├── login.php               # Customer login
├── logout.php              # Logout
├── userhome.php            # Customer profile/home
├── viewallcategory.php     # Gift categories
├── giftbycategory.php      # Category/product pages
├── booking.php              # Product booking
├── viewmybooking.php       # Customer booking history/status
├── feedback.php             # Customer feedback
├── editprofile.php          # Edit customer profile
├── changepassword.php       # Change password
├── contact.php              # Contact page
├── dbconfigure.php          # Database connection/helpers
└── giftshopphp.sql          # MySQL database schema and sample data
```

Some filenames may vary slightly depending on the version of the project.

## Requirements

Install one of the following local development environments:
- [XAMPP](https://www.apachefriends.org/) (recommended for beginners), or
- PHP with a MySQL/MariaDB server and a web server configured.

You will also need a web browser.

## Installation and Setup

1. Download or clone the repository.

   ```bash
   git clone <YOUR_GITHUB_REPOSITORY_URL>
   ```

2. Copy the project into your web server directory.

   For XAMPP on Windows, copy the `giftshopphp` folder into:

   ```text
   C:\xampp\htdocs\
   ```

3. Start the services.

   Open the XAMPP Control Panel and start **Apache** and **MySQL**.

4. Create/import the database.

   - Open `http://localhost/phpmyadmin/`.
   - Choose **Import**.
   - Select `giftshopphp/giftshopphp.sql` and import it.
   - The SQL script creates and selects the `giftshopphp` database.

5. Configure the database connection.

   Open `dbconfigure.php` and check these settings for your local environment:

   ```php
   $dbserver = "localhost";
   $dbuser = "root";
   $dbpwd = "";
   $dbname = "giftshopphp";
   ```

   Update the username and password if your MySQL setup uses different credentials. Do not publish real database credentials.

6. **Open the application.**

   Visit:

   ```text
   http://localhost/giftshopphp/
   ```

7. Create a customer account** through the registration page to test customer features.

## Database Overview

The supplied SQL file defines these tables:

| Table | Purpose |
|---|---|
| `admin` | Administrator login details |
| `siteuser` | Customer account/profile information |
| `category` | Gift categories and category images |
| `product` | Product details, category, price, and image data |
| `booking` | Customer product booking information and status |
| `feedback` | Feedback submitted by customers |

## How It Works

1. Customers register and log in.
2. Customers browse categories and available products.
3. A customer selects a product and submits a booking with the required details.
4. The booking is stored in the MySQL database.
5. The administrator reviews bookings and updates their status.
6. Customers can view their booking information and current status.

## Screenshots

To make the GitHub repository easier to understand, add screenshots of the home page, category/product listing, registration/login page, booking page, and admin dashboard here.

Example:

```markdown
![Home Page](screenshots/home.png)
![Product Categories](screenshots/categories.png)
![Admin Dashboard](screenshots/admin-dashboard.png)
```

Create a `screenshots/` folder and add your own screenshots before using these image links.

## Security Notes

- This project is intended for learning and demonstration. Review it before deploying it publicly.
- The included SQL file contains a sample administrator account. Do not use sample credentials on a live website; change or remove them before sharing or deploying the project.
- Do not commit real passwords, API keys, private database details, or personal customer data.
- For production use, implement password hashing, prepared SQL statements, input validation, output escaping, CSRF protection, and secure session/cookie settings.
- The project includes a payment-related page, but do not assume that real payment processing is configured or secure without further verification.

## Limitations

- This is a PHP/MySQL learning project and may need code updates for a modern PHP environment.
- Confirm database setup and test all flows locally before deployment.
- Online hosting requires a compatible PHP and MySQL/MariaDB environment.

## Future Improvements

- Use prepared statements throughout the application.
- Hash passwords securely.
- Add search, sorting, and product filters.
- Add product stock/availability management.
- Improve mobile responsiveness and accessibility.
- Add automated tests and a clear order/payment workflow.

## Author

Your Name

Replace this with your name and add your LinkedIn/GitHub profile links if you want them displayed in the repository.

## License

No license is specified yet. Add a `LICENSE` file if you want to define how others may use, modify, and distribute this project.
