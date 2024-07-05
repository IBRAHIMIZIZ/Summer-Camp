1) **K-th Largest**  
To find the Kth largest element in the array, sort the array and return the element at index n-k.
```py
def kth_largest(arr, k, n):
    return sorted(arr)[n-k]

n = int(input())
arr = list(map(int, input().split()))
k = int(input())
print(kth_largest(arr, k, n))\

# Time complexity: O(N log N)
# Space complexity: O(N)
```

Time complixity: O(Nlog(N))
Space complixity: O(N)


2) **Troop Formation**  
We need to check if the situation is dangerous by searching for repeated sequences of '0000000' or '1111111' in the string.
```py
def Troop(s):
    condition = 1
    no = True
    for i in range(1, len(s)):
        if s[i] == s[i-1]:
            condition += 1
            if condition == 7:
                print("YES")
                no = False
                break
        else:
            condition = 1
    if no:
        print("NO")

s = input()
Troop(s)

# Time complexity: O(N)
# Space complexity: O(N)
# Where N is the string size

```
OR
```py
def Troop(s):
    if "0000000" in s or "1111111" in s:
        print("YES")
    else:
        print("NO")

s = input()
Troop(s)

# Time complexity: O(N)
# Space complexity: O(N)
# Where N is the string size
```

