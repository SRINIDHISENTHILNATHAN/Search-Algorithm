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
Developed by:SRINIDHI SENTHIL
RegisterNumber: 22001408
'''
def linearSearch(array,n,k):
    # write your code for linear search
    for i in range(0,n):
        if array[i]==k:
            return i
    return -1
    
array = eval(input())
# sort the array
k = eval(input()) # k-item to be seared for
# get the length of array and store in the variable n
n=len(array)
array.sort()
result=linearSearch(array,n,k)
if (result !=-1):
    print(array)
    print("Element found at index: ",result)
# use the function for linear search
# use if-else to print sorted array and "Element not found" if the item is not present in the list otherwise print sorted array and "Element found at index: ", result
else:
    print(array)
    print("Element not found")
```

ii)	# Find the element in a list using Binary Search(Iterative Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:SRINIDHI SENTHIL
RegisterNumber: 22001408
'''
def binarySearchIter(array, k, low, high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            low=mid+1
        else:
            high=mid+1
    return -1
    
        
array = eval(input())
array.sort()
print(array)
k=eval(input())
low=0
high=len(array)-1
result=binarySearchIter(array,k,low,high)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")
```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
''' 
Program to find the element in a list using Binary Search(Iterative Method)..
Developed by:SRINIDHI SENTHIL
RegisterNumber: 22001408
'''
def binarySearch(array, k, low, high):
    #write your code for linear search
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]<k:
            return binarySearch(array,k,mid+1,high)
        else:
            return binarySearch(array,k,low,mid+1)
    return -1
    
        
array = eval(input())
array.sort()
print(array)
k=eval(input())
low=0
high=len(array)-1
result=binarySearch(array,k,low,high)
if result>=0:
    print("Element found at index: ",result)
else:
    print("Element not found")
    
```
## Sample Input and Output

i) #Use a linear search method to match the item in a list.
![image](https://user-images.githubusercontent.com/121373170/214590614-ade18698-9d8f-4e8e-9309-bba881e6bcc8.png)

ii)	# Find the element in a list using Binary Search(Iterative Method).
![image](https://user-images.githubusercontent.com/121373170/214590704-016d2aa2-5057-472a-b356-9e1194a31f9a.png)

iii)	# Find the element in a list using Binary Search (recursive Method).
![image](https://user-images.githubusercontent.com/121373170/214590830-2395c7ca-9193-424f-b51f-6da3920e6379.png)



## Result
Thus the linear search and binary search algorithm is implemented using python programming.
