# python-algorithms
### -> Binary Search 
The function takes a sorted array and an item as input then returns the index of the item as output in logarithmic time.
```py
def binary_search(list, item):
    low = 0
    high = len(list) - 1 

    while low <= high:
        mid = (low + high)
        guess = list[mid]
        if guess == item:
            return mid
        if guess > item:
            high = mid - 1
        else:
            low = mid + 1
    return None
```