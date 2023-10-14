![image](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/assets/144240022/61376ab7-0abc-4b8c-bb7b-b6cbbe3aa390)# Звіт до роботи
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
seasons = ['Весна', 'Літо', 'Осінь', 'Зима']
print (list(enumerate(seasons, start=1)))
```
   Програма вивела:
```text
<< [(1, 'Весна'), (2, 'Літо'), (3, 'Осінь'), (4, 'Зима')] >>
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
    print(s,'урок закінчився')
    s = s + 1
    if s>6:
         break
print('Кінець уроків')
```
   Програма вивела:
```text
<< 1 урок закінчився
2 урок закінчився
3 урок закінчився
4 урок закінчився
5 урок закінчився
6 урок закінчився
Кінець уроків>>
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

   9.  Приклади Python коду від ChatGPT:
   - вбудовані функції:

  ![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/14.png)

   - код, який демонструє роботу циклів:
    
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/15.png)

   - код, який демонструє роботу розгалужень:
    
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/16.png)

   - код з конструкцією try->except->finally:
    
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/17.png)

   - код з lambdas:
    
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/2_lab/screenshots/18.png)

### Висновок: 
> У цій роботі я навчився користуватися основними конструкціями в Python.

