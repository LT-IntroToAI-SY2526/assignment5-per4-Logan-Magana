# Assignment 5 Write up

Assignment 5 can be broken up into the following parts:
1. Import the Necessary Modules:
- `copy`: For creating deep copies of objects
- `Stack` and `Queue`: Custom implementations for DFS and BFS operations
2. Utility Functions: 
- `remove_if_exists`: Removes a specified element from a list if it exists, which is used to remove the possibilites from a cell
3. Board Class:
- Represents the Sudoku board
- Consists of functions that will find the most constrained cell, and update the board, which eliminates possible solutions
4. DFS & BFS Functions:
- `DFS`: Uses depth-first search to solve the Sudoku puzzle. It works by trying to fill the most constrained cell with potential values until a solution is found or backtracks if a mistake is made
- `BFS`: Uses breadth-first search to solve the Sudoku puzzle in a similar fashion to DFS but explores nodes level by level
5. Main Execution:
- Defines two different sets of initial moves for Sudoku puzzles
- Uses both DFS and BFS to solve each puzzle and prints the results


After completing the assignment, answer the following reflection questions:

## Reflection Questions

1. What are some things that you learned through this assignment? Think about the concepts of backtracking, constraint satisfaction, and search algorithms. Were there any particular challenges you faced while implementing the Board class methods or the DFS/BFS functions? How did you overcome them? The main thing I learned from this was the use of DFS and BFS. I was pretty unaware of BFS especially since most problems that I solve involve DFS ( like a maze or a logic puzzle ). I was able to determine that DFS commits to a solution until it reaches a solution or a dead end in which it backtracks and BFS goes through both options step by step until one side becomes a dead end. Although I understood the logic behind both systems, the syntax itself was difficult to write on my own since i'm pretty new to programming. I am able to come up with some psuedo code in my head though.



2. How can you apply what you learned in this assignment to future programs or projects? Consider other types of problems that involve searching through possibilities, making decisions, and backtracking when those decisions don't work out. Can you think of real-world scenarios where DFS or BFS might be useful? What about other constraint satisfaction problems? One scenario that I can think of is chess, which I've started learning about recently.  Although there is a seemingly infinite amount of moves one can make in a game of chess, if you narrow the scope to a move or two, you can use DFS or BFS to exucute the best move possible. Since it is against another player, there may be another section in the program that is used to predict the other players move, which may require another DFS or BFS but from the "players" perception.



3. Explain how the Stack and Queue classes work and why they are important for DFS and BFS algorithms. Describe the difference between LIFO (Last In First Out) and FIFO (First In First Out) data structures. How does using a Stack versus a Queue change the way the search algorithm explores possible solutions? Why is one data structure better suited for depth-first search and the other for breadth-first search? DFS uses the stack class ( which is basically FIFO ). The stack class makes it so the new boards created go on the "top" of the boards. This is useful for DFS because it can backtrack eaisily based on how the stack class is organized. If it recieves a failure test, it can remove the top boards until it reaches the most recent board with more than one possibility. BFS uses the queue class ( which is LIFO ). When creating a clone because it has reached multiple possible assignments, it will pop the oldest board which is the first item in the list. Because of this structure, BFS can play out the multiple boards at the same time instead of being constrained to update only one like DFS. 
