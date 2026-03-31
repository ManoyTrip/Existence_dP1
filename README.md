# Existence_dP1
This repository contains two folders with Magma code accompanying the article "Existence of minimal del Pezzo surfaces of degree 1 with conic bundles over finite fields" - Manoy T. Trip. 
NB: The code was executed in Magma v28-25. Using different versions of Magma may result in differing output (notably, a difference in the ordering of the conjugacy classes of W(E_8)).

The folder Table_Computation contains Magma files related to the computation of properties associated with each type of del Pezzo surface of degree 1 over Fq.
- RepresentationE6E7E8: In this file, we compute a representation of W(E6), W(E7), W(E8). It stores them in a magma state file "RepresentationE6E7E8_noAIM".
- Functions: This file contains Magma functions that are used in the computations in "E7" and "E8".
- E7: In this file, we compute the following properties associated with each type of del Pezzo surface of degree 2:
  - order of Frobenius
  - Size of the conjugacy class
  - Size of the orbits of the lines under the Frobenius action
  - Intersection pattern within each orbit
  - Index
  - Eigenvalues of the Frobenius action
  - Picard rank
  - trace
  The properties are listed in the output file "OutputdP2.txt"
- E8: In this file, we compute the following properties associated with each type of del Pezzo surface of degree 1:
  - order of Frobenius
  - Size of the conjugacy class
  - Size of the orbits of the lines under the Frobenius action
  - Intersection pattern within each orbit
  - Index
  - Eigenvalues of the Frobenius action
  - Picard rank
  - trace
  The properties are listed in the output file "OutputdP1.txt"
-E7E8_execution.txt: Executing this file will run the computation. It needs the Magma state file "RepresentationE6E7E8_noAIM", as well as the text files "Functions", "E7", "E8". 

The folder Existence_Bounds contains Magma files related to the computation of bounds on q for the existence of del Pezzo surfaces of degree 1 over Fq.
- ContractDP1: In this file, we compute for each type of dP1, what are the possible resulting types of dP2 when we blow down one line defined over Fq, if it exists. Conversely, for every type of dP2, we determine which type of dP1 is obtained when we blow up 1 point outside of the "bad locus".
- LowerBoundExistencedP1: In this file, for each type of dP1 with a line defined over Fq, we compute a lower bound on the value of q such that a dP1 over Fq of this type exists for all values above this bound.
- ExistenceLowq: For each type of dP1 of index 8, we compute for small values of q whether 8 points in general position in the corresponding configuration exist in P^2.
