#imports
import random

#constants
#This is my version of Jumper/hangman 
= (
    """
 ------
|     |
|
|
|
|
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|
|
|
|
|
----------
"""
   ,
"""
 ------
|     |
|     0
|     +
|
|
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|    -+
|
|
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|    -+-
|
|
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|   /-+-
|
|
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|   /-+-/
|
|
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|   /-+-/
|     |
|
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|   /-+-/
|     |
|     |
|
|
----------
"""
    ,
"""
 ------
|     |
|     0
|   /-+-/
|     |
|     |
|    |
|    |
----------
"""
    ,
"""
 ------
|     |
|     0
|   /-+-/
|     |
|     |
|    | |
|    | |
----------
"""
)

#This is a list of the words that could be used
WORDS = ("sincere", "silver", "gospel", "sleepy", "delicious")
#Initialize variables
#This randomly chooses a word from the list
word = random.choice(WORDS)  #the word to be guessed
so_far = "-" * len(word)  #one dash for each letter in word to be guessed

wrong = 0  #number of wrong guesses player has already made
used = []  #letters already guessed
print("Welcome to Hangman. Good Luck!")
#so, the program will continue while there are still guesses left and the player
#didn't guess the word
while wrong < MAX_WRONG and so_far != word:
    print(HANGMAN[wrong])
    print("\nYou've used the following letters:\n", used)
    print("\nSo far, the word is:\n", so_far)

    guess = input("\n\nEnter your guess: ")
    #This will convert the guess to all uppercase becasue that's how it it is in the
    #tuple
    guess = guess.upper()

    #So if they guess the saame letter twice, this will print
    while guess in used:
        print("You've already guessed the letter", guess)
        guess = input("Enter your guess: ")
        guess = guess.upper()
    #So, whatever's guessed, gets added to the used list 
    used.append(guess)
    #So, if the guess is correct, it will print the following
    if guess in word:
        print("\nYes!", guess, "is in the word!")
        #create new so_far to include guess
        #This means it will replace the blank with the letter
        new = ""
        for i in range(len(word)):
            if guess == word[i]:
                new += guess
            else:
                new += so_far[i]
        #This redefines so_far to include the letter guessed correctly
        so_far = new
    #So if the guess is wrong, then it will print the following
    else:
        print("\nSorry,", guess, "isn't in the word.")
        #This adds a wrong try
        wrong += 1
#So if the number of tries reaches the limit, meaning the hangman is hanged, it
#prints the following
if wrong == MAX_WRONG:
    print(HANGMAN[wrong])
    print("\nYou've been hanged!")
#This says that if it doesnt reach the limit, it will print the following
#becasue it means that the person got the word right.
else:
    print("You've guessed it!")
print("\nThe word was", word)
input("\n\nPress the enter key to exit.")
