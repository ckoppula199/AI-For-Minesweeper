# AI-For-Minesweeper
Demo: https://www.youtube.com/watch?v=MYeM4G5D6dE  

AI for the game minesweeper that uses propositional logic to come up with inferences based on a knowledge base to solve a minesweeper board.  
  
Completed as part of Harvards CS50 Intro to AI course.  
  
{A, B, C, D, E, F, G, H} = 1 represents a logical sentence that says out of cells A, B, C, D, E, F, G, and H, exactly 1 of them is a mine.  
  
If {A, B, C} = 0 then we know A, B and C are safe and don't contain mines. Anytime we know out of a set of cells, 0 of them are mines, we can mark them all as safe.  
  
If {A, B, C} = 3 then we know A, B and C are all mines. Anytime the length of the set is equal to the number of mines present then we know all members of the set are mines.  
    
If {A, B, C, D, E} = 2 and {A, B, C} = 1 we can deduce that {D, E} = 1. Anytime Set B is a subset of set A we can rewrite A = x for all x in A and x not in B (A difference B) and the number in mines of A = mines in A - mines in B.  
  
Using these inference rules our AI should be able to solve a minesweeper board. This approach does not guarantee a win, there may be points where no inferences can be made and a random move must be made for new inferences to be made.

  
Note: I was responsible for writing the Sentence and MinesweeperAI classes in minesweeper.py file. The rest of the code is provided by Harvard CS50 and is not my own work.

To run simply enter python runner.py in the command line in the same directory as the project.

