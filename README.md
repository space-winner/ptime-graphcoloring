# Poly-time quantum algorithm for graph coloring 
Graph coloring algorithm which inputs a graph from the user
Calculates the approximate chromatic number using the greedy algorithm, sets off to find valid coloring with chromatic number
Entangles adjacent nodes so that colorings don't have adjacent nodes colored the same color
Quantum circuit stores valid colorings in a superposed N * k matrix, then amplifies probabilities of valid colorings using Grover's Algorithm
Possible valid colorings encoded in bitstrings, but could be invalid
Classical system converts bitstring to coloring and checks adjacent nodes
Optimal valid colorings outputted
