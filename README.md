# LeetCode-3.Longest_Substring_Without_Repeating_Characters

Given a string, find the length of the longest substring without repeating characters.

Example 1:

Input: "abcabcbb"
Output: 3 
Explanation: The answer is "abc", with the length of 3. 

Solution Python3:
class Solution:

    def lengthOfLongestSubstring(self, s):
    
        dicts = {}
        maxlength = start = 0
        
        for i,value in enumerate(s):
            # "abcabcbb" 
            # "bbbbb"
        
            if value in dicts:
                sums = dicts[value] + 1
                if sums > start:
                    start = sums
                    
            num = i - start + 1
            
            if num > maxlength:
                maxlength = num
                
            dicts[value] = i
            # dicts = {a:1}, maxlength = 1
            # dicts = {a:1,b:2}, maxlength = 2
            # dicts = {a:1,b:2,c:3}, maxlength = 3
    
        return maxlength

            
