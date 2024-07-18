TO CREATE A HANGMAN GAME THROUGH PYTHON CODING.
1. Start:
   - Import libraries
   - Display welcome message and initial hangman stage
   - Define hangman stages
   - Choose a random word (w) from word_list
   - Set lives to 6
   - Display game logo and initial underscores

2. Game Loop:
   - While end_of_game is False:
       - Prompt user for a guess
       - Clear screen
       - If guess already made, notify user
       - If correct guess, update display
       - If incorrect guess, decrement lives and notify user
       - If lives == 0, end game with loss message
       - If no underscores left, end game with win message
       - Print current display and hangman stage
