## Final Project: Script 1
### Web-scraping Weather Forecast Information with Python
- A script that scrapes the 5-day weather forecast from the National Weather Service website. The script extracts information from multiple elements listed under the same class name using the BeautifulSoup library. 

- Provide the coorindates of the location you want to check.

- Scapper will provide 5 day weather forecast in uppercase.
## Final Project: Script 2
### HangMan
- A script that play a word guessing game with player.   

- Player has 7 chances to guess the word, one letter each time.  

- With each fail, there will be a reaction from game.  
- 
- Player wins if he/she guess the word correct within 7 tries.  
- 
- Otherwise game will show the correct word then end.

## Final Project: Documentation
### Script1:
From my perspective, script1 is very similar to  lab4 exercise which I need to deal with string objects. The difference here is user has to provide the longitude and latitude as input, then the code concatenates the input with the website URL. The rest of the code is similar to execrise2 of lab4. The script sends a request to the website and scraps 5 days of weather forecast information of the selected location, create a beautiful soup object, and find <lt> label to extract forecast information.
The difficult part of this task is manipulating strings to deliver the result as expected. The difference between lab4 and this assignment is I can’t see the original string which is provided directly in lab4 in the first place. I have to use print to see the string stored in the list and then decide to do the manipulation. After several tries with .replace()  and comparison, script1 finally shows the weather report as expected.

### Script2:
After 2 months of the python learning phase, I decide to build something fun with python.
First, I want to build a little game by utilizing what I learn but don’t have any idea what to build. I google python small projects and try to see if something comes up. I did search for a while although there are so many open-source projects. Finally, I find an interesting game that can also use what I learned. 
This is a game called Hangman. It’s a word-guessing game in which the player has 7 chances to guess a word. In this script, I store a large word list in words.py and then import it to the main python file. 
In the main python file the game process is:
- Create two functions: get_valid_word() and hangman()
- get_vaild_word() produces a random word from words and store it for comparison later.
- hangman() uses set() to distinguish all unique letters in the word and used the letter in the player input.
- Create a while loop to execute the game.
- Compare player input letter with the unique letter in the set(). 
- if the letter in the set() returns the current word with the letter already been guessed else minus one chance.
- Break the while loop if the player exhausts 7 chances(hangman) or completes the word.  
- Delivery of the result.

### Problems:
- The first problem is I don’t know how to import the word list from another python file on Colab which works fine on local IDLE. Solved by solution on StackOverflow: https://stackoverflow.com/questions/48905127/importing-py-files-in-google-colab
- The second problem is finding a data structure to store the hangman process.  Python Dictionary is a perfect data structure since I want to access the different steps relates to the corresponding lives.  
- The third problem I encountered is when I tried to write code more pythonic.  I want to reduce the lines of code, thus, I use list comprehension to create word_list:
***word_list = [letter if letter in used_letters else '-' for letter in word]***
I did not understand how this work at first, so I spent some time practicing with the list comprehension and finally getting this work.

- The last problem is the design of game logic in the while loop, I use several if, elif, else statements to implement game logic, it takes some time to figure out the right flow. I solve this problem by writing pseudocode first and then implement the design with real python code.



