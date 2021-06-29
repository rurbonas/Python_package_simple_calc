# Building Python Packages
## What is Python Package and benefits
### Structure 

- step 1 ` create an app folder `
- step 2 inside app folder `__init__.py` empty - to initialise our package
- step 3 inside app folder `fizzbuzz.py` add our functionality 
- step 4 `program.py` on dir level - to use as our run file
- `setup.py` on a dir level - to describe our module details such as version, author and contact details


```
building_python_packages
-- app
--- __init__.py
--- fizzbuzz.py
program.py
setup.py
``` 

- Let's build our package starting with `setup.py`
```python
from setuptools import setup

# Information about the package
setup(name="app")

# Optional
version = "1.0"
description = "Python app"
author = "Ron"
author_email = "abc@abc.com"
url = "https//www.spartaglobal.com"
```
- code for `simple_calc.py`
```python
# Create a class called Calculator
class Calculator:

    # add
    def Add(self, num1, num2):
        return num1 + num2

    # subtract
    def Subtract(self, num1, num2):
        return num1 - num2

    # multiply
    def Multiply(self, num1, num2):
        return num1 * num2

    # divide
    def Divide(self, num1, num2):
        return num1 / num2


```
- code for `program.py`
```python
from app.simple_calc import Calculator

calc = Calculator()

print(calc.Add(5, 3))
print(calc.Add(2, 4))
print(calc.Subtract(2, 4))
print(calc.Multiply(2, 4))
```

- ` pip install .` to install our package using `pip` package manager
