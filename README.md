# py
import random
n = random.randint(0, 50)
nguesses = 5
while (True):
  print("Guess the number between 0 to 50")
  num = int(input())
  if (num > n):
    nguesses = nguesses - 1
    if (nguesses == 0):
      print("No. of guesses left:", nguesses)
      print("GAME OVER")
      break
    else:
      print("Hint: Choose smaller number")     
      print("No. of guesses left:", nguesses)
      continue
  elif (num < n):
    nguesses = nguesses - 1
    if (nguesses == 0):
      print("No. of guesses left:", nguesses)
      print("GAME OVER")
      break
    else:
      print("Hint: Choose greater number")     
      print("No. of guesses left:", nguesses)
      continue
  elif (num == n):
    nguesses = 5 - (nguesses - 1)
    print("Congratulations! You have guessed in", nguesses, "attempts")
    break
