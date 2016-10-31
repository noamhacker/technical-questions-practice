# technical-questions-practice
A collection of practice questions I've worked on.
<hr>
* CTCI page 90 question 1.1:
Implement an algorithm to determine if a string has all unique characters. What if you cannot use additional data structures?
  * [Code](http://ideone.com/embed/jrtcab#)

* CTCI page 90 question 1.2: 
Given two strings, write a method to decide if one is a permutation of the other.
  * [Code](http://ideone.com/xjYP6B) (better space-efficiency than CTCI solution!)

* CTCI page 91 question 1.5:
Check if two strings are one edit or zero edits away (edit = insert, remove, or replace a character).
  * [Code](http://ideone.com/yUTcNY) (incomplete)

* to-do: CTCI page 91 1.7, 1.8, and 1.9

* CTCI page 94 question 2.1:
Write code to remove duplicates from an unsorted linked list. Also try an O(1) space solution.
  * [Code](http://ideone.com/rmQ5Rn)

* CTCI page 95 question 2.7:
Given two singly linked lists, determine if the two lists intersect, and return the intersecting node (based on reference, not value).
  * [Code](http://ideone.com/KwJqfy)

* CTCI page 99 question 3.4:
Implement a Queue class which implements a queue using two stacks.
  * [Code](http://ideone.com/p2kyu3)

* CTCI page 109 question 4.2: Given a sorted increasing array, create a binary search tree with minimal height.
  * [Code](http://ideone.com/wekUzn)

* CTCI page 109 question 4.3: Given a binary tree, create a linked list of all the nodes at each depth (if the tree's depth is N, you must create N linked lists)
  * [Code](http://ideone.com/tYH7Mj), using HashMap instead of ArrayList

* CTCI page 110 question 4.5: Implement a function to check if a binary tree is a binary search tree.
  * [Code](http://ideone.com/8oTq3U)
  
* CTCI page 116 question 5.3: You have an integer and you can flip exactly one bit from a 0 to a 1. Write code to find the length of the longest sequence of 1s you could create.
  * [Code](http://ideone.com/9Vujnx), worst case O(n^2) but can be improved to O(n) with some simple logic

* CTCI page 134 question 8.1: A child is running up a staircase with n steps and can hop either 1 step, 2 steps, or 3 steps at a time. Implement a method to count how many possible ways the child can run up the stairs.
  * [Code](http://ideone.com/TjzBnK), bottom-up approach, O(n) time, O(1) space (compared to CTCI's top-down O(n), O(n) solution).
  
* CTCI page 135 question 8.2: Find the shortest path in a grid where certain cells are off limits. You start at the top left and want to get to the bottom right, and you can only move right or down. 
  * My solution would start at the bottom right and visit every cell, using a second grid to store the value of steps away it is from the goal (each cell is 1 step more than its smallest adjacent cell's length). Then from the top right, continuously move to the adjacent cell with the lowest step value. Visiting each cell means O(rc) time, with r being row and c being column. CTCI's solution uses recursion to follow a similar strategy (find if a path exists from the start to cells progressively further away from the goal) and is also O(rc) time, but less than O(rc) space (which mine is). Both solutions are dynamic programming approaches, and I believe my algorithm has the potential to find the shortest path while CTCI's algorithm simply finds a possible path.
  
* CTCI page 135 question 8.5: Write a recursive function to multiply two positive integers without using the * operator (or / operator). You can use addition, subtraction, and bit shifting, but you should minimize the number of those operations.
  * [Code](http://ideone.com/rm6DQ7)

* InterviewBit [Flatten Binary Tree to Linked List](https://www.interviewbit.com/problems/flatten-binary-tree-to-linked-list/): Given a binary tree, flatten it to a linked list in-place (a tree with only the right nodes populated in a straight line).
  * [Code](http://ideone.com/N8N30i) (copy and paste into InterviewBit's environment). There may be a more optimal way to not store an ArrayList and instead build the answer on the fly. The time complexity is O(n) because we visit each node once (pre-order traversal).
