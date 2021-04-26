# Bubble sort algorithm

with Python

```python
import random

def create_random_arrey(n,x,y):
    my_list = [random.randint(x, y) for i in range(n)]

    return my_list


def bubble_sort_algorithm_v_1(my_list):

    counter = 0
    swapped = True
    while swapped:
        counter += 1
        swapped = False
        for j in range(1,len(my_list)):
            if my_list[j - 1] > my_list[j]:
                my_list[j-1], my_list[j] = my_list[j], my_list[j-1]
                swapped = True

    print(f"Looped {counter} times through the list when sorting the {len(my_list)} long list")


def bubble_sort_algorithm_v_2(my_list):

    for j in range(1,len(my_list)):
        for i in range(1,len(my_list)):
            if my_list[i -1] > my_list[i]:
                my_list[i - 1], my_list[i] = my_list[i], my_list[i - 1]

my_list = create_random_arrey(14,1,20)
print("Random list: ",my_list)

bubble_sort_algorithm_v_1(my_list)
print("Sorted list v 1: ", my_list)

bubble_sort_algorithm_v_2(my_list)
print("Sorted list v 2: ",my_list)
```
