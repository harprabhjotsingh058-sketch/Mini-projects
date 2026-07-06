import random
secret_number = random.randint(1, 100)
print("===================================")
print("      NUMBER GUESSING GAME")
print("===================================")
print("I have selected a number between 1 and 100.")
print("Try to guess it!")
attempts = 0
while True:
    try:
        guess = int(input("\nEnter your guess: "))
        attempts += 1

        if guess < secret_number:
            print(" Too low! Try again.")

        elif guess > secret_number:
            print(" Too high! Try again.")

        else:
            print("\n Congratulations!")
            print(f"You guessed the correct number: {secret_number}")
            print(f"Total attempts: {attempts}")
            break

    except ValueError:
        print(" Please enter a valid integer.")
        
