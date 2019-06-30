
## EASY

### 859 Buddy Strings 
	
	Description: Given two strings, check if they are the same by swapping
	onlty two letters in A : 'ab' & 'ba'

	My Solution: it immediately returns false if the length of two strings are not equal, 
	then we check whether two strings are the same or not, if they are the same, 
	we create a hashset and add letters in A to the set, if the size of hashset in A is 
	less than the length of A meaning there are at least one letter that repeats, therefore 
	we can simply swap the repeated letter to maintain A and B the same.
	Last case, if two strings are not the same ,we create a list to store the index of the 
	different value. And return true only if 1.list size equals to 2; 2. the value are opposite 
	on those two indeices. 


	Time Complexity:  O(N);
	Space Complexity: O(1);
	
### 125. Valid Palindrome

	Description: Given a string, regardless any character that is not alphanumberic return 
	if the string is palindrom or not.

	My Solution: two pointer, increase/decrease pointer if it points to non-alphanumberic value, 
	if the string contains no number and letter return true, then compare two pointer value, 
	return false if they are not equal.

	Time Complexity:  O(N)
	Space Complexity: O(1)

### 14 Longest Common Prefix
	
	Description: find the longest common prefix from a string array.

	My Solution: return "" if no string exists, let pre = strs[0], 
	traverse the remaining strings in the array, use indexOf() method to find if the pre
	exists in the array or not, if it does not, do the substring from (0 to pre.length()-1) 
	return pre.

	Since the above solution heavily reply on indexOf method, we use pointer j to generalize:
	compare string.charAt(j) with pre.charAt(j) <j needs to be less than both length>, if they are 
	the same increase j, return the substring from 0 to j.

	Time Complexity: O(m*n) <m for the size of string>
	Space Complexity: O(1)

### 344 Reverse String 
	
	Description: Given a char array, reverse the order of array. Requirement: O(1) memory.

	My Solution: two pointers, i from the beginning and j from the end, swap their pointed value,
	the loop ends when i = j.

	Time Complexity: O(N)
	Space Complexity: O(1)

### 520 Detect Capital 
	
	Description: Given an array, check whether it contains no uppcase / all uppercase / 
	uppercase in the first letter.

	My Solution: Create an integer variable called upperCount, if detect uppercase in the given
	String, count++. return whether count == length / count == 0 / count == 1 && first letter is uppercase

	Time Complexity: O(N);
	Space Complexity: O(1);

### 443. String Compression 
	NOTE: the given function in leetcode is awful, use lintcode for this problem instead 
	https://www.lintcode.com/problem/string-compression/note?_from=ladder&&fromId=94

	Description: Given a string with repeated letters, output new string with repeat letter count 
	if new string is smaller than the original. For example: output "a3b2c5" for "aaabbccccc", but
	"aabbcc" for "aabbcc"

	My Solution: first check if the length of original array <= 1 or does not exist, return the origial
	directly, then we assin two variable: start and end, we check when the first different letter comes,
	if the value start points is different than the end points, we calculate the difference and 
	add the end value to the new string, do this until we iterate the whole original string.
	At the end we double check if the new string's length < original we return new /original.

	Time Complexity: O(N);
	Space Complexity: O(1);

### 824 Goat Latin 

	Description: Given a string S, return the new string with several rules < check details in question>

	My Solution: Split S by space, iterate each word in the array, if the word starts with vowel then 
	copy it to the new string, if it starts with consonant then copy the substring from index 1 to the 
	end first then copy the first letter, after finish all of these, add 'ma' and 'a' * (index + 1) to the end .

	Time Complexity: O(N);
	Space Complexity: O(N);

### 345 Reverse Vowels of a String 

	Description: reverse the order of string  when they are vowels 

	My Solution: Change the string to the char array and use two pointers to check if they point 
	to the vowels,if they do, then swap.

	Time Complexity: O(N);
	Space Complextiy: O(N);

### 387 First Unique Character in a String 
	
	Description： Given a string,return the index of the first unique letter in this string.

	My Solution: create a count array with length of 26, iterate the string and add the count of the
	letter to the array. Re-traverse the string, and check if at its count position, the value is 1,
	if it does, return the index. if none of them unique, return -1.

	Time Complexity: O(N);
	Space Complexity: O(1);

## MEDIUM 

### 8. String to Integer (atoi)

	
	Description: Given a string, convert it to integer if it contains. 
	For example: "-123" -> 123; "123" -> 123 "abc" -> 0 

	My Solution: there are several conditions need to be handle : 
	<check the length as always>
	
	first: eleminate space at the beginning -> traverse the string 
	and if we find space index++;

	second: deal with the minus/ plus sign -> check if the string 
	contanins either sign, if it does, make sign variable equals to -1 / 1, 
	otherwise we always assume sign = 1;
	
	third: deal with the given string larger/ smaller than 32-bit signed 
	integer range -> without consider sign before the number, the absolute value of max 
	is 1 less than min value, hence we check if the existing value * 10 will be overflow 
	or not using max-value / 10 and we also need to consider if 
	existing value == max-value/ 10, will it overflow by adding new digit we just coverted, 
	that is max-val % 10 < digit < new integer> 

	After we handle all the conditions we will return the value * sign;

	Time Complexity: O(N)
	Space Complexity: 0(1)

### 151. Reverse Words in a String 

	Description: Given a string return the reversed string without leading and tailing space.

	My Solution: Use split(" ") to split words into string array, and iterate from the last node, 
	append it into the string builder, if the node value is not "" and string builder length > 0, 
	then append a space (the space between two words), return the sb.toString();

	Time Complexity: O(N);
	Space Complexity: O(1)

### 392. Is Subsequence

	Description: given two strings s and t, check if s is the substring of t.

	My Solution: two pointers, one for loop, the condition is both i < s.length() 
	and j < t.length() traverse string t, if matches both i and j increase, 
	otherwise j increases only, return if i == s.length()

	Time Complexity: O(N)
	Space Complexity: O(1)

### 3. Longest Substring Without Repeating Characters 

	Description: Given a string, find the longest substring without repeating letters.

	My Solution: Using hashmap<letter, index> and two pointers to solve the problem, 
	pointer i traverse the string, and check if the map key already exists, if it does, 
	then j points to the next index, no matter exist or not, put the char and index into 
	the map, update the max value with i-j

	Time Complexity: O(N)
	Space Complexity: O(N)
