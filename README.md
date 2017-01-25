# SMuRFS
<h1> The SMuRFS algorithm </h1>

<b> Date: </b> 1/25/2017

<b> Authors: </b> Joshua Mayer, Raziur Rahman, Souparno Ghosh, Randip Pal

<b> Platform: </b> R Version 3.3.2

<b> Required packages: </b>  partykit, Formula, strucchange, matrixStats

<b> Maintainer: </b> Joshua Mayer <emph> joshua.mayer@ttu.edu </emph> 

<b> Description </b> The following is the function to run the Sequential Multi Response Feature Selection (SMURFS). The function selects a subset of features of size <emph> mtry </emph> and a bootstrap sample of size <emph> n </emph>, grows a tree from those features and that bootstrap sample using the conditional inference framework (Hothornet <i> et al. </i>, 2006), then selects the features that are significant at any node of the tree. Features that are not selected are tested on a test set that is a subset of the data. Features that fail the second test are removed from consideration. After <i> ntree </i> iterations the features that survive are the selected features.

<h2> Usage </h2>

SMuRFS(formula, data, ntree = 500, mtry, alpha = 0.05, prop.test = .632, response.position)

<b> Inputs </b>

<strong> Formula: </strong> A object of class formula. This formula will give the inherent regression equation.

<strong> data: </strong> A object of class data frame. Names in the data frame must match the names in the formula. Missing data are removed.

<strong> ntree: </strong> An integer greater than or equal to 1. The number of trees grown for the SMuRFS algorithm. Default is 500.

<strong> mtry: </strong> An integer greater than or equal to 1. The number of variables sampled for each tree.

<strong> alpha: </strong> An number between 0 and 1. The significance level declared for feature removal.

<strong> prop.test: </strong> A number between 0 and 1. The size of the test set for the secondary test, as a proportion of the data. Default is 0.632.

<strong> response.position: </strong>  The column of which the responses are located. It could be done automatically with the Formula package, but this breaks down in high dimensions.
################################################################
################################################################


