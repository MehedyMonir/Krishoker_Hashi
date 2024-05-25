# Krishoker Hashi

Welcome to Krishoker Hashi, a comprehensive platform designed for farmers to purchase their daily farming commodities as well as food items. Our website is built with a focus on simplicity and ease of use, ensuring that farmers can find and order what they need without hassle.

## Features

- **User Authentication**: Secure login, logout, and signup systems.
- **Shopping Cart**: A convenient cart to manage orders and goods.
- **Remove Item from Order**: Ability to remove unwanted items from the order list.
- **Confirm Order**: Option to confirm the order and update the status to 'confirmed'.

## Built With

- PHP
- HTML
- Bootstrap
- MySQL

## Getting Started

To get a local copy up and running, follow these simple steps.

### Prerequisites

- Download and install [XAMPP](https://www.apachefriends.org/index.html).

### Installation

1. **Start XAMPP** and ensure that MySQL is running. If MySQL can't find the port, copy the backup folder of MySQL and rename it to `data`.
2. **Create a database** named `userdb` which will contain 3 tables: `users`, `ProductList`, and `Orders`.

   Use the following SQL command to create the database and the tables:

````markdown
```sql

CREATE DATABASE userdb;
USE userdb;
CREATE TABLE `users` (
    `id` INT(11) NOT NULL AUTO_INCREMENT,
    `name` VARCHAR(50) NOT NULL,
    `location` VARCHAR(50) NOT NULL,
    `email` VARCHAR(50) NOT NULL,
    `phone` VARCHAR(15) NOT NULL,
    `password` VARCHAR(255) NOT NULL,
    PRIMARY KEY (`id`)
);
 CREATE TABLE ProductList (
     ProductID INT AUTO_INCREMENT,
     Type VARCHAR(255),
     Name VARCHAR(255),
     Price DECIMAL(10, 2),
     Quantity INT,
     PRIMARY KEY (ProductID)
 );
 CREATE TABLE Orders (
     id INT AUTO_INCREMENT,
     phone VARCHAR(255),
     Pname VARCHAR(255),
     Ptype VARCHAR(255),
     Pprice DECIMAL(10, 2),
     status VARCHAR(50) DEFAULT 'not confirmed',
     insert_time TIMESTAMP DEFAULT CURRENT_TIMESTAMP,
     PRIMARY KEY (id)
 );
    ALTER TABLE Orders
    ADD COLUMN status VARCHAR(50) DEFAULT 'not confirmed' AFTER Pprice;
```
````

3. **Copy the repository** to the `xampp/htdocs` folder.
4. **Launch the application** by navigating to `localhost/[repository_name]` in your web browser.

### Note

A product list in the form of SQL is included in the repo to kickstart the project. Simply run the SQL in the productlist_SQL.txt in the `productlist` table to populate it with data.

## Contributing

Contributions are what make the open-source community such an amazing place to learn, inspire, and create. Any contributions you make are **greatly appreciated**.


