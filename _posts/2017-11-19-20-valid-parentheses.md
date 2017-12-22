---
layout   : post
title    : "LINKED LISTS"
subtitle : "SINGLY LINKED LISTS -> DOUBLY LINKED LISTS -> CIRCULAR LINKED LISTS"
date     : 2017-11-19 20:45:00
author   : Rubie
tags:
    - OOP
    - Python
    - ValidParentheses
    - Dict
---


# Description
Given a string containing just the characters '(', ')', '{', '}', '[' and ']', determine if the input string is valid.

The brackets must close in the correct order, "()" and "()[]{}" are all valid but "(]" and "([)]" are not.

# Python
- run time: `66ms`
- Memory(MB) : -
- Big-O: -

```
class Solution(object):
    def isValid(self, s):
        tmp = []
        dic_a = {')':'(', ']':'[','}':'{'}
        for x in s:
            if x in dic_a.values():
                tmp.append(x)
            elif x in dic_a.keys():
                if not tmp or tmp.pop() != dic_a[x]:
                    return False
            else:
                return False
        #return tmp==[]
        return not tmp
```
