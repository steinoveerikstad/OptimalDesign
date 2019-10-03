# Finding an initial feasible solution

Recall from solving a general linear optimization problem, that the first step was to find an initial feasible solution, from which we could start to iterate towards the optimal solution. In the LP formulation this was, for a problem in the standard form, simple since the slack variables became the basic variables, so in practice it meant starting with zero values for the real decision variables.

For a transportation problem this will not work. First, we have no slack variables (because of the feasible solutions property saying that supply = demand), and second, since setting the real variables (i.e. the amount to be transported) to zero is never a fesible solution. Thus, we have to find another way to find the initial feasible solution. There are several ways to do this. In general, we can use a simple methods that typically gives an initial solution that is far from the optimum, or we can use more sophisticated methods that get us closer to the optimum. Here, we will look at three methods:

* The Northwest Corner method
* The Minimum Unit Cost method
* Vogel´s method

As an example, we will use a simple transportation problem (from the 2007 exam) for optimizing transport between a number of Nordic ports (Oslo, Gothenburg and Fredrikshavn) and a number of Europeand ports (Hull, Rotterdam, Hamburg and Oostende). The parameter table is given in the table below:

<img src="ParamtableExam2007.png" width="500">

## The Northwest Corner method

The simplest method to find an initial feasible solution is by starting assigning as many transportation units as possible to the upper left cell of the table - the _Northwest_ corner. The number of units will ve constrained by either the supply constraint found in the rightmost column, or the demand constraint in the bottom row, as illustrated in the figure below:

<img src="OptTP-NWStep1.png" width="350">

By adding 5 transport units into cell 1,1 we have used all supply available from Oslo ($s_1$), and can thus take the remaining cells in row one away. We then go one step down to cell 2,1. Here we are contrained by the supply from Gothenburg (row 2, being 8) and the remaing demand from Hull (column 1, being 6-5=1). Thus, we assign the smallest of these to the cell, as in the figure below: 

<img src="OptTP-NWStep2.png" width="350">

We continue with this pattern, going right or down dependent on the supply and demand constraints, until we reach the right-lower corner of the table. We now have an initial fesible solution to the transportation problem, as given in the table below:

<img src="OptTP-NWStep3.png" width="350">


