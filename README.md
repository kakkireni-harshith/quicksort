# quicksort
def quick_sort(arr):
    if len(arr) <= 1:
        return arr
    
    pivot = arr.pop()  # Choose the last element as the pivot
    left = []
    right = []

    for element in arr:
        if element <= pivot:
            left.append(element)
        else:
            right.append(element)

    return quick_sort(left) + [pivot] + quick_sort(right)

# Example usage:
arr = [64, 34, 25, 12, 22, 11, 90]
sorted_arr = quick_sort(arr)
print("Sorted Array:", sorted_arr)
