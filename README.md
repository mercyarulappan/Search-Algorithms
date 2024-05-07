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
```python
def linearsearch(a,b,array):
    for i in range(0,b):
        if array[i]==a:
            return i
    return -1
array=eval(input())
a=int(input())
b=len(array)
array.sort()
result=linearsearch(a,b,array)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)
```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```python
# Developed by: MERCY A
# Register number: 212223110027

def binary(array,key,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            low=mid+1
        elif array[mid]>key:
            high=mid-1
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found ")
else:
    print("Element found at index: ",result)

```
iii)	# Find the element in a list using Binary Search (recursive Method).
```python
# developed by: MERCY A
# Register number: 212223110027

def binary(array,key,low,high):
    if high>=low:
        mid=low+(high-low)//2
        if array[mid]==key:
            return mid
        elif array[mid]<key:
            return binary(array,key,mid+1,high)
        elif array[mid]>key:
            return binary(array,key,low,mid-1)
    return -1
array=eval(input())
key=int(input())
array.sort()
low,high=0,len(array)-1
print(array)
result=binary(array,key,low,high)
if result==-1:
    print("Element not found")
else:
    print("Element found at index: ",result)

```
## Sample Input and Output
### linear search method:
![Screenshot 2024-05-07 232417](https://github.com/mercyarulappan/Search-Algorithms/assets/149233730/30de55c0-1646-4421-a0ee-7dfc975d0376)
###  Iterative method in binary search:
![Screenshot 2024-05-07 232446](https://github.com/mercyarulappan/Search-Algorithms/assets/149233730/2984e300-c49c-4d09-b2e0-c01440595415)
### Recursive method in binary search:
![Screenshot 2024-05-07 232446](https://github.com/mercyarulappan/Search-Algorithms/assets/149233730/99ce1c53-0e00-48e6-8c5f-561c4eb3137f)

## Result
Thus the linear search and binary search algorithm is implemented using python programming.
