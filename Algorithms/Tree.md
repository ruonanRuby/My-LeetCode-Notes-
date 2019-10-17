## Easy 
### 104.Maximum Depth of Binary Tree
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
### 112.Path Sum
	Description: Given a sum, find if there is a root-to-leaf path, that its sum equals 
	to the given sum.

	My Solution: Recusive call the left and right node, at the same time, decrease the sum
	by the value of root, if any leaf value equals to the current sum, return true, else 
	return false.

	Time Complexity: O(N);
	Space Complexity: O(h); (logN best case; N worst case)

### 404.Sum of Left Leaves
	Description: find the sum of all left leaves.

	My Solution: Recursive call the left and right node, mark true as it is the left node, 
	false as it is the right node, return the value if it is left leaf, but 0 if it is the 
	right, the final result will be the total sum of left subtree and the right subtree.
	We can write the equation sum(t) = left(t, true) + right(t,false);

	Time Complexity: O(N);
	Space Complexity: O(h); 