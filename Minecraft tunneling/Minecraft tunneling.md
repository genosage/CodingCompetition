You are to assume the role of Steve in the Minecraft world. He is looking to dig a path from a given point to his destination, using a pickaxe of limited durability.

Since the durability of the pickaxe is limited, he is looking to take the least number of swings at the rocks/minerals/dirt to arrive at his destination.

Your task is to calculate the least number of swings that need to be made to create a tunnel through the ground (a cube in this scenario) from one point to another. Moves must be in only one dimension at a time, i.e. the path cannot contain diagonal steps.

### Input definition

#### Input Format

The first line of the input contains the cube size N.

The second line of the input contains the hardness(H) (number of swings required to break) of each block of the cube (N^3 total).

The third line contains the target start block, which consists of 3 numbers representing x,y,z coordinates, in that order.

The forth line contains the target end block, which consists of 3 numbers representing x,y,z coordinates, in that order.

#### Constraints

```
2 <= N <= 25

0 <= H <= 10

start block != end block
```

#### Detailed explanation of line 2 format

Consider the following line 2 input. 3 4 7 3 4 1 0 2

The corresponding cube should be laid out like this.

```
Z Position 0

y
1 |7 3
0 |3 4
   ------x
   0 1
```

```
Z Position 1

y
1 |0 2
0 |4 1 
  ------x
   0 1
```

If a target start block of 0 1 1 was provided, we could see the hardness of this block would be 0.

![](https://msft3c.com/Content/Images/fy2016/MinecraftCube.png)

### Output definition

Output a single integer, representing the smallest number of pickaxe swings required to create a path from the start block to the end block.

Note: Since hardness values are provided for the starting and ending coordinates, those blocks must be broken and those swings are to included in the total count.

### Example input

```
2
3 4 7 3 4 1 0 2
0 1 0
1 0 1
```

### Example output

```
10
```