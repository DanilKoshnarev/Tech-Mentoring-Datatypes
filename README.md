# Алгоритми та Структури Даних

Цей репозиторій допоможе вам зрозуміти основні алгоритми та структури даних і їхню реалізацію на мовах Python, C++ та Go.

## Зміст
1. Вступ до алгоритмів та структур даних
2. Базові структури даних
3. Основні алгоритми
4. Приклади коду


## Вступ до алгоритмів та структур даних
Алгоритми та структури даних є основою комп'ютерних наук і програмування. Вони допомагають ефективно зберігати, обробляти і маніпулювати даними.

## Базові структури даних
- **Масиви**: Колекції елементів з доступом по індексу.
- **Списки**: Послідовності елементів з динамічним розміром.
- **Черги**: Структури даних з принципом FIFO (First In, First Out).
- **Стеки**: Структури даних з принципом LIFO (Last In, First Out).
- **Дерева**: Ієрархічні структури даних.
- **Хеш-таблиці**: Структури даних для швидкого доступу до елементів за ключем.

## Основні алгоритми
- **Сортування**: Алгоритми упорядкування елементів масиву або списку.
  - Bubble Sort
  - Quick Sort
  - Merge Sort
- **Пошук**: Алгоритми знаходження елементів в структурах даних.
  - Linear Search
  - Binary Search

## Приклади коду
### Python
```python
# Quick Sort
def quicksort(arr):
    if len(arr) <= 1:
        return arr
    pivot = arr[len(arr) // 2]
    left = [x for x in arr if x < pivot]
    middle = [x for x in arr if x == pivot]
    right = [x for x in arr if x > pivot]
    return quicksort(left) + middle + quicksort(right)
```
### C++
```c++
// Quick Sort
#include <vector>

void quicksort(std::vector<int>& arr, int low, int high) {
    if (low < high) {
        int pivot = partition(arr, low, high);
        quicksort(arr, low, pivot - 1);
        quicksort(arr, pivot + 1, high);
    }
}

int partition(std::vector<int>& arr, int low, int high) {
    int pivot = arr[high];
    int i = low - 1;
    for (int j = low; j < high; ++j) {
        if (arr[j] < pivot) {
            ++i;
            std::swap(arr[i], arr[j]);
        }
    }
    std::swap(arr[i + 1], arr[high]);
    return i + 1;
}
```
### Go
```
// Quick Sort
package main

import "fmt"

func quicksort(arr []int) []int {
    if len(arr) <= 1 {
        return arr
    }
    pivot := arr[len(arr)/2]
    left := []int{}
    middle := []int{}
    right := []int{}
    for _, x := range arr {
        if x < pivot {
            left = append(left, x)
        } else if x == pivot {
            middle = append(middle, x)
        } else {
            right = append(right, x)
        }
    }
    return append(append(quicksort(left), middle...), quicksort(right),middle...)
```
## Про мене
Привіт! Мене звати **Кошнарьов Данил**, я софтвер девелопер та розробник ПО. Моя мета - допомогти вам освоїти тестування та верифікацію програмного забезпечення та стати кращими програмістами.

## Зворотний зв'язок
Якщо у вас є питання чи пропозиції, не соромтеся зв'язатися зі мною.

