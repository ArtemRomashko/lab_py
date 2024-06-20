# Лабораторна робота №17: Генератори в Python

## Мета роботи:
Коротко опишіть мету лабораторної роботи та очікувані результати.

Метою лабораторної роботи є створення різноманітних генераторів для роботи з числами, структурами даних та послідовностями, а також вивчення їх використання в Python. Очікується, що створені генератори будуть коректно працювати та демонструвати їхню ефективність у відповідних випадках використання.

## Опис завдання:
Детально опишіть завдання, яке потрібно виконати.

Реалізувати набір генераторів для різних типів обробки даних у Python:

1. Генератори чисел:
   - `number_generator(num)`: генератор для послідовності чисел зі списку `num`.
   - `even_number_generator(start, end)`: генератор парних чисел від `start` до `end`.
   - `odd_number_generator(start, end)`: генератор непарних чисел від `start` до `end`.
   - `fibonacci_generator()`: генератор чисел Фібоначчі.
   - `prime_number_generator(limit)`: генератор простих чисел до `limit`.

2. Генератори обходу дерев та графів:
   - Клас `TreeNode` для створення вузлів бінарного дерева.
   - `pre_order_traversal(root)`: префіксний обхід бінарного дерева.
   - `in_order_traversal(root)`: інфіксний обхід бінарного дерева.
   - `post_order_traversal(root)`: постфіксний обхід бінарного дерева.
   - `dfs_traversal(graph, start)`: пошук в глибину в графі.
   - `bfs_traversal(graph, start)`: пошук в ширину в графі.

3. Генератори роботи зі словниками та файлами:
   - `dict_keys_generator(d)`: генератор ключів словника `d`.
   - `dict_values_generator(d)`: генератор значень словника `d`.
   - `dict_items_generator(d)`: генератор пар (ключ, значення) словника `d`.
   - `file_lines_generator(file_path)`: генератор рядків з файлу `file_path`.
   - `file_words_generator(file_path)`: генератор слів з файлу `file_path`.

4. Інші генератори:
   - `string_chars_generator(string)`: генератор символів з рядка `string`.
   - `unique_elements_generator(lst)`: генератор унікальних елементів списку `lst`.
   - `reverse_list_generator(lst)`: генератор елементів списку `lst` у зворотному порядку.
   - `cartesian_product_generator(lst1, lst2)`: генератор декартового добутку двох списків.
   - `permutations_generator(lst)`: генератор перестановок списку `lst`.
   - `combinations_generator(lst)`: генератор комбінацій списку `lst`.
   - `tuple_list_generator(lst)`: генератор елементів кортежу зі списку кортежів `lst`.
   - `parallel_lists_generator(*lists)`: генератор паралельних значень зі списку списків.
   - `flatten_list_generator(nested_list)`: генератор елементів вкладеного списку `nested_list`.
   - `nested_dict_generator(nested_dict)`: генератор елементів вкладеного словника `nested_dict`.
   - `powers_of_two_generator(n)`: генератор степенів числа 2 до `n`.
   - `powers_of_base_generator(base, limit)`: генератор степенів бази `base` до `limit`.
   - `squares_generator(start, end)`: генератор квадратів чисел від `start` до `end`.
   - `cubes_generator(start, end)`: генератор кубів чисел від `start` до `end`.
   - `factorials_generator(n)`: генератор факторіалів чисел до `n`.
   - `collatz_sequence_generator(n)`: генератор послідовності Коллатца для числа `n`.
   - `geometric_progression_generator(initial, common_ratio, limit)`: генератор геометричної прогресії.
   - `arithmetic_progression_generator(initial, common_diff, limit)`: генератор арифметичної прогресії.
   - `running_sum_generator(lst)`: генератор накопичувальної суми списку `lst`.
   - `running_product_generator(lst)`: генератор накопичувального добутку списку `lst`.

## Виконання роботи:
Опишіть кроки, які були виконані для досягнення мети. Включіть наступну інформацію:

- Кожна лабораторна робота завантажена в окрему папку на GitHub.
- Назва папки відповідає номеру лабораторної роботи.
- В папці мають бути наступні файли:
  - Основний код програми (main.py).
  - README файл з детальним поясненням.
  - Структура проекту.
  - Опис кожного файлу та його призначення.
  - Опис основних функцій та методів з поясненням їх роботи.
  - Приклади використання.

## Результати:
Опишіть отримані результати та додайте скріншоти або приклади виводу програми.

### Приклад використання генератора перестановок:
```python
from generators import permutations_generator

input_list = ['a', 'b', 'c']
permutations = permutations_generator(input_list)

for perm in permutations:
    print(perm)
('a', 'b', 'c')
('a', 'c', 'b')
('b', 'a', 'c')
('b', 'c', 'a')
('c', 'a', 'b')
('c', 'b', 'a')

### Висновки:
Коротко підведіть підсумки, чи була досягнута мета роботи, які проблеми виникли та як вони були вирішені.