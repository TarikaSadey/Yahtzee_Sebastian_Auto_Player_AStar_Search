
### THE GAME OF SEBASTIAN
* The problem poses a one player game of luck and skill of rolling five dice and write an algorithm to obtain a maximum
  score within 13 chances provided we need to choose optimum re-rolls of specific dice using none or 2 more chances per 
  specific turn.
  
* Within one game of thirteen turns, we need to assign dice roll to specific categories in the score card given a 
  category can be only assigned once per a game.
  
#### Problem Abstraction:
* We have implemented expectation probability concept to obtain the optimal best score using the below described 
  technique.

* For each first roll of random selection of dice we have considered all possible combinations of die roll and 
  calculated expected score for each combination.
  
* The expected score is obtained by assigning the die combination to all possible 13 categories and storing the 
  category and its respective score into a dictionary.
  
* We then take the best score from the sorted dictionary and send it to max_layer function. We then compare each expected
  score and store the max score for each combination. After all the iterations we send back the best possible re-roll
  indices to be rolled in the second chance. 
  
* Similar process is followed for the second roll.

* The third roll function gives the best category from the list of available unassigned categories in each game for a 
  given best die combination after second re-roll.
  
* The minimum, maximum and mean scores are then calculated after the player plays 100 games giving us the desired output.

#### Problems Faced:
* Assignment of best category for a given turn has proved to be quite a task when calculating the max expected value of
  each die roll combination which we have overcome by eliminating the already assigned categories from the list.
  
* We have eliminated the duplicate combinations of die roll to optimize time complexity of the code.
