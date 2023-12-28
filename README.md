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
Developed by: D Vergin Jenifer
RegisterNumber: 23004210 
'''
def linearSearch(array,n,k):
    result=0
    sorted_array=sorted(array)
    print(sorted_array)
    for i in range(n):
        if sorted_array[i]==k:
            result=i
            break
    if result!=0:
        print("Element found at index: ",result)
    else:
        print("Element not found")
array = eval(input())

n=len(array)
k = eval(input()) 
linearSearch(array,n,k)

```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..

Developed by: D Vergin Jenifer
RegisterNumber: 23004210
'''
def binarySearchIter(array, k, low, high):
    array.sort()
    while low<=high:
        mid=(low+high)//2
        mid_val=array[mid]
        if mid_val==k:
            return mid
        elif mid_val<k:
            low=mid+1
        else:
            high=mid-1
    return -1
    
array = eval(input())

k = eval(input()) 
low, high=0,len(array)-1
result=binarySearchIter(array, k, low, high)
print(sorted(array))
if result!=-1:
    print("Element found at index: ",result)
else:
    print("Element not found")

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search (recursive Method).
Developed by: D Vergin Jenifer
RegisterNumber: 23004210
'''
def binarySearch(array, k, low, high):
    if low<=high:
        mid=(low+high)//2
        mid_val=array[mid]
        if mid_val==k:
            return mid
        elif mid_val<k:
            return binarySearch(array, k, mid+1, high)
        else:
            return binarySearch(array, k, low,mid-1)
    else:
        return -1
    
array = eval(input())

k = eval(input()) 
low=0
high=len(array)-1
result=binarySearch(sorted(array),k,0,len(sorted(array))-1)
print(sorted(array))
if result!=-1:
    print("Element found at index: ",result)
else:
    print("Element not found")

```
## Sample Input and Output
![image](https://github.com/VerginJenifer/Search-Algorithm/assets/136251012/b1d8dbb9-4880-44e6-bc1d-65b015d01bde)


![image](https://github.com/VerginJenifer/Search-Algorithm/assets/136251012/8e0f9da7-2ca9-417a-94de-5c4e06d1313c)


![image](https://github.com/VerginJenifer/Search-Algorithm/assets/136251012/2228216d-d2ae-4efe-9166-ca1329c90ad6)


## Result
Thus the linear search and binary search algorithm is implemented using python programming.
