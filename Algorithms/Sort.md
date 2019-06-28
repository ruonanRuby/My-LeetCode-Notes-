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

## Medium 

### 179 Largest Number 
	
	Description: Given a list of non negative number, return a largest number string 
	that these number can form.

	My Solution: Create a string array and sort it with the required order, that is, 
	'ab' > 'ba' then add the new sorted array into the string and return the string.

	Time Complexity: O(nlogn);
	Space Complexity: O(N)

### 75. Sort Colors 

	Description: Given an integer array with one three types of number 0 -> red 
	1 -> white 2 -> blue,sort the array by the order of red -> white -> blue,i.e. 0,1,2.

	My Solution: Use three pointers, i points to 0, j points to 2, and k iterates the array,
	swap when k points to 0/2, increase k only when k points to 0/1.

	Time Complexity: O(N);
	Space Complexity: O(1); 