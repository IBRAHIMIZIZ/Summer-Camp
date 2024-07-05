1) **K-th Largest**  
To find the Kth largest element in the array, sort the array and return the element at index n-k.
```py
def kth_largest(arr, k, n):
    return sorted(arr)[n-k]

n = int(input())
arr = list(map(int, input().split()))
k = int(input())
print(kth_largest(arr, k, n))

# Time complexity: O(N log N)
# Space complexity: O(N)
```


2) **Troop Formation**  
We need to check if the situation is dangerous by searching for a sequence of '0's or '1's repeated 7 times in the string..
```py
def Troop(s):
    condition = 1
    no = True
    for i in range(1, len(s)):
        if s[i] == s[i-1]:
            condition += 1
            if condition == 7:
                return "YES"
        else:
            condition = 1
    if no:
        return "NO"

s = input()
print(Troop(s))

# Time complexity: O(N)
# Space complexity: O(N)
# N is the string size

```
OR
```py
def Troop(s):
    if "0000000" in s or "1111111" in s:
        return "YES"
    else:
        return "NO"

s = input()
print(Troop(s))

# Time complexity: O(N)
# Space complexity: O(N)
# Where N is the string size
```




3) **Pizza Party**
If there are N friends, including Sofia, the pizza needs to be cut into N+1 slices. The minimum number of straight cuts needed is either N+1 (if N is even) or 
(N+1)/2 (if N is odd).
```py
def Pizza(n):
    if n == 0:
        print(0)
    else:
        if n % 2 == 0:
            return n+1 
        else:
            return (n+1)//2

n=int(input())
print(Pizza(n))

# Time complexity: O(1)
# Space complexity: O(1)
```
4) **Anagram**

```py
def Anagram(s1, s2):
    if len(s1) != len(s2):
        return "Not Anagram"
    
    freq1 = {}
    freq2 = {}

    # Count frequencies of characters in s1
    for i in s1:
        if i in freq1:
            freq1[i] += 1
        else:
            freq1[i] = 1
                
    # Count frequencies of characters in s2
    for i in s2:
        if i in freq2:
            freq2[i] += 1
        else:
            freq2[i] = 1

    # Compare the frequency dictionaries
    if freq1 == freq2:
        return "Is Anagram"
    return "Not Anagram"


s1 = input()
s2 = input()
print(Anagram(s1, s2))

# Time complexity: O(N)
# Space complexity: O(N)
# N is lentgh of the longer string
```
OR
```py
def Anagram(s1,s2):
    if len(s1) != len(s2):
        return "Not Anagram"
    # when the both strings are sorted they should be in the same exact order
    if sorted(s1) == sorted(s2):
        return "Is Anagram"
    else:
        return "Not Anagram"

s1=input()
s2=input()
print(Anagram(s1,s2))
# Time complexity: O(NlogN)
# Space complexity: O(N)
# N is lentgh of the longer string
```


