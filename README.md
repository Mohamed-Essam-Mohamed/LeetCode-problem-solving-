# LeetCode Problem Solving

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
