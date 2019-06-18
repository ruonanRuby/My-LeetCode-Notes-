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

## Question 922 Sort Array By ParityII
	Description: Given an non-negative integer array, sort them so that A[i] is even when i is even and A[j] is odd when j is odd

	My Solution: Two pointer, i iterates even index and j iterates odd index, swap when A[i] == odd && A[j] == even. 

	Time Complexity: O(n);
	Space Complexity: O(1);

## Question 509 Fibonacci Number 
	Description: calculate F(N) with given non-negative integer N;

	My Solution: Dynamic Programming, create a DP array and return arr[N];

	Time Complexity: O(N);
	Space Complexity: O(N);

## Question 1085 Sum of Digits in the Minimum Number 
	Description: find the sum of minimal digits return 1 if it is even and 0 if it is odd.

	My Solution: Iterate array and find the min, then mod 10 to get the sum of last digit, divide 10 th make the number smaller, loop ends when min number == 0 

	Time Complexity: O(N);
	Space Complexity: O(1);

## Question 1086 High Five
	Description: Given a 2d array with student id and their scores, find the average of top five scores for every student and return a new 2d array to store it. 

	My Solution: Using hashmap with priority Queue as key value. 

	Time Complexity: O(n^2log(n));
	Space Complexity: O(N);

## Question 1002 Find Common Characters
	Description: Given a string array, output the common characters that show up in all string and output the minimim times as the character shows i.e.: 'l' 'l' for 'roller' etc.

	My Solution: Create an array to count the minimum times that each character shows in every string, meaning 'apple' p with 2 times but 'play' for 1 time. Iterate each string in string array and count the times character shows up, then find the total minimum after traversing the whole array. 
	Output the string list as it required.

	Time Complexity: O(N);
	Space Complexity: O(1);

## Question 867 Transpose Matrix
	Description: transpose the matrix A by flipping over its main diagonal. Ex: A[[1,2], [3,4]] ANS: [[1,3], [2,4]]

	My Solution: Create a new 2D array ANS with flipped the index of A, then output the new 2D array.

	Time Complexity: O(N) <the size of A> 
	Space Complexity: O(N)

## Question 985 Sum of Even Numbers After Queries 
	Description: return the sum of even value in A after adding value from given index in the queries array

	My Solution: find the original sum, then add / minus value whether the given index is calculated in the sum and whether the new value is even or odd.

	Time Complexity: O(N)
	Space Complexity:  O(N)