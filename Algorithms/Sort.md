## Easy

### 506 Relative Ranks

	Description: Given an integer array, return string array with the first 
	three largest as "gold medal", "silver medal" and "bronze medal", all the 
	other left with string number. 

	My Solution: clone the original array, and sort the new array rank. put the rank 
	to the map with their value and the difference from the arraylength to index.
	Traverse the original array and find the rank from the map, add the required input
	to the string array, return array.

	Time Complexity: O(NlogN);
	Space Complexity: O(N)

### 21 Merge Two Sorted Lists 
	
	Description: Given two sorted linked list, merge them into one sorted list 

	My Solution: Two pointers iterate two list, if one is smaller than the other, 
	the new node points to the smaller one,pointer go to the next.

	Time Complexity: O(M+N);
	Space Complexity: O(N);