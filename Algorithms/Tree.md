## Easy 
### 104 Maximum Depth of Binary Tree
	Description: Given a binary tree, find its maximum depth.

	My Solution: Using recursion traverses root.left / right, return 
	the maximum value between left and right depth.

	Time Complexity: O(N)
	Space Complexity: O(1)

### 637. Average of Levels in Binary Tree
	Description: find the average value of each level in the tree return as a list.

	My Solution: iterate the binary tree, count the sum of each level 
	and the nodes count of each level, then calculate the average and return.

	Time Complexity: O(N);
	Space Complexity: O(h); <the height of the tree>