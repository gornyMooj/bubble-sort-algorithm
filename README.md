# Bubble sort algorithm

with Python

```python
import random

def create_random_arrey(n,x,y):
    my_list = [random.randint(x, y) for i in range(n)]

    return my_list


def bubble_sort_algorithm_v_1(my_list):

    swapped = True
    while swapped:
        swapped = False
        for j in range(1,len(my_list)):
            if my_list[j - 1] > my_list[j]:
                my_list[j-1], my_list[j] = my_list[j], my_list[j-1]
                swapped = True

   

def bubble_sort_algorithm_v_2(my_list):

        for j in range(len(my_list), 1, -1):
            for i in range(1,j):
                if my_list[i -1] > my_list[i]:
                    my_list[i - 1], my_list[i] = my_list[i], my_list[i - 1]
                
                

my_list = create_random_arrey(14,1,20)
print("Random list: ",my_list)

bubble_sort_algorithm_v_1(my_list)
print("Sorted list v 1: ", my_list)

bubble_sort_algorithm_v_2(my_list)
print("Sorted list v 2: ",my_list)
```
