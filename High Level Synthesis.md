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
