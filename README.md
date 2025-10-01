# Experiment 20 - To study and implement Searching Programs in C++

---

## Aim
- To study and implement fundamental searching algorithms in C++, including **Linear Search** and **Binary Search**.
- To compare their efficiency, time complexity, and respective use cases.

---

## Tools Used
- Visual Studio Code
- MinGW-w64 with g++ Compiler

---

## Theory
**Searching** is the process of finding the location of a specific element (the **key**) within a collection of data. The efficiency of a searching algorithm is a critical aspect of program performance.

### 1. Linear Search
This is the simplest search algorithm. It traverses the array sequentially from the first element to the last, comparing each element with the key.
- **Works on:** Both sorted and unsorted arrays.
- **Time Complexity:** O(n), as in the worst case, it has to check every element.

### 2. Binary Search
This is a highly efficient "divide and conquer" algorithm that works only on **sorted arrays**. It repeatedly divides the search interval in half.
- It compares the key with the middle element.
- If they match, the search is successful.
- If the key is less than the middle element, it narrows the search to the lower half.
- If the key is greater, it narrows the search to the upper half.
- **Time Complexity:** O(log n), as it eliminates half of the remaining elements with each comparison.

| Algorithm | Best Case | Worst Case | Requires Sorted Data? |
| :--- | :---: | :---: | :---: |
| **Linear Search** | O(1) | O(n) | No |
| **Binary Search** | O(1) | O(log n) | Yes |

---

## Algorithm / Logic

### Program 1: Linear Search
1.  **Start**
2.  Prompt the user to input an array and the `key` to be searched.
3.  Use a `for` loop to iterate through each element of the array from index `0` to `n-1`.
4.  Inside the loop, check if `array[i] == key`.
5.  If a match is found, print the index `i` and terminate the search.
6.  If the loop completes without finding the key, print a "Element not found" message.
7.  **End**

### Program 2: Binary Search
1.  **Start**
2.  Prompt the user to input a **sorted** array and the `key` to be searched.
3.  Initialize two pointers: `low = 0` and `high = n-1`.
4.  Use a `while` loop that continues as long as `low <= high`.
5.  Inside the loop, calculate the middle index: `mid = low + (high - low) / 2`.
6.  Compare the element at the middle index with the key:
    - If `array[mid] == key`, the element is found. Print the index `mid` and terminate.
    - If `array[mid] < key`, the key must be in the right half. Update `low = mid + 1`.
    - If `array[mid] > key`, the key must be in the left half. Update `high = mid - 1`.
7.  If the loop finishes, the element is not in the array. Print a "Element not found" message.
8.  **End**

---

## Conclusion
This experiment demonstrated two fundamental searching techniques. **Linear Search** is simple and works on any array but is inefficient for large datasets. **Binary Search** is significantly more efficient but has the prerequisite that the data must be sorted. The choice of algorithm depends on the nature of the data and the performance requirements of the application. Understanding these trade-offs is essential for effective problem-solving in data structures and algorithms.
