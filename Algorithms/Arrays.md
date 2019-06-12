# Easy 

##  Question 1064.Fixed Point
	Description: Find the SMALLEST index in which A[i] == i

	My Solution: check the array not-exist situation then iterate the array 
	from 0 to (length - 1 ) to find the first index matches the requirement.
	
	Time Complexity: O(n);
	Space Complexity: O(1);
 	
## Question 832 Flipping an Image 
	Description: flip the row of binary matrix A then invert it 

	My Solution: Iterative row.length / 2 to flip and inver the node value 

	Time Complexity: O(N) <the size of binary matrix>
	Space Complexity: O(N)

## Question 977 Squares of a Sorted Array
	Description: Given an non-decreasing integer array, return non-decreasing square array.

	My Solution: Brute Force Iterative and Arrays.sort (probably a really bad and ugly choice),need improvement from discussion board.

	Time Complexity: O(nlogn)
	Space Complexity: O(n)

	Improvement: using two pointer to solve the problem, one from the beginning,the other from the end, compare the square of A[i] and A[j] then add the larger one into the square array(which tracked by k)

	Time Complexity: O(n)
	Space Complexity: O(n)

## Question 1051 Height Checker 
	Description: Given an array, find the number which is not in its sorted position;

	My Solution: copy and sort the array, then compare whether the sorted contains the same element as the origin at the same position, count the difference

	Time Complexity: O(nlogn)
	Space Complexity: O(n)

## Question 561 Array partition I 
	Description: find the max sum of min(ai,bi), ai and bi both from array nums

	My Solution: In order to find the max sum, we need to minimize the loss, so sort the array then sum all even index nodes value 

	Time Complexity: O(nlogn)
	Space Complexity: O(n)