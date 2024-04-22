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
# Program to search the item in a list using linear search.
# Developed by :RAGHUL V
# RegisterNumber : 212223240132
def linear_search(array,n,k):
    for i in range(0,k):
        if n==array[i]:
            return i
    return -1
array=eval(input())
n=eval(input())
array.sort()
k=len(array)
result=linear_search(array,n,k)
if (result == -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)










```
ii)	# Find the element in a list using Binary Search(Iterative Method).
```
# Program to find the element in a list using Binary Search(Iterative Method).
# Developed by : RAGHUL V
# RegisterNumber : 212223240132
def binary_search(array,n,low,high):
    while(low<=high):
        mid=low+(high-low)//2
        if array[mid]==n:
            return mid
        elif array[mid]>n:
            high=mid-1
        else:
            low=mid+1
    return -1
array=eval(input())
n=eval(input())
array.sort()
result=binary_search(array,n,0,len(array)-1)
if(result== -1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)








```
iii)	# Find the element in a list using Binary Search (recursive Method).
```
# Program to find the element in a list using Binary Search(recursive Method).
# Developed by : RAGHUL V
# RegisterNumber : 212223240132
def binarysearch(array,k,low,high):
    if low<=high:
        mid=low+(high-low)//2
        if array[mid]==k:
            return mid
        elif array[mid]>k:
            return binarysearch(array,k,low,mid-1)
        else:
            return binarysearch(array,k,mid+1,high)
    return -1
array=eval(input())
array.sort()
k=eval(input())
result=binarysearch(array,k,0,len(array)-1)
if(result==-1):
    print(array)
    print("Element not found")
else:
    print(array)
    print("Element found at index: ",result)






```
## Sample Input and Output
![image](https://github.com/Rahulv2005/Search-Algorithms/assets/152600335/5d8b60bb-18ce-4f7a-b39a-492cb02404da)
![image](https://github.com/Rahulv2005/Search-Algorithms/assets/152600335/71188a30-e896-4b54-90be-983dd3c785ea)
![image](https://github.com/Rahulv2005/Search-Algorithms/assets/152600335/01b40e43-fd5a-40f5-b6f6-d0b9d8144760)
![image](https://github.com/Rahulv2005/Search-Algorithms/assets/152600335/17fe6fbf-1a91-4c48-8f45-360e5c756f77)
![image](https://github.com/Rahulv2005/Search-Algorithms/assets/152600335/ca447b80-be91-4e68-b076-dd329404d211)
![image](https://github.com/Rahulv2005/Search-Algorithms/assets/152600335/e475941b-2a60-468f-a5f9-5bfc92074c7c)








## Result
Thus the linear search and binary search algorithm is implemented using python programming.
