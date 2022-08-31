# Jungle

A mini e-commerce application built with Rails 6.1 for purposes of teaching Rails by example.


Bugs fixed : 
- Money Formatting - Fixed errors were currency ($) symbol was not showing up.
- Missing Admin Security - Making sure only the admin had access to admin controls.

UI Updates :
- When the cart is empty, the carts page will display a related message instead of an empty cart and re-direct the user back to the products page
- When Product has 0 quantity, a sold out badge is displayed on the product list page and the add button is disabled
- Added additional information about previous orders for a user to look over what they have ordered in the past.

Features added :
- Admin Dashboard Counts - Provide an inventory and category count for the admin
- About Page - added an about page for the user to learn about the people behind Jungle!
- Admin Categories - added a feature allowing an admin to make new categories
- User Authentication - added a login and register pages, and logout option and created a new database table to handle users.

### Homepage 

!["Homepage"]()


### Product List


!["Product List"]()


### Product View


!["Product View"]()


### Order Confirmation


!["Order Confirmation"]()


### Admin Dashboard


!["Admin Dashboard"]()


## Testing 

The newly implemented features and functions were tested using rspec model testing and cypress E2E feature testing.

## Setup

1. Run `bundle install` to install dependencies
2. Create `config/database.yml` by copying `config/database.example.yml`
3. Create `config/secrets.yml` by copying `config/secrets.example.yml`
4. Run `bin/rails db:reset` to create, load and seed db
5. Create .env file based on .env.example
6. Sign up for a Stripe account
7. Put Stripe (test) keys into appropriate .env vars
8. Run `bin/rails s -b 0.0.0.0` to start the server

## Database

If Rails is complaining about authentication to the database, uncomment the user and password fields from `config/database.yml` in the development and test sections, and replace if necessary the user and password `development` to an existing database user.

## Stripe Testing

Use Credit Card # 4111 1111 1111 1111 for testing success scenarios.

More information in their docs: <https://stripe.com/docs/testing#cards>

## Dependencies

- Rails 6.1 [Rails Guide](http://guides.rubyonrails.org/v6.1/)
- Bootstrap 5
- PostgreSQL 9.x
- Stripe
