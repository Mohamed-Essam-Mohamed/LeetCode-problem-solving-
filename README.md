# LeetCode Problem Solving
# 1 - Given two strings needle and haystack, return the index of the first occurrence of needle in haystack, or -1 if needle is not part of haystack.

## Example 1:
### Input: haystack = "sadbutsad", needle = "sad"
### Output: 0
### Explanation: "sad" occurs at index 0 and 6.
### The first occurrence is at index 0, so we return 0.
## Example 2:

### Input: haystack = "leetcode", needle = "leeto"
### Output: -1
### Explanation: "leeto" did not occur in "leetcode", so we return -1.

```ruby
public static int strStr(String haystack, String needle ) {
        boolean cheak = false;
        if (haystack.length() < needle.length() )
            return -1;
        // sadbutsad sad    leetcode leeto     hello ll
        for (int i = 0; i < haystack.length()-needle.length()+1; i++) { 
            
            if(haystack.substring(i,i + needle.length()).equals(needle)){
                return i ;
            }
        }
        return -1;
    }
```
# 2 - Given a string s consisting of words and spaces, return the length of the last word in the string.

A word is a maximal 
substring
 consisting of non-space characters only.

 

## Example 1:

### Input: s = "Hello World"
### Output: 5
### Explanation: The last word is "World" with length 5.

## Example 2:

### Input: s = "   fly me   to   the moon  "
### Output: 4
### Explanation: The last word is "moon" with length 4.

## Example 3:

### Input: s = "luffy is still joyboy"
### Output: 6
### Explanation: The last word is "joyboy" with length 6.

```ruby
public static int lengthOfLastWord(String s) {
       s = s.trim();
       int counter =  0 ;
         for (int i = s.length()-1; i >= 0; i--) {
             if( s.charAt(i) == ' '){
                 break;
             }
             counter++;
         }
         
       return counter;
    }
```
```ruby
private static int sum(int a , int b){
        int sumNumber = a - b ;
        if(sumNumber < 0){
            return sumNumber*-1;
        }
        return sumNumber;
        
    }
    public static int scoreOfString(String s) {
        int sum = 0 ;
        for (int i = 0; i < s.length()-1; i++) {
            sum += sum(s.charAt(i) ,s.charAt(i+1));
        }
        return sum;
    }
```
