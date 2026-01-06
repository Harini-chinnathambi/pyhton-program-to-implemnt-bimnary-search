PROGRAM:

def binarySearch(numbers, low, high, x):
    if high >= low:
        mid = low + (high - low) // 2  
        if numbers[mid] == x:
            return mid
        elif numbers[mid] > x:
            return binarySearch(numbers, low, mid - 1, x) 
        else:
            return binarySearch(numbers, mid + 1, high, x)  
    else:
        return -1  


numbers = [9, 4, 6, 7, 2, 1, 5]
numbers.sort() 
x = 7 
result = binarySearch(numbers, 0, len(numbers) - 1, x)
if result != -1:
    print(f"Search successful, element {x} found at position {result}.")
else:
    print("The given element is not present in the array.")



OUTPUT:

Search successful, element 7 found at position 5

