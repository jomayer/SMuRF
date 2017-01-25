# SMuRFS
The SMuRF algorithm
Authors: Joshua Mayer, Raziur Rahman, Souparno Ghosh, Randip Pal
Platform: R Version 3.3.2
Required packages:  partykit, Formula, strucchange, matrixStats
###############################################################
#########<b> inputs </b> ######################################
Formula: 
################################################################
################################################################

The following is the function to run the Sequential Multi Response Feature Selection (SMURFS). The function grows a tree using the conditional inference framework (Hothornet <i> et al. </i>, 2006) then selects the features that are significant at any node of the tree. Features that are not selected are tested on a test set that is a subset of the data. Features that fail the second test are removed from consideration. 
