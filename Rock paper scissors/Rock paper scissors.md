The World Rock Paper Scissors Society has decided to create a new tournament for robotic players only. The robots must enter pre-programmed with the series of moves that they will make.

The rules are simple: each opponent shows the symbol of rock, paper, or scissors at the same time. Rock beats scissors. Scissors beats paper. Paper beats rock. The losing player takes one robotic step backward and the winner takes one step forward. This repeats until one player has traveled a net five steps forward and is declared the winner.

You will be given the programmed series of moves for each robot. These moves will be used in order (when you get to the end of the series, start again at the beginning). Your task is to determine the winner. Note that a match may have at a maximum 100,000 plays of rock, paper, scissors. If that number has been reached and no winner found, a draw is declared.

#### Input definition

Input consists of two lines. The first line is for robot player one. The second is for robot player 2.

The lines start with the name of the robot player. This is followed by a : character; robot names are not allowed to have : characters in them. This is then followed by the series of moves the robot is to make in single characters. R stands for rock. P stands for paper. S stands for scissors.

#### Output definition

The output consists of two items, the number of rounds played in the match (remember that 100,000 is the maximum). This number should be represented as an integer with only numeric characters.

The second line should contain either the name of the winning robot or the text `:DRAW:`.

#### Example input

```
Johnny 5:RPSRPSR
D.A.R.Y.L.:PPSSPPSSRRPPSS
```

#### Example output

```
21
Johnny 5
```