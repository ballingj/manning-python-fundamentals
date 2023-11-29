Objective

    Explore classes, instances of classes, and how methods can be added to a class after it has been defined.

Importance to project

    These experiments will help you understand what a bound method is and how it works in Python. You will also learn how to see what is really in a class and an instance of that class. Finally, you’ll learn what monkey patching is.

Workflow

  1. Create your own version of the Price class, similar to this:

    class Price:
        def __init__(self, part_number, price):
            self.price = price
            self.part_number = part_number

        def get_price(self):
            return  self.price

  2. Create an instance of the class called item_price.

  3. Use the dir() function and the .__dict__ attribute to explore both the instance and the class. What would you say is the difference between dir() and .__dict__? Are there any attributes that are part of the class but not the instance? Any that are part of the instance but not the class?

  4. Now we’re going to create two standalone functions that we’ll attach to our class. For this to work, each function needs to get an instance of Price as its first parameter.
      1) Create a function called set_discount(item_price, percent_off) that adds a percent_off attribute to a Price object.
      2) Next, create a get_discount_price(item_price) function that calculates the discount price using the price and the percent_off attributes of the item_price object.

  5. Attach both functions to the class and see if they work as instance methods, as in the following example:

    Price.set_discount = set_discount

    By attaching the functions using the =, we have made them look like part of the class. That means that we can use them as if they were originally part of the class. Try some experiments with instances of the original class. Do they work any differently from the methods defined as part of the class from the beginning? Try some other experiments. If you add the functions to the class after it’s been defined, do they work with instances that were created before the functions were added to the class?

    Adding a method to a class after it’s been created is commonly called monkey patching.

  6. If you add a function to an instance instead of to the class, what happens? Does it work at all? How is its behavior different?

