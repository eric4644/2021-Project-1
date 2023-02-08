The Huffman Compression Program

You will implement a subset of steps in the Huffman compression algorithm.  

1. Count how many times every character occurs in a file. These counts are used to build weighted nodes that will be leaves in the Huffman tree. For this assignment, assume your input will be text files and you can process your data in 8-bit chunks. 

2. Create a heap (priority queue) and enter the character/frequency pairs that you found in step one into the heap. The heap should be ordered by the frequency.

3. Build the Huffman tree from the heap. Pop the two minimal nodes from the heap, join these nodes together as children of a newly created node, and insert the newly created node back into the priority queue. The new node is weighted with the sum of the two minimal nodes taken from the priority queue. Continue this process until only one node is left in the priority queue. This is the root of the Huffman tree.

4. Create a table that maps each characters (8-bit chunks) to a prefix code. The table of encodings is formed by traversing the path from the root of the Huffman tree to each leaf, each root-to-leaf path creates an encoding for the value stored in the leaf. When going left in the tree append a zero to the path; when going right append a one. All characters/encoding bit pairs may be stored in some kind of table or map to facilitate easy retrieval later.

You are responsible for implement the heap in file heap.c; the Huffman tree in file tree.c; as well as the code generation in code.c. 
