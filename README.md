# Nerdle

This project is the game of nerdle, which is essentially wordle but with math.


## Requirements

* python3


## Installation

Download as a zip file or clone from github
* git clone **_https://github.com/WTCSC/nerdle-DexterityB.git_**

(_Unzip if neccessary_) and open **nerdle-DexterityB** in the terminal
* cd **nerdle-DexterityB**

Run **nerdle.py**, using python3, in the terminal
* python3 **nerdle.py**


## Examples

Basic usage:

```python

def generate_numbers_for_multiplication():
    # The first number has to be single digits and not zero or one in order to create an 8 character equation
    # The second number must be two digits and not ten or eleven as those can't create a three character result
    num1 = random.randint(2, 9)
    num2 = random.randint(12, 99)
    result = num1 * num2
    return num1, num2, result
    # 
```


Advanced usage:

```python
def generate_numbers_for_addition():
     # The initial numbers can't be triple digits as that wouldn't let the equation be 8 characters
    num1 = random.randint(1, 99)
    num2 = 1000
    if num1 < 10:
        num2 = random.randint(num1 + 90, 99)
    elif 9 < num1 < 90:
        num2 = random.randint(10, 99 - num1)
    elif num1 > 90:
        num2 = random.randint(100-num1, 9)
    result = num1 + num2
    return num1, num2, result
```


Intended flow of the program:
1. The program shows you an example of what nerdle looks like and explains the rules
2. The program asks for a nerdle guess
3. The program returns the answer with green, yellow, and grey boxes if the guess is valid, if not, it asks for an actual guess
4. The program repeates steps 3 and 4 until the player has guess the equation or lost
5. The program ask if you want to play again, in which case it repeats from step 2


## Testing

* Just run the code using python3, and go through the program to make sure it works properly, meaning:
 * The nerdle game plays out properly
 * The program asks for equations, with error handling
 * There aren't any errors
 * It ask if you want to play again
* Don't push if there are errors


## License

This project is not licensed


[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/Tm7PdKHd)
[![Open in Codespaces](https://classroom.github.com/assets/launch-codespace-2972f46106e565e64193e422d61a12cf1da4916b45550586e14ef0a7c637dd04.svg)](https://classroom.github.com/open-in-codespaces?assignment_repo_id=20879479)
<!-- 
   Assignment Notes:
   - To run the game, execute `python3 nerdle.py` in the terminal.
   - Your task is to implement the equation generation functions in `equation_generator.py` and the solution validator in `game_engine.py`.
   - Don't forget to import your modules.
   - PAY ATTENTION TO THE TODO COMMENTS IN THE CODE.
   - Each function has comments detailing its purpose and requirements.
   - Code is automatically tested *every time* you push changes to GitHub.
-->
