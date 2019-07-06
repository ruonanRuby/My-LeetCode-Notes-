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

### 540 Single Element in a Sorted Array 
	 Description: Given a array where every element appears twice except one, find the single
	 element using O(logN) time and O(N) space.

	 My Solution: Using binary search to solve the problem, as we know that if there is 
	 no such a element, then there will be 2*k elements total,but now it is 2*k + 1
	 therefore we can use binary search to locate the element space, if it is in the odd space, 
	 then return right, if it is in the even space then return left. 

	 Time Complexity: O(logn)
	 Space Complexity: O(N)

### 162. Find Peak Element 
	Description: Find the peak index of the array, that is the number in that index is larger than 
	its adjacent two numbers. 

	My Solution: Using binary element to find the index, if < mid + 1,left = mid + 1 
	if < mid - 1,right = mid. return the largest number between left and right

	Time Complexity: O(logN)
	Space Complexity: O(N)

### 153 Find Minimum in Rotated Sorted Array
	Description: Find the minimum number in the ascending rotated at unknown pivote order array.

	My Solution: check the last value with the first, if the last is larger return the first 
	as the array is in ascending order, then do the binary search, if the mid is larger then 
	nums[0] then left = mid + 1, else right = mid, return mid if it is smaller than its two adjacent 
	values, and return the smaller value in left and right if there is no return in the loop.

	Time Complexity; O(logN)
	Space Complexity: O(1)

### 33 Search in Rotated Sorted Array I
	Description: Given an sorted array in ascending order, then rotate it with an unknown pivot,
	find the target number in the array, return index if it exist return -1 if it is not.

	My Solution: Draw a picture for this problem which helps sovling. 
	Fist check if either left or right or mid is the target if it does return directly.
	If not, there are four cases:
	First: Both mid and target in left to peak range -> right = mid
	Second: Both mid and target in bottom to right range  -> left = mid + 1
	Third: Target is in left to peak range but mid is in bottom to right range -> right = mid 
	Fourth: Target is in bottom to right range and mid is in left to peak range. -> left = mid + 1
	return -1 if we cannot find the target.

	Time Complexity: O(logN)
	Space Complexity: O(1)

### 81 Search in Rotated Sorted Array II
	Description: Most the same as the last question,but this one allows duplicate values,
	question 33 does not. 

	My Solution: Based on the last question algorithm, and consider the cases that the mid 
	value equals to left value, or mid value equals to right value. 
	If mid == left > right  -> left = mid + 1;
	If mid == right < left -> right = mid;
	else mid == left == right (we cannot make sure which side the mid is) then we do left ++;

	return true if nums[mid] == target.

	Time Complexity: O(logN);
	Space Complexity: O(1)