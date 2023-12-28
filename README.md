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
## Developed by: NITHISH KUMAR S
## Reference Number: 23013506
i)	#Use a linear search method to match the item in a list.
```
def linearsearch(array,n,k):
    for i in range(0,n):
        if (array[i]==k):
            return i
    return -1
array=eval(input())
k=int(input())
n=len(array)
array.sort()
result=linearsearch(array,n,k)
if (result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
def binarysearchIter(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array=eval(input())
array.sort()
k=eval(input())
result=binarysearchIter(array, k, 0, len(array)-1)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
def Binarysearch(array, k, low, high):
    while low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid-1
    return -1
array=eval(input())
array.sort()
k=eval(input())
result=Binarysearch(array, k, 0, len(array)-1)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)

```
## Sample Input and Output

1) ![image](https://github.com/nithish467/Search-Algorithm/assets/150232274/b42e9186-b1e0-41db-a26f-fa3786190dac)

![image](https://github.com/nithish467/Search-Algorithm/assets/150232274/2d1507bf-d321-437f-b679-34e0f6b8a32b)


2) ![image](https://github.com/nithish467/Search-Algorithm/assets/150232274/6cfeb3e4-447d-44cf-9680-fa63331bd32e)

![image](https://github.com/nithish467/Search-Algorithm/assets/150232274/e1c05f7d-69d9-4c16-b4da-725746b3d32d)


3) ![image](https://github.com/nithish467/Search-Algorithm/assets/150232274/a920951f-93fe-4236-8719-ab9c9367cf3c)

![image](https://github.com/nithish467/Search-Algorithm/assets/150232274/6d11eb80-c486-400a-a020-370aa0ac33f1)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
