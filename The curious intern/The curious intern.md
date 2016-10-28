Samantha the Intern is leaving Microsoft soon, and wants to visit the fun places around the Puget Sound before she goes. She doesn't have much time so she decides to rank each spot on a fun scale from 1 to 99, inclusive.

As she moves farther west into Seattle, there are more fun things to do, with the number of fun things equal to the length of her trip.

![](https://msft3c.com/Content/Images/fy2016/FunThingsToDo.png)

Samantha doesn't like travelling far between fun spots, so after visiting a spot she can only move to an adjacent spot.

![](https://msft3c.com/Content/Images/fy2016/AnAdjacentSpot.png)

Every time she moves, she wants to go deeper into the city. Can you help Samantha by finding the most possible fun she can have by the end of her day?

There are 2 to the power of L possible paths, so Samantha hopes you don't try to brute force the solution.

#### Limits:

L layers, where 45 <= L <= 55. Each layer will consist of fun scores F, where F is from [0, 100).

#### Input:

L, which is the number of layers to follow. Followed by L lines of space-delimited fun scores, where the number of scores is equal to the depth (1 score at a depth of 1, 2 scores at a depth of 2, etc.).

#### Output:

The number corresponding to the sum of scores in the greatest possible path.

#### Input definition

The input will be a number, followed by that many lines of space-delimited numbers. Each subsequent line will have one more number/score than the line before. Extra padding included for readability should be ignored.

#### Output definition

A single number corresponding to the greatest path through the graph. When moving down through the graph, only adjacent numbers can be considered.

#### Example input

```
5
        20
      35  22
    09  17  12
  04  05  34  04
76  41  61  01  48
```

#### Example output

```
167
```