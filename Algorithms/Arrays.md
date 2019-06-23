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

## Question 766 Toeplitz Matrix 

	Description: return true if every diagonal in a matrix from top-left to bottom-right has the same element.

	My Solution: the diagonal means starting from [i][j] both indices increment by one i.e. [i + 1][j + 1],therefore, we compare the value to see if they are same or not 

	Time Complexity: O(N) < the size of matrix>
	Space Complexity: O(1)

## Question 566 Reshape the Matrix 

	Description: reshape the matrix with given new row and column 

	My Solution: since the total number of values is the same, so we have i from 0 to (r*c)-1, with that we have i/c = new row index i % c = new column index, FYI: c is the new column number 
	i/nums[0].length = row index, i%nums[0].length = column index. Hence we can put the value into the new array.

	Time Complexity: O(N)< The size of nums matrix>
	Space Complexity: O(N)

## Question 243 Shortest Word Distance 
	
	Description: find the shortest distance between two given words in the array.

	My Solution: Iterate the array and check if the value equals to any given word, if it does, keep the index as first for word1 or second for word2, once one index changed, compare the current minimum distance with the new minimum distance to find the min, and return the min after iteration.

	Time Complexity: O(N)
	Space Complexity: O(1)

## Question 888 Fair Candy Swap 

	Description: output the swap value from two array so that the sum of each array values is the same.

	My Solution: sort two arrays, then check the first array with the output sum, if it is less than sum meaning it needs larger value from second array, if it is larger than sum meaning it needs swap larger value to second array.output the ans array.

	Time Complexity: O(n^2)
	Space Complexity: O(1)

## Question 1014 Partition Array Into Three Parts With Equal Sum 

	Description: return a boolean value to see if the array can be make up by three subarrays, which have the same sum.

	My Solution: first check if the total sum of array can be divided by 3 and the length >=3, if not then return false directly, then using two pointers, one starts from the beginning one starts from the end,  if one side reach the goal then wait the other side and return true if both side = (sum/3)

	Time Complexity: O(n)
	Space Complexity: O(1)

## Question 896.Monotonic Array 
	
	Description: return a boolean value if the array is monotonic increasing/ decreasing or not. 
	monotonic increasing: i < j A[i] <= A[j] monotonic decreasing: i < j A[i] >= A[j]

	My Solution: using two boolean value to compare local max/ min between two adjacent value, if it is decreasing then it is not mono increasing, it is increasing then it it not mono decreasing. return (monoInc || monoDec)

	Time Complexity: O(N)
	Space Complexity: O(1)

## Question 485 Max Consecutive Ones 
	
	Description: return the max number of consecutive 1s in the array.

	My Solution: count the consecutive 1s in the array, if the next value is 0 count becomes 0, then update the global max with Math.max(count,max) return the max.

	Time Complexity: O(N)
	Space Complexity: O(1)

## Question 283 Move Zeroes 
	
	Description: move all 0's in the array the the end while mainting the relative order of none-zero elements.

	My Solution: two pointers, i iterates the array, one it points to none- zero element, check the other pointer j , if it points zero, swap, otherwise increase j.

	Time Complexity: O(N)
	Space Complexity: O(1)

## Questin 448 Find All Numbers Disappeared in an Array 
	
	Description: Given an array with value all 1<= arr[i] <= n, find the numbers that never appear in the array but within the range. 

	My Solution: Since value is 1 difference to the index, therefore we can use the index to solve the problem.
	First iterate the array and find the index = arr[i] - 1, then make the arr[index] to negative number.
	Second, traverse the array again, if the value is larger than 0 meaning we never touch that index then add index + 1 to the output list .

	Time Complexity ; O(N)
	Space Complexity: O(1)

## Question 169 Majority Element 

	Description: find the majority element in an array, that is the value that appears in the array more than length/2 times.

	My Solution: first solution: as the number appears more than n/2 time (n = length of array), therefore, we sort the array then output arr[n/2] which will be the number we want 

	Time Complexity: O(nlogn);
	Space Complexity: O(1);

	second Solution: this algorithm learned from http://www.cs.utexas.edu/~moore/best-ideas/mjrty/index.html, 
	we count the time that one elements shows in the array, if the count == zero, we record the element as the output, if the next element is not the output value, we decrease the count by one, otherwise we increase the count by one, the output val will be the one we want. 

	Time Complexity: O(n);
	Space Complexity: O(1);