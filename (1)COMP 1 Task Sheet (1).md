
- Task Sheet 1
-
<hr>
#Task 3(a)
**Question**

1. *Which function is responsible for getting the name from the user?*
The function is called `GetPlayerName()`

2. *How will you ensure that the user is asked for the name repeatedly?*
To ensure this I will use  a while loop and an if statement.
User will enter the loop and asked for their name.
Once the user has inputted their name, the if statement validates if the name is left Blank. If so it will repeat until the user inputs something.

3. What additional variable will you need and what will its data type be?
I will need to use an additional variable which is called `checker`. It is used if the user inputs their name it will tell the loop to exit. The data type for this variable will be Boolean.

**Pseudo Code**
```
checker <- False
WHILE condition
	GET PlayerName 
	IF PlayerName = "" THEN
		checker <- True
	ELSE
		PRINT "You must enter something for your name!"
	END IF
```

**Program Code**

```python
checker = False
  while checker == False:
    PlayerName = input('Please enter your name: ')
    if PlayerName == "":
      print("You must enter something for your name!")
    else:
      checker = True 
```
<hr>
#Task 3(b)

**Questions**

1. Which function is responsible for adding scores to the table?
`UpdateRecentScores(RecentScores, Score)`

**Program Code**

```python
def UpdateRecentScores(RecentScores, Score):
  user_input = input("Do you want to ad your score to the high score table? (y or n): ")
  user_input = user_input.lower()
  user_input = user_input[:1]
  if user_input == "y":
    PlayerName = GetPlayerName()
    FoundSpace = False
    Count = 1
    while (not FoundSpace) and (Count <= NO_OF_RECENT_SCORES):
      if RecentScores[Count].Name == '':
        FoundSpace = True
      else:
        Count = Count + 1
      if not FoundSpace:
        for Count in range(1, NO_OF_RECENT_SCORES):
          RecentScores[Count].Name = RecentScores[Count + 1].Name
          RecentScores[Count].Score = RecentScores[Count + 1].Score
          Count = NO_OF_RECENT_SCORES
          RecentScores[Count].Name = PlayerName
          RecentScores[Count].Score = Score
  else:
    pass
```
<hr>
#Task 5

**Questions**

1.What additional module will you need to import into the program?
`from datetime import *`
2. Identify the four functions that will require changes.
`DisplayRecentScores(RecentScores)`
`UpdateRecentScores(RecentScores, Score)`
`PlayGame(Deck, RecentScores)`
`ResetRecentScores(RecentScores)`
3. How do you convert a string in the format DD/MM/YY (e.g. 14/08/93) to a date type in Python?
```python
dob= datetime.strptime(date_of_birth,"%d/%m/%Y")
```
<hr>

#Additional Tasks

|Role|Description|-|
|-|-|-|
|Fixed Value|This is a value which will not be changed. This number will be set from the start.|`NO_OF_RECENT_SCORES = 3`|
|Stepper|This is used to keep track of something.|`Count = 1`|
|Most Recent Holder|This basically holds the latest value encountered.|`GameOver = True`|
|Gatherer|This basically gathers the sum of all values and keeps a running total of values.|-|
|Transformation|This variable always can get assigned a new value when the code runs or iterates.|`Choice = input()`|
|Follower|This variable copies the old value so that, the other variable can get assigned the new value.|-|
|Temporary| This variable holds values for a short time until it appends or assigns it to a different variable.|-|


#Additional Task - Functions and parameters

1.Describe the difference between passing by value and passing by reference in your own words.

 - Passing by Value:  Is when you have a copy of the original and you can modify it without altering the original
 - Passing by Reference: Is when you have the original and you can modify(work with) the original 

2. For each function in the program identify the mechanism using to pass each parameter. Note: this task will take a while but it will improve your understanding of the program and by useful for the exam.

`def GetRank(RankNo):` = RankNo is passed by Reference
`def GetSuit(SuitNo):` = SuitNo is passed by Refrence
`def DisplayMenu():` = None
`def GetMenuChoice():` = None
`def LoadDeck(Deck):` = Deck is passed by Reference
`def ShuffleDeck(Deck):` = Deck is passed by Value
`def DisplayCard(ThisCard):` = ThisCard is passed by Value
`def GetCard(ThisCard, Deck, NoOfCardsTurnedOver):` = 
 - ThisCard is passed by Value
 - Deck is passed by Value
 - NoOfCardsTurnedOver is passed by Value
 `def IsNextCardHigher(LastCard, NextCard):`
 - LastCard is passed by Value
 - NextCard is passed by Value
`def GetPlayerName():` = None
`def GetChoiceFromUser():` = None
`def DisplayEndOfGameMessage(Score):` = Score is passed by Value
`def DisplayCorrectGuessMessage(Score):` = Score is passed by Value
`def ResetRecentScores(RecentScores):` = RecentScore is passed by Value
`def DisplayRecentScores(RecentScores):`  = RecentScore is passed by Value
`def UpdateRecentScores(RecentScores, Score, current_date):`=
 - RecentScore is passed by Value
 - Score is passed by Value
 - current_date is passed by Value
`def PlayGame(Deck, RecentScores):` = 
- Deck is passed by Value
- RecentScore is passed by Value






> Written with [StackEdit](https://stackedit.io/).