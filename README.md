# Rock Paper Scissors Cellular Automata


I have seen the concept implemented but I did not find any rule sets for it.

So I am trying to do this from scratch.

I start by created a grid of 32 by 32 cells, which is smaller than most implementations I have see

I have two grids one for updating and one for the current, as in other CAs

## The rule set I started with (then abandoned) was:
    
    if any killer exists in that cells neighborhood that cell takes the killers type

    for example if the cell you are looking at is ROCK and their is PAPER in any of the 8 neighbor cells
    ROCK is then changed to Paper

  For this version I randomly filled the grid with RPS and it had a very boring 

  outcome.  And added some random copy errors when to create some random movement



## The second and current rule set looks at the total number of each type in the neighborhood:

    -if the cell is blank it takes the type that is greatest non blank  type
    -- this makes the cells seem to grow like bacteria

    -if the cell is rock and there is more paper than rock in the   neighborhood (including the cell itself) -- rock changes to paper

    -if the cell is paper and there are more scissors than paper in the   neighborhood (including the cell itself) --paper changes to scissors

    -if the cell is scissors and there are more rocks than scissors in the neighborhood (including the cell itself) --scissors changes to rocks


This leads to a boring state rather quickly as each type carves out its place

so I have added a copy error when copying one generation to the next

with around a  one in 100 chance of picking a different type it creates something that mirrors living colonies at war with one another

This "cross contamination" creates a nice bacteria like growth and destruction with pockets of rock growing inside an expanse of scissors and paper growing inside of rock. 

This is a different result to other implementations with other rules. some linked below.

link to live page of my rock paper scissors ca

https://greggelong.github.io/rpsca


some links to papers and other implementations with different rules

https://softologyblog.wordpress.com/2018/03/23/rock-paper-scissors-cellular-automata/

https://web2.qatar.cmu.edu/~gdicaro/15382/additional/rock-paper-scissor-bacterial-diffusion-CA.pdf
 