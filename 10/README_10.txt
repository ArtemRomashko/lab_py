# Лабораторна робота №10: Об'єктно-орієнтоване програмування в Python

## Мета роботи:
Мета цієї лабораторної роботи - навчитися використовувати основні концепції об'єктно-орієнтованого програмування (ООП) в Python, такі як класи, спадкування, інкапсуляція та поліморфізм.

## Опис завдання:
1. Створити клас `Student` з атрибутами `name`, `age` та `grade`, а також методом для виведення інформації про студента.
2. Створити клас `Animal` з атрибутами `name` та `sound`, а також методом для відтворення звуку.
3. Створити клас `Dog`, який успадковує клас `Animal` та додає атрибут `breed`.
4. Створити ієрархію класів `Bird`, `Sparrow` та `Penguin` з методом `fly`, який реалізує поліморфізм.
5. Створити клас `Encapsulation`, який демонструє різні рівні доступу до атрибутів.
6. Створити клас `Rectangle` з методами для обчислення периметра.
7. Створити клас `AverageCalculator` з методом для обчислення середнього значення чисел.

## Виконання роботи:
### Структура проекту:


### Опис файлів та їх призначення:
- `main.py`: Основний код програми, що містить реалізацію завдань.
- `README.md`: Документ з детальним поясненням роботи.

### Опис основних класів та методів з поясненням їх роботи:
1. **Клас `Student`**:
    - Опис: Зберігає інформацію про студента.
    - Атрибути:
        - `name`: Ім'я студента.
        - `age`: Вік студента.
        - `grade`: Оцінка студента.
    - Методи:
        - `display_info()`: Повертає рядок з інформацією про студента.

    ```python
    class Student:
        def __init__(self, name, age, grade):
            self.name = name
            self.age = age
            self.grade = grade
        
        def display_info(self):
            return f"Name: {self.name}, Age: {self.age}, Grade: {self.grade}"
    ```

2. **Клас `Animal`**:
    - Опис: Зберігає інформацію про тварину.
    - Атрибути:
        - `name`: Ім'я тварини.
        - `sound`: Звук, який видає тварина.
    - Методи:
        - `make_sound()`: Повертає рядок зі звуком тварини.

    ```python
    class Animal:
        def __init__(self, name, sound):
            self.name = name
            self.sound = sound
        
        def make_sound(self):
            return f"{self.name}: {self.sound}"
    ```

3. **Клас `Dog`** (успадковує `Animal`):
    - Опис: Додає атрибут породи до класу `Animal`.
    - Атрибути:
        - `breed`: Порода собаки.
    
    ```python
    class Dog(Animal):
        def __init__(self, name, sound, breed):
            super().__init__(name, sound)
            self.breed = breed
    ```

4. **Класи `Bird`, `Sparrow`, `Penguin`**:
    - Опис: Демонстрація поліморфізму через метод `fly()`.
    - Методи:
        - `fly()`: Повертає рядок з інформацією про здатність літати.

    ```python
    class Bird:
        def fly(self):
            return None

    class Sparrow(Bird):
        def fly(self):
            return "Sparrow flies high"

    class Penguin(Bird):
        def fly(self):
            return "Penguin cannot fly"
    ```

5. **Клас `Encapsulation`**:
    - Опис: Демонструє інкапсуляцію з різними рівнями доступу до атрибутів.
    - Атрибути:
        - `public`: Публічний атрибут.
        - `_private`: Приватний атрибут (пропонований до приховування).
        - `__protected`: Захищений атрибут (псевдо-захищений).

    ```python
    class Encapsulation:
        def __init__(self, public, _private, __protected):
            self.public = public
            self._private = _private
            self.__protected = __protected
    ```

6. **Клас `Rectangle`**:
    - Опис: Обчислює периметр прямокутника.
    - Атрибути:
        - `width`: Ширина прямокутника.
        - `height`: Висота прямокутника.
    - Методи:
        - `calculate_perimeter()`: Повертає периметр прямокутника.

    ```python
    class Rectangle:
        def __init__(self, width, height):
            self.width = width
            self.height = height

        def calculate_perimeter(self):
            return self.width*2 + self.height*2
    ```

7. **Клас `AverageCalculator`**:
    - Опис: Обчислює середнє значення чисел.
    - Атрибути:
        - `numbers`: Список чисел.
    - Методи:
        - `calculate_average()`: Повертає середнє значення чисел.

    ```python
    class AverageCalculator:
        def __init__(self, numbers):
            self.numbers = numbers

        def calculate_average(self):
            return sum(self.numbers) / len(self.numbers)
    ```

### Приклади використання:
```python
# Приклад використання класу Student
student = Student("John", 21, "A")
print(student.display_info())

# Приклад використання класу Animal і Dog
dog = Dog("Buddy", "Woof", "Golden Retriever")
print(dog.make_sound())

# Приклад використання класів Sparrow і Penguin
sparrow = Sparrow()
penguin = Penguin()
print(sparrow.fly())
print(penguin.fly())

# Приклад використання класу Encapsulation
encapsulation = Encapsulation("public", "private", "protected")
print(encapsulation.public)
print(encapsulation._private)

# Приклад використання класу Rectangle
rectangle = Rectangle(5, 10)
print(rectangle.calculate_perimeter())

# Приклад використання класу AverageCalculator
calculator = AverageCalculator([1, 2, 3, 4, 5])
print(calculator.calculate_average())

### Результати:
Після виконання функцій отримано наступні результати:

Для класу Student: успішно створений об'єкт та відображена інформація про студента.
Для класу Animal та його нащадка Dog: успішно створений об'єкт та відтворений звук тварини.
Для класів Bird, Sparrow та Penguin: демонстрація поліморфізму у методі fly().
Для класу Encapsulation: продемонстровано різні рівні доступу до атрибутів.
Для класу Rectangle: успішно обчислений периметр прямокутника.
Для класу AverageCalculator: успішно обчислене середнє значення чисел.

### Висновки:
Мета роботи була досягнута. Було успішно виконано всі поставлені завдання з використанням об'єктно-орієнтованого підходу в Python. Проблеми, які виникли під час виконання, були вирішені шляхом детального аналізу та використання принципів ООП.

### Інструкції з запуску:
Вимоги до середовища:
Python 3.x