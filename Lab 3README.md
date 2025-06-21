# lab3_sympy_Gerbise

This project demonstrates how to perform symbolic computation using the sympy library in Python. It covers expression evaluation, equation creation, simplification, and expansion using algebraic expressions.

Task #1: Import Necessary SymPy Modules

import sympy as sp
from sympy import symbols, sqrt
from IPython.display import display

sp.init_printing()

  Imports sympy for symbolic math operations.
  Uses display() to output nicely formatted mathematical expressions in notebooks.
  init_printing() enables pretty printing (e.g., fractions and square roots shown nicely).

Task #2: Solve the Following Expressions

expression1 = sp.Rational(5, 3) + sp.sqrt(10)/2
display(expression1)

  Creates a symbolic expression that adds the rational number 5/3 √10/2
  sp.Rational(5, 3) ensures exact fractional computation.

expression2 = sp.sqrt(50) * sp.sqrt(sp.Rational(5, 9))
display(expression2)

  Multiplies two square roots: √50 and √5/9
  SymPy simplifies square roots precisely rather than returning decimals.

Task #3: Create Equations Using Symbols

x, y = sp.symbols('x y')
equation1 = sp.Eq(2*x + 3*y, 12)
display(equation1)

  Defines an equation 2x + 3y = 12 using symoblic variables x and y.

x, y = sp.symbols('x y')
equation2 = sp.Eq(x - y, 4)
display(equation2)

Represents the equation x - y = 4

Task #4: Simplification

x = sp.symbols('x')
expression1 = (x**2 + 2*x + 1) / (x + 1)
simplified1 = sp.simplify(expression1)
display(expression1, simplified1)

  Simplifies the rational expression   x^2 + 2x + 1 / x+1
  Recognizes that the numerator is a perfect square and reduces it to a simpler form.

x = sp.symbols('x')
expression2 = (1 - 1 / (1 + 1/x)) / (1 + 1/x)
simplified2 = sp.simplify(expression2)
display(expression2, simplified2)

  Simplifies a more complex rational expression involving fractions within fractions.

Task #5: Expansion

x, y = sp.symbols('x y')
expression2 = (2*x + y)*(x - 2*y)
expanded2 = sp.expand(expression2)
display(expression2, expanded2)

  Multiplies two binomials and expands the result into a simplified polynomial.
