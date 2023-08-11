# class
#!/usr/bin/python3
"""7-rectangle.py: A module that defines a Rectangle class that inherits from BaseGeometry"""

BaseGeometry = __import__('5-base_geometry').BaseGeometry


class Rectangle(BaseGeometry):
    """Rectangle: A class that represents a rectangle"""

    def __init__(self, width, height):
        """__init__: A method that initializes a Rectangle instance with width and height

        Args:
            width (int): The width of the rectangle
            height (int): The height of the rectangle
        """
        self.integer_validator("width", width) # Validate the width using the inherited method
        self.integer_validator("height", height) # Validate the height using the inherited method
        self.__width = width # Set the width as a private attribute
        self.__height = height # Set the height as a private attribute

    def area(self):
        """area: A method that returns the area of the rectangle"""
        return self.__width * self.__height # Calculate and return the area

    def __str__(self):
        """__str__: A method that returns a string representation of the rectangle"""
        return "[Rectangle] {}/{}".format(self.__width, self.__height) # Format and return the string
