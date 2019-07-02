## Easy 

### 475. Heaters 
	Description: given two arrays one for house position and another for heater position, 
	find the minimum radius standard of heaters to cover all the houses.

	My Solution: Use binary search to narrow the minium radius that the heater can cover.
	First sort houses and heaters array, as we know that the house and heater position will 
	not exceed 10^9, so our right pointer starts from 10^9 and left pointer starts from 0, 
	then calculate the mid, do the binary search of the mid(which is the radius range), we 
	check that given a radius range if all the houses can be coverd by heater (a check method
	might be needed), if it can, we narrow the radius range by moving right piinter to mid position,
	if it cannot we enlarge the radius range letting left pointer to mid + 1 position.
	we return the mid. 

	Time Complexity: O(nlogn);
	Space Complexity: O(1);


## Medium 

### 34. Find First and Last Position of Element in Sorted Array 
	Description: Given an integer array and a target number return an array contains 
	the first and last index of the target number in the given array.

	My Solution: Use two binary search to find the first and last index of the target number.
	The idea is basically the same of find the first and the last, create a variable cur,
	keep track of the position of the target value in the array, return cur,the only different is 
	moving the pointer, that is find the first -> move right pointer and find the last -> move 
	the left pointer. To avoid that the original array length == 1, we need to check 
	one side pointer when return the cur. that is check left pointer == target when return first index,
	check right pointer == target when return last index. return the index array.

	Time Complexity: O(logn)
	Space Complexity: O(1)