# PROLOG PROJECTS

The following projects can be found in the 'projects' folder.
To run each one make sure you have a SICStus Prolog installation and consult the file within the respective 'src' folder of each project with the name of that project (racingkings.pl, houses.pl or zurero.pl).

## Racing Kings

In this game, checks are entirely forbidden: not only is it forbidden to move one's king into check, but it is also forbidden to check the opponent's king.

The purpose of the game is to be the first player to move their king to the eighth row. When White moves their king to the eighth row, and Black, immediately on the next move, moves their king to the eighth rank, the game is declared a draw (this rule is to compensate for White's first-move advantage).

Apart from the above, pieces move and capture exactly as in normal chess.

**Final Grade: 19.5/20**

## Zurero

This game is an interesting variation of Go-Moku, in which players "slide" stones along the board lines from the edge of the board till the "sliding" stone is stopped by another stone on the board.

The intriguing feature of the game is that the "sliding" stone pushes the "stopping" stone if there is an empty space behind it.

**Final Grade: 19.6/20**

## Houses

This project is based on a CLPFD (Constraint Logic Programming with Finite Domains) solution.
The Houses Puzzle’s is a puzzle created by Erich Friedman, a puzzles enthusiast, with the objective of connecting pairs of houses so that there are at max two different distances. These pairs of houses, with only one connection each, are created with the elements of a list with even number of house coordinates, which is the puzzle’s input.

**Final Grade: 18.9/20**


# PROLOG CONVENTIONS FOR BETTER CODE

## Predicate names

Lower case letters with words delimited by underscore.

**Example** ast_node (not ASTnode or astNode)  
**Reason** consistency with standard Prolog notation and in-built predicates

## Variables

Java-style but start with capital letter.

**Example** AVeryLongVariableName (not a_very_long_var_name)   
**Reason** Shorter and easier to write than the underscore variant. The leading capital letter is required by PROLOG to identify variables.

## Comments

Commenting style from official SWI-Prolog code, public at their repository.
* '+' can be used to describe an argument that should be instantiated
* '-' can be used to describe an argument that the predicate will instantiate
* '?' can be used to describe an argument which can be either instantiated or not

**Example** 

```c
/*  max_member(-Max, +List)
    
    True when Max is the largest  member in the standard order of terms.  
    
    Fails if List is empty.
*/
  max_member(Max, List).
```

**Reason** Better documentation and quick understanding of the predicates


## Line breaking

One predicate per line.   

If argument list is too long, put one argument in every line with matching brackets in same column.  

**Example** 

```c

mortal(X):- 
  alive(X).

example_with_long_parameter_list(X, Y, Z):-
  findall(X,
         (long(Z,X), conjunction(X), of(X,Y), predicates(X)),
         Result),
  next_predicate(Result).

```

**Reason** Better code readability.
