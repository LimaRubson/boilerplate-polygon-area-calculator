# Polygon Area Calculator

This is the boilerplate for the Polygon Area Calculator project. Instructions for building your project can be found at https://www.freecodecamp.org/learn/scientific-computing-with-python/scientific-computing-with-python-projects/polygon-area-calculator

# My collaboration in the project:

# Shape Calculator

This Python program includes two classes: `Rectangle` and `Square`, both designed to represent geometric shapes and perform various calculations.

## Rectangle Class

The `Rectangle` class is initialized with width and height attributes. It provides the following methods:

- **`set_width(self, width):`**: Updates the width of the rectangle.
  
- **`set_height(self, height):`**: Updates the height of the rectangle.

- **`get_area(self):`**: Returns the area of the rectangle (width * height).

- **`get_perimeter(self):`**: Returns the perimeter of the rectangle (2 * width + 2 * height).

- **`get_diagonal(self):`**: Returns the diagonal of the rectangle ((width ** 2 + height ** 2) ** 0.5).

- **`get_picture(self):`**: Returns a string representing the shape using lines of "*". If the width or height is larger than 50, it returns "Too big for picture."

- **`get_amount_inside(self, shape):`**: Takes another shape (square or rectangle) as an argument. Returns the number of times the passed-in shape could fit inside the rectangle.

- **`__str__(self):`**: String representation of the rectangle, e.g., "Rectangle(width=5, height=10)".

## Square Class

The `Square` class is a subclass of `Rectangle`. It is initialized with a single side length, and it inherits methods from the `Rectangle` class. Additionally, it provides:

- **`set_side(self, side):`**: Updates the side length of the square.

- **`__str__(self):`**: String representation of the square, e.g., "Square(side=9)".

## Example Usage

```python
from shape_calculator import Rectangle, Square

rect = Rectangle(10, 5)
print(rect.get_area())
rect.set_height(3)
print(rect.get_perimeter())
print(rect)
print(rect.get_picture())

sq = Square(9)
print(sq.get_area())
sq.set_side(4)
print(sq.get_diagonal())
print(sq)
print(sq.get_picture())

rect.set_height(8)
rect.set_width(16)
print(rect.get_amount_inside(sq))
