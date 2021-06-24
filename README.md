# FIU CEN4010 group project - Bookstore API

This API will be used as part of the backend for a bookstore website.

# Setup environment

    pip3 install pipenv # Only the first time
    pipenv install --dev # Only the first time
    pipenv shell

# How to clear the database

    remove the db.sqlite file
    python3 -c 'from BookstoreAPI import db; db.create_all()'

# Launch server

    python3 BookstoreAPI.py

# Sending POST and GET requests

    Use the script [APIcalls.py](https://github.com/lustered/BookstoreAPI/blob/master/utils/APIcalls.py) in [utils/](utils)

## Objectives

| Feature ID |          Feature           | Benefit                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | Implemented |
| :--------: | :------------------------: | :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | :---------: |
|     1      | Book Browsing and Sorting  | Users will have a simple and enjoyable way to discover new books and Authors and sort results. <br/><br/> [API Actions] <br/> - Retrieve List of Books by Genre <br/> - Retrieve List of Top Sellers (Top 10 books that have sold the most copied) <br/> - Retrieve List of Books for a particular rating and higher <br/> - Retrieve List of X Books at a time where X is an integer                                                                                       |     ❌      |
|     2      |       Profile Manage       | Users can create and maintain their profiles rather than enter in their information each time they order <br/><br/> [API Actions] <br/> - Create a User with username(email), password and optional fields (name, email address, home address) <br/> - Retrieve a User Object and its fields by their username <br/> - Update the user and any of their fields except for mail <br/> - Create Credit Card that belongs to a User and Retrieve a list of cards for that user |     ❌      |
|     3      |       Shopping Cart        | Users can manage items in a shopping cart for immediate or future Purchase <br/><br/> [API Actions] <br/> - Create a shopping cart instance for a user. Shopping cart must belong to a user. <br/> - Update the shopping cart with a book. <br/> - Retrieve the list of book(s) in the shopping cart. <br/> - Delete a book from the shopping cart instance for that user                                                                                                   |     ❌      |
|     4      |        Book Details        | Users can see informative and enticing details about a book <br/><br/> [API Actions] <br/> - An administrator must be able to create a book with the book ISBN, book name, book description, price, author, genre, publisher , year published and copies sold. <br/> - Must be able retrieve a book’s details by the ISBN <br/> - An administrator must be able to create an author with first name, last name, biography and publisher                                     |     ❌      |
|     5      | Book Rating and Commenting | Users can rate AND comment on books they’ve purchased to help others in their selection <br/><br/> [API Actions] <br/> - Must be able to create a rating for a book by a user on a 5 star scale with a datestamp <br/> - Must be able to create a comment for a book by a user with a datestamp <br/> - Must be able to retrieve a list of ratings and comments sorted by highest rating <br/> - Must be able to retrieve the average rating for a book                     |     ❌      |
|     6      |    Wish List Management    | Users can create and have 3 different wish lists which can have books moved to from the primary list. <br/><br/> [API Actions] <br/> - Must be able to create a wishlist of books that belongs to user and has a unique name <br/> - Must be able to add a book to a user’s wishlisht <br/> - Must be able to remove a book from a user’s wishlist into the user’s shopping cart <br/> - Must be able to list the book’s in a user’s wishlist                               |     ❌      |
