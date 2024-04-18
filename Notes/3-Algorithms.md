# Week 3 Algorithms
## Linear Search
- **Definition**：A linear search sequentially checks each element of the list until it finds an element that matches the target value。
- **Cost**： On average, this algorithm has a Big-O runtime of O(N)

- **Example**: find 50
```
For each i from 0 to n-1:
    If doors[i] == 50:
        return true
return false
```

## Binary Search

- **Definition**: Binary search works on sorted arrays. Binary search conpares the middle and the target value. Then iterates for the left or right half middle comparision until find the matches.

- **Cost**: O(logN)

- **Example**: find 50
```
If no doors left
    return false
If doors[middle] == 50:
    return true
Else if 50 < doors[middle]:
    search doors[0] through doors[middle -1]
Else if 50 > doors[middle]:
    search doors[middle+1] through doors[n-1]
```

## Running time

- running time involves an analysis using big O notation.

- The $\Omega$ symbol is used to denote the best case of an algorithm, such as $\Omega (log\ n)$

- The $\Theta$ symbol is used to denote where the upper bound and lower bound are the same, where the best case and the worst case running times are the same.

## Data Structures
- C allows a way by which we can create our own data types via `struct`.
- 
```C
typedef struct
{
    string name;
    string number;
}
person;

int main(void)
{
    person people[3];

    people[0].name = "Carter";
    people[0].number = "+1-617-495-1000";
}
```

## Sorting

### Selection Sort
- 
```
For i from 0 to n–1
    Find smallest number between numbers[i] and numbers[n-1]
    Swap smallest number with numbers[i]
```
- Time: 
    - $(n-1)+(n-2)+...+1$
    - $n(n-1)/2$ or, more simply, $O(n^2)$
    - $\Omega(n^2)$ and $\Theta(n^2)$ since it always do the loop for n times

### Bubble Sort
- 
```
Repeat n-1 times
    For i from 0 to n–2
        If numbers[i] and numbers[i+1] out of order
            Swap them
    If no swaps
        Quit
```
- Time: 
    - $(n-1)(n-1)$
    - $O(n^2)$
    - Best case $\Omega(n)$, worst case $\Theta(n^2)$, as if the first time no swap, it quit and no more loop

### Merge Sort
- 
```
If only one number
    Quit
Else
    Sort left half of number
    Sort right half of number
    Merge sorted halves
```
- Time:
    - $O(n\log n)$
    - Best case $\Omega(n\log n)$, worst case $\Theta(n\log n)$

## Recursion
- *Recursion* is a concept within programming where a function calls itself. 
- **Always need to tell the program to end, otherwise will has infinite loop**
