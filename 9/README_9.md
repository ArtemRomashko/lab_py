# Лабораторна робота №9: Перевірка вхідних даних за допомогою регулярних виразів

## Мета роботи:
Мета цієї лабораторної роботи - навчитися використовувати регулярні вирази для перевірки вхідних даних на відповідність певним шаблонам, що часто зустрічаються в реальних задачах.

## Опис завдання:
1. Перевірити, чи рядок складається лише з двох символів (літери або цифри), які повторюються.
2. Перевірити, чи рядок містить лише великі літери.
3. Перевірити, чи рядок є правильною IP-адресою v4.
4. Перевірити, чи рядок є правильним часом у форматі HH:MM:SS.
5. Перевірити, чи рядок є правильним поштовим індексом США.
6. Перевірити, чи рядок є правильним іменем користувача (6-12 символів, лише малі літери, цифри, підкреслення та дефіси).
7. Перевірити, чи рядок є правильною кредитною карткою (починається з 4, 5 або 6 і складається з 16 цифр, дозволені пробіли або дефіси).
8. Перевірити, чи рядок є правильним номером соціального страхування США (SSN).
9. Перевірити, чи рядок є надійним паролем (мінімум 8 символів, містить великі та малі літери, цифри та спеціальні символи).
10. Перевірити, чи рядок є правильною IP-адресою v6.

## Виконання роботи:
### Структура проекту:


### Опис файлів та їх призначення:
- `main.py`: Основний код програми, що містить реалізацію завдань.
- `README.md`: Документ з детальним поясненням роботи.

### Опис основних функцій та методів з поясненням їх роботи:
1. **task1(i)**:
    - Опис: Перевіряє, чи рядок складається лише з двох символів (літери або цифри), які повторюються.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

2. **task2(i)**:
    - Опис: Перевіряє, чи рядок містить лише великі літери.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

3. **task3(i)**:
    - Опис: Перевіряє, чи рядок є правильною IP-адресою v4.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

4. **task4(i)**:
    - Опис: Перевіряє, чи рядок є правильним часом у форматі HH:MM:SS.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

5. **task5(i)**:
    - Опис: Перевіряє, чи рядок є правильним поштовим індексом США.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

6. **task6(i)**:
    - Опис: Перевіряє, чи рядок є правильним іменем користувача.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

7. **task7(i)**:
    - Опис: Перевіряє, чи рядок є правильною кредитною карткою.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

8. **task8(i)**:
    - Опис: Перевіряє, чи рядок є правильним номером соціального страхування США (SSN).
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

9. **task9(i)**:
    - Опис: Перевіряє, чи рядок є надійним паролем.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

10. **task10(i)**:
    - Опис: Перевіряє, чи рядок є правильною IP-адресою v6.
    - Аргументи:
        - `i`: вхідний рядок.
    - Повертає: `True`, якщо рядок відповідає умовам, інакше `False`.

### Приклади використання:
```python
# Приклад використання task1
result1 = task1('aa11bb22')
print(result1)  # True

# Приклад використання task2
result2 = task2('HELLO')
print(result2)  # True

# Приклад використання task3
result3 = task3('192.168.1.1')
print(result3)  # True

# Приклад використання task4
result4 = task4('23:59:59')
print(result4)  # True

# Приклад використання task5
result5 = task5('12345-6789')
print(result5)  # True

# Приклад використання task6
result6 = task6('username_1')
print(result6)  # True

# Приклад використання task7
result7 = task7('4111-1111-1111-1111')
print(result7)  # True

# Приклад використання task8
result8 = task8('123-45-6789')
print(result8)  # True

# Приклад використання task9
result9 = task9('Password1@')
print(result9)  # True

# Приклад використання task10
result10 = task10('2001:0db8:85a3:0000:0000:8a2e:0370:7334')
print(result10)  # True

### Результати:
Після виконання функцій отримано наступні результати:

Для task1: повернуто список імен, які відповідають умовам.
Для task2: дані успішно записані у JSON файл.
Для task3: визначено невалідні JSON файли.
Для task4: витягнуті всі значення заданого ключа.
Для task5: оновлені певні елементи у JSON файлі.

### Висновки:
Мета роботи була досягнута. Було успішно виконано всі поставлені завдання з обробки JSON файлів. Проблеми, які виникли під час виконання, були вирішені шляхом детального аналізу і використання стандартних методів роботи з JSON у Python.

### Інструкції з запуску:
Вимоги до середовища:
- Python 3.x
- Бібліотека re (стандартна бібліотека Python)