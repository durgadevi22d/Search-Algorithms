# Linear Search and Binary search
## Aim:
To write a program to perform linear search and binary search using python programming.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
## Linear Search:
1.	Start from the leftmost element of array[] and compare k with each element of array[] one by one.
2.	If k matches with an element in array[] , return the index.
3.	If k doesn’t match with any of elements in array[], return -1 or element not found.
## Binary Search:
1.	Set two pointers low and high at the lowest and the highest positions respectively.
2.	Find the middle element mid of the array ie. arr[(low + high)/2]
3.	If x == mid, then return mid.Else, compare the element to be searched with m.
4.	If x > mid, compare x with the middle element of the elements on the right side of mid. This is done by setting low to low = mid + 1.
5.	Else, compare x with the middle element of the elements on the left side of mid. This is done by setting high to high = mid - 1.
6.	Repeat steps 2 to 5 until low meets high
## Program:
### i) Use a linear search method to match the item in a list.

#### Use a linear search method to match the item in a list.
#### Developed By: DURGADEVI P
#### Register Number : 212223100006
```
def linearSearch(array,n,k):
 for i in range(0,n):
     if(array[i]==k):
        return i
 1/5
 return -1
array = eval(input())
k=eval(input())
n=len(array)
array.sort()
res=linearSearch(array,n,k)
if(res==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",  res)
```
### ii) Find the element in a list using Binary Search(Iterative Method).

#### Find the element in a list using Binary Search(Iterative Method).
#### Developed By: DURGADEVI P
#### Register Number : 212223100006
```
def binary(lst , n, low, high):
    while low<=high:
        mid = low+ (high -low)//2
        if lst[mid]==n:
            return mid
        elif lst[mid]<n:
            low = mid+1
        else:
            high = mid-1
    return -1
lst = eval(input())
lst.sort()
n=eval(input())
result = binary(lst,n,0,len(lst)-1)
if(result==-1):
    print(lst)
    print("Element not found")
else:
    print(lst)
    print("Element found at index: " , result)
```
### iii) Find the element in a list using Binary Search (recursive Method).

#### Find the element in a list using Binary Search (recursive Method).
#### Developed By: DURGADEVI P
#### Register Number : 212223100006
```
def binary(lst , n, low, high):
    if low<=high:
        mid = low+ (high -low)//2
        if lst[mid]==n:
            return mid
        elif lst[mid]>n:
            return binary(lst , n, low, mid-1)
        else:
             return binary(lst , n , mid+1, high)
    else:
        return -1
lst = eval(input())
lst.sort()
n=eval(input())
result = binary(lst,n,0,len(lst)-1)
if(result==-1):
    print(lst)
    print("Element not found")
else:
    print(lst)
    print("Element found at index: " , result)
```
## Sample Input and Output
[output](/1.png)
[output](/2.png)
[output](/3.png)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
