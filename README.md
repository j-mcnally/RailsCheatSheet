RailsCheatSheet
===============

Wiki for ruby / rails for beginners.


Basics
------

Variables: A code identifier that encapsulates some item of data.

`variable = 3`

this sets a variable named variable equal to 3. From this point forward in you method variable is the same thing as 3.

`1 + variable` would be equal to 4.

variables should be 





Strings: Any word letters etc, that are not code. These are essentially described in two ways with double quotes, and single quotes.

Double quotes are the best bet here. Following is an example of setting a variable to a string.



Hashes:


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

Similarally if your table was named `elephants` your model would be named `Elephant` and you would query a record with

`Elephant.find(1)` if you want the record with an ID of 1.

If you wanted say the record with the ID of 22 you could say.

`Elephant.find(22)`


Creating a new record can be done 2 ways. If we use our example from step 1 of tweets we can use the same model
to create new records.

We can say

`t = Tweet.new`

`t.body = 'Some new tweet'`

`t.save`

or we can say

`t = Tweet.create({body: 'some new tweet'})`

the important difference is in the first example we are only creating the tweet in memory first, 
it is not written to the database
until after we call save method.

With the create function in the second example the object is created and immediatly saved to the database.

