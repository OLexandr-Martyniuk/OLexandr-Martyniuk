# Звіт до роботи
## Тема: _Основи програмування на Python. Основні конструкції в Python_
### Мета роботи: _Навчитися користуватися основними конструкціями в Python_
---
### Виконання роботи
    Створив у Python файл і, застосовуючи команду print, виконав коди.
    1. Познайомився з основними типами даних:
```python
a = "Перемога"
b = 1 # числова змінна
c = ["a", 1, 1.25, "Перемога"] # List
d = {"a": "Перемога", "b": 1} # Dict
e = ("a", ) # Tuple
f = {"ss", } # Set
print (a)
print (b+b)
c.remove (1)
print (c)
d.update(g=3, h=4)
print (d)
print (e)
print (f)
```
   Програма вивела:
```text
<< Перемога
2
['a', 1.25, 'Перемога']
{'a': 'Перемога', 'b': 1, 'g': 3, 'h': 4}
('a',)
{'ss'} >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/1.png)

    2. Вивів вбудовані константи:
```python
def print_some(value=None):
    value = value or 'some'  # Якщо значення не передано, використовуємо some.
    print(value)

print_some() # some
```
    Програма вивела:
```text
<< some >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/2.png)

```python
def is_it_true(anything):
 if anything:
   print("yes, it's true")
 else:
   print("no, it's false")

print (is_it_true(None))
print (is_it_true(not None))
```
    Програма вивела:
```text
<< no, it's false
None
yes, it's true     
None >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/3.png)

   3. Вивів результат роботи вбудованих функцій:
   - abs(x) - повертає абсолютне значення числа
  ```python
print(abs(-5), f"є рівним {abs(5)}")
```
   Програма вивела:
```text
<< 5 є рівним 5 >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/4.png)

  - bin(x) - перетворення цілого числа на двійковий рядок із префіксом «0b»
  ```python
print(bin(3))
```
   Програма вивела:
```text
<< 0b11 >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/5.png)

 - enumerate - повертає об’єкт перерахування
  ```python
seasons = ['Spring', 'Summer', 'Fall', 'Winter']
print (list(enumerate(seasons, start=1)))
```
   Програма вивела:
```text
<< [(1, 'Spring'), (2, 'Summer'), (3, 'Fall'), (4, 'Winter')] >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/6.png)

 4.  Напиcав коди, які демонструють роботу циклів:
 ```python
programming_languages = ["Python", "JavaScript", "Java", "C++"]
for language in programming_languages:
  print(language)
```
   Програма вивела:
```text
<< Python
JavaScript
Java
C++ >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/7.png)

 ```python
i = 0
while i < 10:
    print(i)
    i = i + 1
```
  Програма вивела:
```text
<< 1
2
3
4
5
6
7
8
9 >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/8.png)

 5.  Напиcав коди, які демонструють роботу розгалуження:
 ```python
age = 17
if age > 18:
   print('Ти повнолітній')
else:
   print('ти не повнолітній')
```
   Програма вивела:
```text
<< Ти не повнолітній>>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/9.png)

 ```python
s = 1
while True:
    print(s,'lesson has already passed')
    s = s + 1
    if s>6:
         break
print('End of lessons')
```
   Програма вивела:
```text
<< 1 lesson has already passed
2 lesson has already passed
3 lesson has already passed
4 lesson has already passed
5 lesson has already passed
6 lesson has already passed
End of lessons>>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/10.png)

 6.  Конструкція try->except->finally. Код з помилкою:
 ```python
my_dict = {"a":1, "b":2, "c":3}
 
try:
    value = my_dict["d"]
except KeyError:
    print("Помилка ключа зіставлення!")
finally:
    print("Інструкцію виконано!")
```
   Програма вивела:
```text
<< Помилка ключа зіставлення!
Інструкцію виконано!>>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/11.png)

 7.  Написав код контекст-мeнеджером with:
 ```python
with open("file.txt", "r") as file:
    content = file.read()
    print(content)
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/12.png)
  
 8.  Написав код з lambdas:
 ```python
full_name = lambda first, last: f'Мене звати {first.title()} {last.title()}'
print(full_name ('Олександр', 'Мартинюк'))
```
   Програма вивела:
```text
<<Мене звати Олександр Мартинюк>>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/13.png)

### Висновок: 
> У цій роботі я навчився користуватися основними конструкціями в Python.

