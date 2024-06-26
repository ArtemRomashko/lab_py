# Лабораторна робота №11: Обробка числових масивів в Python

## Мета роботи:
Мета цієї лабораторної роботи - навчитися обробляти числові масиви в Python, використовуючи різні алгоритми та підходи, такі як обчислення суми квадратів, сортування за частотою, пошук максимальної суми підмасиву тощо.

## Опис завдання:
1. Реалізувати функцію для обчислення суми квадратів елементів масиву.
2. Реалізувати функцію для обчислення суми елементів масиву, що перевищують середнє значення.
3. Реалізувати функцію для сортування елементів масиву за частотою їх появи.
4. Реалізувати функцію для знаходження відсутнього числа у послідовності від 1 до n.
5. Реалізувати функцію для знаходження довжини найдовшої послідовності послідовних чисел.
6. Реалізувати функцію для циклічного зсуву елементів масиву.
7. Реалізувати функцію для обчислення масиву добутків елементів без поточного елемента.
8. Реалізувати функцію для знаходження максимальної суми підмасиву.
9. Реалізувати функцію для обходу матриці за спіраллю.
10. Реалізувати функцію для знаходження k найближчих точок до початку координат.

## Виконання роботи:
### Структура проекту:

### Опис файлів та їх призначення:
- `main.py`: Основний код програми, що містить реалізацію завдань.
- `README.md`: Документ з детальним поясненням роботи.

### Опис основних функцій з поясненням їх роботи:
1. **task1(nums)**:
    - Опис: Обчислює суму квадратів елементів масиву.
    - Вхідні дані: список чисел `nums`.
    - Вихідні дані: сума квадратів чисел.
    - Код:
    ```python
    def task1(nums):
        return sum(x ** 2 for x in nums)
    ```

2. **task2(nums)**:
    - Опис: Обчислює суму елементів масиву, що перевищують середнє значення.
    - Вхідні дані: список чисел `nums`.
    - Вихідні дані: сума елементів, що перевищують середнє значення.
    - Код:
    ```python
    def task2(nums):
        avg = sum(nums) / len(nums)
        return sum(x for x in nums if x >= avg)
    ```

3. **task3(nums)**:
    - Опис: Сортує елементи масиву за частотою їх появи.
    - Вхідні дані: список чисел `nums`.
    - Вихідні дані: відсортований список чисел.
    - Код:
    ```python
    def task3(nums):
        freq = collections.Counter(nums)
        return sorted(nums, key=lambda x: (-freq[x], x))
    ```

4. **task4(nums)**:
    - Опис: Знаходить відсутнє число у послідовності від 1 до n.
    - Вхідні дані: список чисел `nums`.
    - Вихідні дані: відсутнє число.
    - Код:
    ```python
    def task4(nums):
        n = len(nums) + 1
        total = n * (n + 1) // 2
        return total - sum(nums)
    ```

5. **task5(nums)**:
    - Опис: Знаходить довжину найдовшої послідовності послідовних чисел.
    - Вхідні дані: список чисел `nums`.
    - Вихідні дані: довжина найдовшої послідовності.
    - Код:
    ```python
    def task5(nums):
        num_set = set(nums)
        max_length = 0

        for num in num_set:
            if num - 1 not in num_set:
                current_num = num
                current_length = 1

                while current_num + 1 in num_set:
                    current_num += 1
                    current_length += 1

                max_length = max(max_length, current_length)

        return max_length
    ```

6. **task6(nums, k)**:
    - Опис: Виконує циклічний зсув елементів масиву.
    - Вхідні дані: список чисел `nums`, число `k`.
    - Вихідні дані: список чисел після зсуву.
    - Код:
    ```python
    def task6(nums, k):
        k = k % len(nums)
        return nums[-k:] + nums[:-k]
    ```

7. **task7(nums)**:
    - Опис: Обчислює масив добутків елементів без поточного елемента.
    - Вхідні дані: список чисел `nums`.
    - Вихідні дані: список добутків.
    - Код:
    ```python
    def task7(nums):
        left_products = [1]
        right_products = [1]
        result = []

        for i in range(1, len(nums)):
            left_products.append(left_products[-1] * nums[i - 1])

        for i in range(len(nums) - 2, -1, -1):
            right_products.insert(0, right_products[0] * nums[i + 1])

        for i in range(len(nums)):
            result.append(left_products[i] * right_products[i])

        return result
    ```

8. **task8(nums)**:
    - Опис: Знаходить максимальну суму підмасиву.
    - Вхідні дані: список чисел `nums`.
    - Вихідні дані: максимальна сума підмасиву.
    - Код:
    ```python
    def task8(nums):
        max_sum = current_sum = nums[0]

        for num in nums[1:]:
            current_sum = max(num, current_sum + num)
            max_sum = max(max_sum, current_sum)

        return max_sum
    ```

9. **task9(matrix)**:
    - Опис: Обходить матрицю за спіраллю.
    - Вхідні дані: двовимірний список `matrix`.
    - Вихідні дані: список елементів у порядку обходу за спіраллю.
    - Код:
    ```python
    def task9(matrix):
        if not matrix:
            return []

        rows, cols = len(matrix), len(matrix[0])
        result = []

        top = left = 0
        bottom = rows - 1
        right = cols - 1

        while top <= bottom and left <= right:
            for i in range(left, right + 1):
                result.append(matrix[top][i])
            top += 1

            for i in range(top, bottom + 1):
                result.append(matrix[i][right])
            right -= 1

            if top <= bottom:
                for i in range(right, left - 1, -1):
                    result.append(matrix[bottom][i])
                bottom -= 1

            if left <= right:
                for i in range(bottom, top - 1, -1):
                    result.append(matrix[i][left])
                left += 1

        return result
    ```

10. **task10(points, k)**:
    - Опис: Знаходить k найближчих точок до початку координат.
    - Вхідні дані: список точок `points`, число `k`.
    - Вихідні дані: список k найближчих точок.
    - Код:
    ```python
    def task10(points, k):
        return sorted(points, key=lambda x: x[0] ** 2 + x[1] ** 2)[:k]
    ```

### Результати:
Після виконання функцій отримано наступні результати:

task1: Обчислена сума квадратів елементів масиву.
task2: Обчислена сума елементів масиву, що перевищують середнє значення.
task3: Елементи масиву відсортовані за частотою їх появи.
task4: Знайдено відсутнє число у послідовності від 1 до n.
task5: Знайдена довжина найдовшої послідовності послідовних чисел.
task6: Виконано циклічний зсув елементів масиву.
task7: Обчислено масив добутків елементів без поточного елемента.
task8: Знайдена максимальна сума підмасиву.
task9: Матриця обійдена за спіраллю.
task10: Знайдено k найближчих точок до початку координат.

### Висновок:
У результаті виконання лабораторної роботи ми успішно реалізували декілька основних алгоритмів обробки числових масивів у Python. Кожне завдання було вирішено з використанням власної функції, яка відповідає поставленій задачі. Ми використали різні техніки, такі як сортування, використання арифметичних операцій та ітерацій для досягнення бажаного результату.

### Використані ресурси:
Python 3.x
Модуль collections для функції task3