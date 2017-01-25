# SMuRFS
<h1> The SMuRFS algorithm </h1>

<b> Authors: </b> Joshua Mayer, Raziur Rahman, Souparno Ghosh, Randip Pal

<b> Platform: </b> R Version 3.3.2

<b> Required packages: </b>  partykit, Formula, strucchange, matrixStats


<b> Inputs </b>

<strong> Formula: </strong> A object of class formula. This formula will give the inherent regression equation.

<strong> data: </strong> A object of class data frame. Names in the data frame must match the names in the formula. Missing data are removed.

<strong> ntree: </strong> An integer greater than or equal to 1. The number of trees grown for the SMuRFS algorithm.

<strong> mtry: </strong> An integer greater than or equal to 1. The number of variables sampled for each tree.
################################################################
################################################################

The following is the function to run the Sequential Multi Response Feature Selection (SMURFS). The function grows a tree using the conditional inference framework (Hothornet <i> et al. </i>, 2006) then selects the features that are significant at any node of the tree. Features that are not selected are tested on a test set that is a subset of the data. Features that fail the second test are removed from consideration. 
