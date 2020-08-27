# Project "Shopee"

## Summary
Create a web based application that can be used in any shop to create orders and keep track of products. The application needs to be made using a multi-tier approach i.e. the frontend needs to be built on a Javascript framework and the backend is APIs only. 

The features are needed

* Manage adding/updating users (you can use CMS/framework features for this if available)
* Manage adding/updating product categories (you can use CMS/framework features for this if available)
* Manage products
* These products can be used to create a basic order/bill for customers. We want to have a form, list, and detail view for orders for this.
* Also a screen may be needed for settings / configuration form

## Technologies / Languages / Frameworks you must use
* Backend / APIs must be implemented using any PHP based framework / CMS of your choice (Eg: Laravel / CodeIgniter / Joomla / Wordpress or similar ones)
* For database you can use (Eg: MySql or Postgres)
* Frontend / UI (views) must be implemented using any JAVASCRIPT based framework of your choice (Eg: Angular / React / Vue.js or similar ones)
* You must make use of any CSS / UI framework of your choice and avoid writing your own CSS (Eg: Bootstrap / Semantic UI or similar ones)


## Project Configuration
Need a way to set up the below configurations
* Shop GST Number
* Shop Address
* Tax percentage


## Workflows in the system

### Add Product 
* Fields - Product name, description, photo, category, price per item, stock level
* Add, edit, delete product should be possible
* Client side validation is added for required fields

### Products List
* List should show the products added
* List should have filter for category and a filter to hide/show out of stock products

### Add Order
* Fields - customer name, mobile number
* Choose one or more products and quantity for each
* Changing quantity should update the amount
* Stock should be checked when a quantity is entered. It should not be possible to create an order with quanity more than stock
* Show total at the bottom

### Orders List
* List should show customer name, number, count of order products, total amount, date
* Order number should link to order details view

### Order details
* Should look like an invoice
* Show the GST number and shop address
* Show all the customer details
* Show all the products, qty and price

## Report expected

Product wise sales report having the below columns
* Product Name
* No. of items sold 
* Total Sales Amount
* Current stock

All report columns should be sortable

## Acceptance Criteria - Database:
* All DB tables, columns should have meaningful names
* All DB tables should have enough indexes

## Acceptance Criteria - Menu / Sidebar Links
* Links shall be provided to access all UI screens
* Either show menu at top or show as sidebar on UI
* Menu / Sidebar should highlight current UI screen name

## Acceptance Criteria - Security 
* Use best practices to ensure XSS, CSRF, SQL injection etc are taken care of
