Download Link: https://assignmentchef.com/product/solved-cse100-algorithm-design-and-analysis-lab-15
<br>
<strong>Graphs: read/print graph; graph ops (BFS)</strong>

Provided C++ file Graph.cpp contains the definition of a struct Graph. The struct stores the information necessary to represent a directed weighted graph. A list called vertices stores the vertices, which are indicated as strings. A map called edges stores the edges. The key in the map is the edge, defined as a pair of strings, which are possible vertex names. The value is the weight of the edge. You can assume that the weights are all non negative. The class provided cannot be changed; you can only add methods, if needed, and variables, but you cannot change the underlying representation used to store the adjacency list.

<strong>Input structure </strong>Read from the keyboard the described graph and store it using an instance of the class Graph. The input is divided in sections. The first section starts with the vertices’ names. There is one name per line. You can assume that names do not contain any space. The list of vertices terminate when the string END is read. Then the section describing edges starts. For each edge you have the starting vertex, the ending vertex, and the weight. The section ends when you read the string END. As usual, the END strings should not be processed. Note that the input may contain the erroneous edges connecting vertices not declared in the former section; these edges should not be inserted. Once the graph has been built, print out its structure using the provided PrintOut function.

Then start a cycle where you read operation codes and parameters and perform the following operations:

<ul>

 <li><em>Operation code 0</em>, no parameters: terminate the program.</li>

 <li><em>Operation code 1</em>, 1 parameter of type string (called <em>A</em>): print 1 if <em>A </em>is a vertex in the given graph, 0 otherwise.</li>

 <li><em>Operation code 2</em>, 2 parameters of type string (called <em>A </em>and <em>B</em>): print the edge cost if the edge (<em>A,B</em>) exists, −1 otherwise.</li>

 <li><em>Operation code 3</em>, 2 parameters of type string (called <em>A </em>and <em>B</em>): print the number of edges from vertex <em>A </em>to <em>B</em>, −1 if unreachable. You have to implement breadth-first search (BFS) to solve this part of the assignment.</li>

</ul>

Example input/output is given on the next page.




<em>Example input                                                           Example output</em>

Bremen                           Bremen

Hannover                         Hannover

Hamburg                          Hamburg

Osnabruck                        Osnabruck

END                             Bremen Hannover 123

Hannover Bremen 123             Hamburg Hannover 190

Hannover Osnabruck 50            Hannover Bremen 123

Bremen Hannover 123             Hannover Osnabruck 50

Hamburg Hannover 190              1

END                              0

1 Bremen                         -1

<ul>

 <li>Brem 50</li>

 <li>Osnabruck Hannover 0</li>

 <li>Hannover Osnabruck 2</li>

 <li>Hannover Hannover -1</li>

</ul>

3 Hannover Hamburg

3 Osnabruck Bremen

0