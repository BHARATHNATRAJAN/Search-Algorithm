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
i)	#Use a linear search method to match the item in a list.
```
''' 
Program for linear search method to match the item in a list
Developed by: Bharath.N
RegisterNumber: 23003413
'''
def linearSearch(array,k):
    for i in range(len(array)):
        if array[i]==k:
            return i
    return -1
    
array = eval(input())
k = eval(input())
array.sort()
result = linearSearch(array,k)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)




```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by: Bharath.N
RegisterNumber: 23003413
'''
def binarySearchIter(array, k):
    low=0
    high=len(array)-1
    mid=0
    while low <= high:
        mid = (high+low)//2
        if array [mid]<k:
            low=mid+1
        elif array[mid]>k:
            high = mid-1
        else:
            return mid
    return -1
    
array = eval(input())
array.sort()
k = eval(input())
result =binarySearchIter(array,k)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ", result)





```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: Bharath.K
RegisterNumber: 23013413
'''
def BinarySearch(arr, k, low, high):
    if high >= low:
        mid=(high+low)//2
        if arr[mid]==k:
            return mid
        elif arr[mid]>k:
            return BinarySearch(arr,k,low,mid-1)
        else:
            return BinarySearch(arr,k,mid+1,high)
    else:
        return -1
    
arr = eval(input())
arr.sort()
k=eval(input())
low=0
high=len(arr)-1
result=BinarySearch(arr,k,low,high)

if (result ==-1):
    print(arr)
    print("Element not found")
else:
    print(arr)
    print("Element found at index: ", result)






```
## Output
![output](/output1.png)
![output](/output2.png)
![output](/output3.png)





## Result
Thus the linear search and binary search algorithm is implemented using python programming.