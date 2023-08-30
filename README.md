# The best Python Styleguide out there 🔥
###### /s
### By Gtruaan

Hello! Welcome to the compilation of syntax rules and good practices that I invented out of boredome. I'll try to update this once in a while, adding new rules.

## Rule 0: Strings go with `"`

Single character strings or strings inside a formatting block (`{}`) can use single quotes.

Example:
```python
print("Hello World!", f"Our names are {', '}.join(names)");
```

## Rule 1: Every line must end in a Semi-Colon

No exceptions... (except imports).

Example:
```python
OutHandler.LogError("Limit exceded");
UserInteraction.Prompt("Continue?");
```

## Rule 2: `this` instead of `self`

Looks prettier I guess.

Example:
```python
def __init__(this, name: str):
    this._name: str = name;
```

## Rule 3: Variables and arguments/returns must be type-hinted when first defined

Not being strongly typed is Python's worst offense.

Example:
```python
class Funcs:
  @staticmethod
  def Greet(name: str) -> None:
      print("Hello", name);
  
currentName: str = "John";
currentName = "Gus";
names: List[str] = [currentName];
```

> Note: Use `typing` module.

## Rule 4: Variable naming conventions

Variables, classes and methods always follow these rules:
- **Variables**: lowerCamelCase
- **"Private" Variables**: _sameWithUnderscore
- **Classes**: UpperCamelCase
- **Methods**: UpperCamelCase

## Rule 5: Order of imports

1. First go the external imports (e.g. `random`, `selenium`, `math`, etc.).
2. A space.
3. Then go the user-defined modules.
4. A space.
5. Finally, the `typing` imports

Example:
```python
import random
from pygame.locals import quit

from source.utils import UserDefinedClass

from typing import List, Any
```

## Rule 6: Everything must be wrapped inside a class

Even functions. Just slap them in a class and put on that juicy `@staticmethod`.
There can't be any code outside a class. Only exception is:
```python
if __name__ == "__main__":
    Program.Main();
```

Example:
```python
from random import randint


class Program:
    @staticmethod
    def Sum(a: int, b: int) -> int:
        return a + b;

    @staticmethod
    def Main() -> None:
        a: int = 3;
        b: int = randint(1, 3);

        print(Program.Sum(a, b));


if __name__ == "__main__":
    Program.Main();
```

## Rule 7:

To be continued...

