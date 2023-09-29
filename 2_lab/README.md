# Звіт до роботи
## Тема: _Основи програмування на Python. Основні конструкції в Python_
### Мета роботи: _Навчитися користуватися основними конструкціями в Python_
---
### Виконання роботи
    Створив у Python файл і, застосовуючи команду print, виконав коди.
    1. Познайомився з основними типами даних
```a = "Перемога"
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
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/1.png)

    4. Створив файл my_first_app.ipynb та скопіював в нього код програми, запустив програму;
```python
from datetime import datetime
name = "Olexandr"
location = "Lviv"

print(f"{name} start programming at {datetime.now()}. {location} is the best city!")
```
    5. Програма вивела:
```text
<< Olexandr start programming at 2023-09-16 20:06:03.793422. Lviv is the best city >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/2.png)

   6. Створив файл my_first_app.md, написав код програми, запустив програму;
```python
from datetime import datetime
name = "Олександр"
location = "Львів"

print(f"{name} створив першу свою програму {datetime.now()} у місті {location}")
```
 7. Програма вивела:
```text
<< Олександр створив першу свою програму 2023-09-19 15:20:34.540359 у місті Львів>>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/3.png)
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/4.png)
### Висновок: 
> У цій роботі я навчився завантажувати роботи у репозиторій.

