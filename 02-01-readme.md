Objective

    Create a class from components using the type() function.

Importance to project

    Completing this activity will help you understand how the components that make up a class fit together. Next, we’ll look at how those elements can be manipulated.

Workflow

    1. Create your own version of the Price class, similar to this:

    class Price:
        def __init__(self, part_number, price):
            self.price = price
            self.part_number = part_number

        def get_price(self):
            return  self.price

    Create an instance of the class and test it to make sure that the price is set and the get_price() method works.

    2. Create two functions, function__init__ and function_get_price, that take the same parameters as the methods in the Price class.

    3. Create a dictionary namespace with two keys, "__init__" and "get_price", with the values being the names (just the names—no parameters, no parenthesis, no quotes) of the functions you just created (function__init__ and function_get_price).

    4. Create a class with type().

      Price2 = type('Price2', (), namespace)

        - The first parameter is the class name, which should (but doesn’t have to) match the name on the left side of the =.

        - The second parameter, (), is the list of superclasses, which is empty in this case.

        - The last parameter is the namespace dictionary we created above.

    5. Test to see if there are any differences between the first class you defined and the one created using type().

