# guess-the-number-game
import random

#This module contains the functions which are used for generating random numbers.

#To know more about random you can prefer this link     -- https://docs.python.org/3/library/random.html

#This is when you guess the number
def Human_guess(x):
  random_number = random.randint(1,x)

  #now we need loop and we don't know the exact counting of loops so we will have while loop
  Human_guess = 0
  while Human_guess != random_number:
    Human_guess = int(input(f" Guess a number between 1 & {x}:"))
    if Human_guess  < random_number:
      print("Sorry gussed numbers are too low, Guess again")
    elif Human_guess > random_number:
      print("Sorry gussed numbers are too High, Guess again")
  print(f"Eureka! , You have guessed the right numbers {random_number} ")

Human_guess(5)

#This is when the Device guess the number

def Computer_guess(x):
  low = 0
  high = x
  feedback = " "
  while feedback != "Correct":
     if low != high:
       guess = random.randint(low,high)
     else:
       guess = loe #could also be high
     feedback = input(f"Is your {guess} too High(H) , too Low(L) or Correct").lower()
     if feedback == "h":
      high = guess - 1
     elif feedback == "l":
      low = guess + 1
  print(f"YAYAY! The computer guessed the right number , {guess} , Absolute correctly ! ") 
Computer_guess(5)
