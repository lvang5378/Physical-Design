## Analytic techniques
- Model the placement problem using an objective (cost) function, which can be optimized via numerical analysis
- Examples: quadractic placement, and force directed placement

###Quadratic placement
On lecture, page 25/33
- Objective function is quadratic; sum of (weighted) **squared Euclidean distance** represents placement objectuve function.  

        L(P) = 1/2* sum [Cij*( (xi-xj)^2 + (yi-yj)^2 )]  
n is the total number of cells, and c(i, j) is the **connection cost between cell i and j**.

- Only two-point-connections
- Minimize objective function by equating its derivative to zero which **reduces to solving a system of linear equations.**
   
---


- Each dimension can be considered independently: 
        
      Lx(P); Ly(P)
- Convex quadratic optimization problem: any local minimum solution is also a global minimum    `??? definition of convex quadratic optimization problem????`
- Optimal x- and y-coordinates can be found by setting the partial derivatives of Lx(P) and Ly(P) to zero
  - partial derivative of Lx(P) = AX-bx = 0; Ly(P) = AY-by = 0;
    - A is a matrix with A[i][j] = -c[i][j] when i!=j
    - A[i][j] = the sum of incident connection weights of cell i
    - X is a vector of all the x-coordinates of the **non-fixed cells**, 
    - and bx[i] = the sum of x-coordinates of all **fixed cells** attached to i
    - Y is a vector of all the y-coordinates of the **non-fixed cells**, 
    - by[i] = the sum of y-coordinates of all **fixed cells** attached to i
- System of linear equations for which iterative numerical methods can be used to find a solution.

---

#### Mechanical analogy: mass-spring system
  * Squared Euclidean distance is proportional to the energy of a spring
between these points
  * Quadratic objective function represents total energy of the spring system;
**for each movable object, the x (y) partial derivative represents the total force
acting on that object**
  * Setting the forces of the nets to zero, an _equilibrium_(平衡, 均衡) state is mathematically
modeled that is characterized by zero forces acting on each movable object
  * At the end, all springs are in a force equilibrium with a minimal total spring
energy; this equilibrium represents the minimal sum of squared wirelength  

**Result: many cell overlaps**

---

####Second stage of quadratic placers: cells are spread out to remove overlaps
- Methods:
  - Adding fake nets that pull cells away from dense regions toward anchors
  - Geometric sorting and scaling
  - Repulsion forces, etc.


---
####Adv and dis-adv
- Advantages:
  - Captures the placement problem concisely in mathematical terms
  - Leverages efficient algorithms from numerical analysis and available software
  - Can be applied to large circuits without netlist clustering (flat)
  - Stability: small changes in the input do not lead to large changes in the output
- Disadvantages:
  - Connections to fixed objects are necessary: I/O pads, pins of fixed macros, etc.
