RailsCheatSheet
===============

Wiki for ruby / rails for beginners.



Models
------

A model is the primary object used to read and store values to a database.

A model is basically a table in the database abstracted as an application class. This abstraction is done via an ORM (Object Relation Mapper).

A basic model will have an attribute/property with every column/field from your database table.

Given the following table

    |-------------------------------------------------|
    |                    tweets                       |
    |-------------------------------------------------|
    | ID  |                    Body                   |
    |-------------------------------------------------|
    | 1   |            MY AWSOME TWEET                |
    |-------------------------------------------------|



We would have a model named Tweet with two attributes.

id and body

Notice how the name of the model is the singular/capitalized form of the table name tweets. This would make our model's name Tweet.

If we want to find the tweet with an ID of 1. We could use this model to query our table by simplying calling

`Tweet.find(1)`

this find method will work with any model. And the default find field will always be id.


