# Poly-time quantum algorithm for graph coloring 

**The Usefulness of Graph Coloring:**
Graph coloring has a lot of applications to our daily lives, such as scheduling and register allocations for programming. Furthermore, graph coloring is an NP complete problem, which means that other NP problems can be reduced to it. If we find a fast polynomial time algorithm for graph coloring, a lot of our current day challenges, such as DNA sequencing, could be solved efficiently.

**Inspiration:**
The inspiration for our project comes from a very recent preprint on a general poly-time method to color a graph validly using a matrix that superposes all possible colorings and handles them in parallel. The use of the matrix was interesting, but this theory had room for improvement, such as allowing various types of graphs, and checking graph coloring outputs to see if they are actually valid colorings. 

**Our Contributions:**
First, we allowed the user to input the number of nodes and the edge connections they wanted. In the original code, the program was not considering edge connections or accounting for them, which caused the theory to be slightly flawed. 
Secondly, we decided to optimize the algorithm by only allowing for optimized colorings. Instead of setting different k-colors to attempt to find valid colorings, we decided to program an approximation of the chromatic number using the Largest First method of the greedy algorithm to set as the k-color to find valid colorings for. This results in an optimized coloring being calculated and outputted by the quantum circuit instead of the user attempting different k-colors in decending order. 
Thirdly, we took nodes that were adjacent to each other (which we can now factor in due to users inputting the edges in the graph), and entangled them using a CNOT gate. This results in adjacent nodes not having the same color when considering colorings, which greatly reduces the sample space and time complexity of the algorithm. We also modified the quantum circuit to account for the entangled adjacent nodes. 
Fourth, since quantum measurements are based on probability, it is likely that outputted colorings may be invalid by just using a quantum circuit. So, we implemented a verification system by converting the bitstring outputted by the quantum circuit (which is a proposed valid coloring of the graph inputted), turned it into a node-edge color system, and checked adjacent nodes to ensure they did not have the same color. This process is also polynomial time since it just depends on the number of nodes and edges. 
Now the algorithm is mostly debugged from the preprint version, and optimized to find valid best-case k-color graph colorings within polynomial time. 

**Future Research Potential:**
This algorithm has a lot of use for the quantum research community. This project could be applied to other NP problems, since other NP problems could be reduced to graph coloring. Similar approaches could be applied to problems such as DNA sequencing to find a cure for cancer. This system of intertwining classical programming and quantum programming could be the key in making current NP algorithms polynomial time on a quantum system. In short, this developed algorithm has a lot of research potential in quantum computational complexity and quantum algorithms. 
