## EASY PROBLEMS 

### 771.Jewels and Strones 

	Description: Given two strings, one for the jewels the other for the stones, 
	find how many characters are there in the stone that is the same as characters 
	in the jewel string.

	My Solution: Using hash set: create a hash set for jewels characters and 
	check if the character in the stone strings has already added to the set, 
	if it does, count++;

	Time Complexity: O(M+N); => M: size of jewel string, N: size of stone string 
	Space Complexity: O(M);

### 938. Range Sum of BST 

	Description: Given the root of BST, find the sum of all nodes value that 
	between two values: L and R (inclusive).

	My Solution: Use recursion to solve the problem, we have three cases to think 
	about the root value.
	First, if the root value > R, then the value is out of range, we recursive call 
	root.left to see if it satisfies our desire.
	Second, if the root value < L, then the value is also out of range, we go to root.
	right to check again.
	Third, the root value stays the range, then we want to add the value to the output, 
	and recursively call root.left and root.right to further detect possible nodes.

	Time Complexity: O(N) 
	Space Complexity: O(H) < the height of the tree, O(N) for the extreme case >  

### 905. Sort Array By Parity 

	Description: Given a none-negative integers array, re-order the array so that all 
	the even numbers come first and odd numbers follow.

	My Solution: Two Pointers, i starts from the beginning, j starts from the end, 
	if A[i] is odd, and A[j] is even, do the swap and change the pointing position 
	(i increment and j decrement), otherwise increase/ decrease i /j by condition,
	i.e: A[i] is even i++, A[j] is odd j--;

	Time Complexity: O(N)
	Space Complexity: O(N)

### 977. Squares of a Sorted Array (the same solution in the array problems set)

	Description: Given an non-decreasing integer array, return non-decreasing square array.

	My Solution: use two pointer to traverse the original array and k to add 
	square element to the ans array. output ans array.

	Time Complexity: O(N)
	Space Complexity: O(N)

### 929 Unique Email Addresses 
	
	Description: find the number of unique email addresses: when local name contains 
	'.', it will be ignore , when local name contains '+', the rest characters 
	before '@' will be ignored.

	My Solution: add email to hash set, using string builder and switch case to distinguish 
	different email address, when charAt(i) == '+', use a for loop to traverse all the 
	character until it meets '@' then append all the rest string to the string builder, 
	output the stringbuilder to string, and add the string to the hash set,
	return the size of hash set for the answer.

	Time Complexity: O(N)
	Space Complexity: O(N)

### 942.DI String Match 
	
	Description: Find the Permutation arr for the given string S which contains 'I' 
	and 'D' only, if S[i] == "I", then A[i] < A[i+1]; if S[i] == "D", then A[i] > A[i+1].

	My Solution: Let's consider two extreme cases:
	Case 1: "DDDD" A = [4,3,2,1,0] as A[i] > A[i+1] > A[i+2] > ...> A[S.length()]
	Case 2: "IIII" A = [0,1,2,3,4] AS A[i] < A[i+1] < A[i+2] < ... < A[S.length()]

	Therefore, we can see that 'D' starts from S.legth() and 'I' starts from 0, therefore
	 we use two variables to trace the times each letter shows in the string and put that 
	 value in the proper index position. and output the ans array.

	Time Complexity: O(N)
	Space Complexity: O(N)

### 463. Island Perimeter 
	
	Description: Find the perimeter of island, that is given a 2d array, and 1 represents 
	land and each cell is a square, find the perimeter of all the 1 in array.

	My Solution: first iterate the 2d array if the cell is 1 num++, and check its right and 
	up neighborhood is 1 or not, if it does count  = count + 2 * (2) <if they both are 1>
	because we only check one side not the other, meaning if its right for example [1][1] 
	is a square, then when we check the cell [1][1] we will not check its left, however there 
	is a square we've checked, therefore we need to count twice. 
	After the loop ends, we return num * 4 - count for the perimeter of the island.

	Time Complexity: O(N) < size of 2d array>
	Space Complexity: O(1)

### 482. License Key Formatting 
	
	Description: Reformat the given string, remove the dash and add dash every k letters from the end,
	all the letters should in uppercase, return the new string.

	My Solution: Iterate the string, if found dash continue the loop, check if count == k if it does add
	dash into the new string builder, and count back to zero else add the letter uppercase and count ++;
	return the reverse string builder to string.

	Time Complexity: O(N)
	Space Complexity: O(N)


