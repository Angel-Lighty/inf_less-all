# Ответы на вопросы

1. Почему приведённый в параграфе алгоритм поиска называется двоичным?
   Двоичный поиск называется так потому, что на каждом шаге он делит массив на две равные части. Алгоритм сравнивает искомое значение со значением, находящимся в середине массива, и на следующей итерации продолжает поиск только в одной из получившихся частей, в зависимости от того, больше или меньше искомое значение. Это делает алгоритм очень эффективным для отсортированных массивов, так как количество элементов, которые нужно проверить, уменьшается в два раза с каждой итерацией.

2. Как можно примерно подсчитать количество шагов при двоичном поиске?
   При двоичном поиске количество шагов (итераций) можно выразить с помощью логарифма. Для массива из n элементов, максимальное количество шагов можно подсчитать по формуле log2(n). Например, для 32 элементов это будет равно log2(32) = 5. Это значит, что максимальное количество сравнений, необходимое для нахождения элемента, составляет 5. Более формально, при каждом делении массива мы уменьшаем количество оставшихся элементов в два раза.


### Задачи
```
1. Программа, сортирующая массив по убыванию и ищущая значения, равные заданному числу

def sort_and_find(arr, target):
    sorted_arr = sorted(arr, reverse=True)
    found_indices = [i for i, x in enumerate(sorted_arr) if x == target]
    return sorted_arr, found_indices

Пример использования
arr = [3, 5, 1, 4, 2, 5, 3]
target = 3
sorted_arr, indices = sort_and_find(arr, target)
print("Отсортированный массив по убыванию:", sorted_arr)
print("Индексы найденных значений", target, ":", indices)


2. Программа для подсчета среднего числа шагов при двоичном поиске

import random
import math

def binary_search(arr, target):
    low, high, steps = 0, len(arr) - 1, 0
    while low <= high:
        mid = (low + high) // 2
        steps += 1
        if arr[mid] == target:
            return steps
        elif arr[mid] < target:
            high = mid - 1
        else:
            low = mid + 1
    return steps  # Вернём количество шагов (не найдено)

def average_binary_search_steps(array_size, search_range, num_trials):
    total_steps = 0
    for _ in range(num_trials):
        target = random.randint(0, search_range)
        arr = sorted(random.sample(range(search_range + 1), array_size))  # Генерация отсортированного массива
        steps = binary_search(arr, target)
        total_steps += steps
    return total_steps / num_trials

Пример использования
array_size = 32
search_range = 100
num_trials = 1000
average_steps = average_binary_search_steps(array_size, search_range, num_trials)
print("Среднее число шагов при двоичном поиске:", average_steps)
