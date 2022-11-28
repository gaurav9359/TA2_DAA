# TA2_DAA

##### NAME - GAURAV PATHAK
##### SUBJECT - DAA(TA2)
##### ROLL NO. - A40
##### BATCH - A2


Using the NumPy library and the random.randint() method, we populated a (n x n) matrix, randomly with only 0 and 1 values.

Inorder to convert this matrix into a graph, we had to first convert it into an Adjacency List. This step was necessary because the graph that would be formed by the matrix of ramdom 0's and 1's would be directed.

Now this Adjacency List was passed into the actual logic of the program where we were expected to find a cycle. There is a cycle in a graph only if there is a back edge present in teh graph. Depth First Traversal can be used to detect a cycle in a Graph, because DFS for a connected graph produces a tree.

So in this program using DFS, we check if the graph is disconnected and if it happens to be disconnected, then we get the DFS forest and check for a cycle in individual trees by checking the back edges. To detect a back edge we had to keep track of vertices cirrently in the recursion stack of function fot the DFS traversal. We come to the conclusion that the graph has a cycle if a vertex is reached that is already in the recursion stack.

Create the graph using the adjacency list.
Create a recursive function that initializes the current vertex, visited array, and recursion stack.
Mark the current node as visited and also mark the index in the recursion stack.
Find all the vertices which are not visited and are adjacent to the current node and recursively call the function for those vertices
  If the recursive function returns true, return true.
  If the adjacent vertices are already marked in the recursion stack then return true.
Create a wrapper function, that calls the recursive function for all the vertices, and
  If any function returns true return true.
  Else if for all vertices the function returns false return false.
