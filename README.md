# Graph Representations

Implement a function that converts an adjacency matrix to an adjacency list for
a directed unweighted graph using the template in `code.js`. Test your new
function; I've provided some basic testing code that uses
[jsverify](https://jsverify.github.io/) in `code.test.js`. Now, the test code
does contain the solution, so you can have a look at it if you get stuck, but
try not to peek before attempting to solve it on your own.

## Runtime Analysis

What is the runtime complexity of the conversion that you implemented? Does it
depend on the number of vertices, the number of edges, or both?

Describe your reasoning and the conclusion you've come to. Your reasoning is the
most important part. Add your answer to this markdown file.

## Bonus

Implement a function to convert an adjacency list to an adjacency matrix and
analyze it as above.

Runtime analysis:

The runtime complexity is O(n^2), where n is the number of vertices in the graph.  This is because all of the for loops in the code have a runtime of O(n^2), as the first loop iterates over all n vertices of the graph and fills the matrix with n X n vertices, and the nested for loops each run n times since they also are iterating over all n vertices, resulting in the combined runtime of O(n^2).  The runtime complexity depends only on the number of vertices, as each vertex will be checked whether there is an edge or not.

I did all of the work myself except when determining how to write line 8.  I was unsure if the line should be written how it is now, adjMatrix[vertex][adjList[vertex][neighbor]] = 1, or if it should be written as adjMatrix[vertex][(adjList[vertex][neighbor] - 1)] = 1, so I asked ChatGPT if the values in an adjacency list are treated as actual values or as index values, and I used its response (index values) to determine that there is no -1 necessary in the line of code.

For the test file, I edited your given test file for the adjMatrix -> adjList and used ChatGPT to help explain what your test file was doing and used it to help me write my test file.

I certify that I have listed all sources used to complete this exercise, including the use of any Large Language Models.  All of the work is my own, except where stated otherwise.  I am aware that plagiarism carries severe penalties and that if plagiarism is suspected, charges may be filed against me without prior notice.

-----

I submitted this assignment last semester.  I did the bonus as a replacement for the main assignment since I was unable to get the main one accepted.
