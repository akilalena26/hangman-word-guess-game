# hangman-word-guess-game
print("Welcome to Hangman! You have 6 guesses to guess the word. Be careful, don't loose the lives! ;p")
print('''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
''')
import random

stages = ['''
  +---+
  |   |
  O   |
 /|\  |
 / \  |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
 /    |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|\  |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
 /|   |
      |
      |
=========''', '''
  +---+
  |   |
  O   |
  |   |
      |
      |
=========
''', '''
  +---+
  |   |
  O   |
      |
      |
      |
=========
''', '''
  +---+
  |   |
      |
      |
      |
      |
=========
''']

end_of_game = False
word_list = ["ardvark", "baboon", "camel"]
w = random.choice(word_list)
l = len(w)
lives = 6
# print(f'Pssst, the solution is {w}.') //To use the word to analyse the process.
display = []
for _ in range(l):
    display += "_"
print(display)
while not end_of_game:
    guess = input("Guess a letter: ").lower()

    for i in range(l):
        letter = w[i]
        if letter == guess:
            display[i] = letter
    if guess not in w:
        lives -= 1
        if lives == 0:
            end_of_game = True
            print("Ohohhhh.....You lost, try again...don't .")
    print(f"{' '.join(display)}")

    if "_" not in display:
        end_of_game = True
        print("Woah!...You win, you have a great thinking...good job.")
    print(stages[lives])
