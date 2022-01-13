# Algorithm

| Algorithm | Specific Type | Related LeetCode Test | Related Article |
| --------- | --------------|-----------------------|-----------------|
|           | Bubble Sort | TBC |TBC |
|           | Selection Sort | TBC |TBC |
| Sorting Algorithm | Insertion Sort | LeetCode 147 Insertion Sort | [Notes](#jump1) |
|           | Hill Shell Sort | TBC |TBC |
|           | Quick Sort | TBC |TBC |
|           | Merge Sort | TBC |TBC |
|           | Heap Sort | TBC |TBC |
|           | Linear Sorting Algorithm | TBC |TBC |



<span id = "jump1">
    

# Insertion Sort Algorithm
When you play the card games, actually you are doing insertion sort.

You can kindly click [here] (https://www.hackerearth.com/practice/algorithms/sorting/insertion-sort/visualize/) to see a dynamic graph demo of the insertion sort algorithm.


![image](https://user-images.githubusercontent.com/69109871/149294730-00cbc348-15f7-47e2-987d-d79a4558b95f.png)

Let's demonstrate step by step about how to implement insertion sort algorithm in an array.
## Insertion Sort Algorithms in Array

Here comes an example of Arr = [5, 1, 0, 6]

- Step 1: split the arry list into two lists. The forward list contains all the sorted elements(by default the 1st element is sorted) while the second list contains unsorted or to be sorted elements.

- Step2: Start iteration for the unsorted list, which means we'll start from the 1st element (Arr[1] = 1) by default.
    set a varialbe called toSortNumber = Arr[i]
    
- Step3: Do the iteration for all the elements on the left of the current unsorted element.
    variable Arr[j] reresents all the sorted elements on the left of Arr[i].
    
- Step4: Compare all the value of the sorted elements in a reverse order with the current unsorted elements,
 
         - if j >= 0  **(incase we may compare the Arr[-1] with Arr[i])** 
 
         - and if Arr[j] > Arr[i], move Arr[j] to the positiion of j + 1, equals to Arr[j + 1] = Arr[j], 
 
         - and Arr[j] would be None.
          
          - iterate varible j -= 1
      
- Step5: repeat step 4 and then return Arr

## Coding Practice
### Run time complexity is O(N^2)
```
def inSertion(arr):
    *iterate the unsorted numbers which are set as current_number*
    for i in range(1, len(arr)):
        target_num = arr[i]
        j = i - 1
        *iterate the sorted numbers before the current_number*
        *arr[j] is toSort number*
        while j >=0 and arr[j] > target_num:
            arr[j + 1] = arr[j]
            j -= 1
            
        arr[j + 1] = target_num
    return arr

testArray = [4, 1, 2, 5]

print(inSertion(testArray))

```
![image](https://user-images.githubusercontent.com/69109871/149334897-3c1e81cc-a3c6-44fb-a08c-263f5eca735f.png)



