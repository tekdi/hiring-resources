# Project "Shopee"

## Summary

We want to create a web based application that can be used in any kind of shop by a shopkeeper to keep track of products and orders.

UI-wise we will need

* a form & list view for **adding/updating users (you can use CMS/framework features for this if available)**

* a form & list view for **adding/updating product categories (you can use CMS/framework features for this if available)**

* a form & list view for **adding/updating products**

* These products can be used to **create a basic order/bill** for customers. We want to have a form, list, and detail view for orders for this.

* Also a screen might be needed for **settings / configuration** form

## Technologies / Languages / Frameworks you must use

* **Backend / APIs** **must** be implemented using any **PHP based framework / CMS** of your choice

    * Eg: Laravel / CodeIgniter / Joomla / Wordpress or similar ones

* For **database** you can use

    * Eg: MySql or Postgres

* **Frontend / UI (views)** **must** be implemented using any **JAVASCRIPT based framework** of your choice

    * Eg: Angular / React / Vue.js or similar ones

* You **must** make use of any **CSS / UI framework** of your choice and avoid writing your own CSS

    * Eg: Bootstrap / Semantic UI or similar ones

## UI Screens / Views needed

<table>
  <tr>
    <td> **Entity** ➡️
</td>
    <td>Configuration
</td>
    <td>User </td>
    <td>Category</td>
    <td>Product</td>
    <td>Order</td>
  </tr>
  <tr>
    <td>**View Type** ⬇️</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
  </tr>
  <tr>
    <td>form</td>
    <td>configform</td>
    <td>userform</td>
    <td>categoryform</td>
    <td>productform</td>
    <td>orderform</td>
  </tr>
  <tr>
    <td>list</td>
    <td>-</td>
    <td>users</td>
    <td>categories</td>
    <td>products </td>
    <td>orders</td>
  </tr>
  <tr>
    <td>details</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>-</td>
    <td>order</td>
  </tr>
</table>


Additionally provide UI screen for reports expected.

## Project Configuration

Add config options for

* **shop_gst_number** [text field]

    * *(note: use this on order details view)*

* **shop_address** [textarea field]

    * *(note: use this on order details view)*



## Workflows in the system

1. **Add Product (view: productform)**

    * **Ability to add these fields**

        1. Product name

        2. Product description 

        3. Category

        4. Price per item

        5. Available stock *[note: products table should stock field, you should update that upon each order placed]*

    2. Add, edit, delete product should be possible

    3. Client side validation is added for required fields

    4. Required fields can not be submitted as blank or only whitespaces (space, tabs)

    5. Files uploaded are stored at

        6. /images/products

2. **Products List (view: products)**

    1. List should** show all fields from product-form**

    2. List should have **filter for category**

3. **Add Order Form (view: orderform)**

    1. Ability to add customer name, mobile number, note

    2. Ability to add product in order

        1. Product

        2. Quantity

        3. Show price based on quantity of product

    3. One or more products can be added **_(use repeatable group of fields)_**

    4. Changing quantity in the repeatable group of fields should update the amount accordingly

        1. Create and use Javascript functions for same

    5. On change of quantity, **check if stock is available**

        1. For that make an **AJAX** call

        2. Add validation to only allow if stock is available

    6. Show **total** at the bottom

        1. Create and use Javascript functions for same

4. **Orders List (view: orders)**

    1. List should show customer name, number, count of order products, total amount, date

    2. Order number should link to order details view

5. **Order details (view: order)**

    1. Output should look like actual **invoice**

    2. Should show **shop details (get from component configuration)**

    3. Should show **shop GST details (get from component configuration)**

    4. Should show order ID, date

    5. Should show customer name, mobile

    6. Should show product, quantity, price **(Show data of repeated order items on this view)**

    7. Should show **total** amount

## Reports expected

* Product wise sales report having the below columns

    1. Product Name, No. of items sold, Total Sales Amount, Current stock

    2. All report columns should be sortable

## Common Acceptance Criteria:

### Acceptance Criteria - Database:

* All DB tables, columns should have meaningful names

* All DB tables should have enough indexes

### Acceptance Criteria - Menu / Sidebar Links:

* Links shall be provided to access all UI screens

* Either show menu at top or show as sidebar on UI

* Menu / Sidebar should highlight current UI screen name

### Acceptance Criteria - Security 

* Make sure to use the CSRF token facility offered by the framework / CMS you use.

* Make sure application is not vulnerable to XSS

