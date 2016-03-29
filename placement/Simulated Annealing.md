#Simulated Annealing requires:
1. State representation:
2. Move set
3. Cost function
4. Cooling schedule

###Example:
####Annealing on a slicing tree,    
1. state representationsL its just the slicing tree itself  
2. move set: what do we perturb? what changes?    
  each annealing move perturbs the topology of the whole tree, small move can relocate ALL modules  
    move types:  
      - subtree swaps  
      - node cut inversion   
      - leaf node change  
3. cost function:    
  area of layout + weight*(Sum of wirelength)
4. cooling schedule  
