##internal representation:
```
Data-flow graph (DFG)   
- Describes datapath  
Control-flow graph  
- Describes control circuits  
Signal-flow graph  
- For DSP (Digital Signal Processing)  
```

###Data flow graph: G(V, E)

##Scheduling:
###ASAP, 
equivalent to finding the longest path in a a DAG
###ALAP:
run the longest path algoithm in reversed topological order:

###Force directed scheduling:
fource  = spring_constant * displacement

###Critical path list scheduling:

###Conflict graph:
**Edge (u, v) <= if task u and v cannot be executed on the same agent**  
- assignment by min-color   NP-complete
- left edge algorithm 
- complimentary graph, then assignment by clique partitioning


##Logic Synthesis In Practice
```terminology: implicant, prime implicant, irredundat cover, canonica forms```  
1. Specify the logic-level behavioral description of the circuit in some HDL
2. Extract from this description the Boolean expressions and represent them in some internal form
3. Manipulate the expressions to obtain an optimized representation (two-level or multilevel)
4. Perform **technology mapping**, from the abstract representation to a netlist of cells from a library 


##ordered BDD (OBDD)
** fixed order is essential for canonical representation **
####Reduced OBDD

##Boolean satisfiability :
"Satisfiability is the problem of determining if the variables of a given Boolean formula can be assigned in such a way as to make the formula evaluate to TRUE” -- quote from wikipedia
```
Also called SAT problem
Famous NP problem
There are public domain SAT solvers
Some combinatorial optimization problems and most ILP problems can be formulated as SAT problem
```
