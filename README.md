# 4T-LE-Refinement
Creates refinement of a given 2D Triangular Mesh using the 4T LE Refinement method.
The file contains 3 classes of types Vertex, Edge and Triangle.

Vertex:
Contains two variables of Type "double" which are x and y positions of the vertex.

Edge:
An Edge can be created using two objects of Type "Vertex".
Variables of Edge are:
Vertex 1, Vertex 2,
type of Type "int" // type is used to identify where the edge is in the domain
                  // All interior edges are assigned type=0 and all exterior edges have type!=0
count of Type "int" //Used to delete obsolete edges during bisection of triangles
	                  //Edge of type 0 becomes obsolete when count becomes 2
	                  //Edge of type Non Zero becomes obsolte when count becomes 1
oppVer of Type "vector<Vertex>" //oppVer is used to track the triangles of this edge                    

Boundary Edges of the initial INPUT MESH have to be stored in 'edg' vector<Edge> by assigning a 'NON ZERO INTEGER' as their type.
Initial INPUT MESH TRIANGLES have to stored in 'trgl' vector<Triangle>.
