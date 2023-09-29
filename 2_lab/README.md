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
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/1.png)

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
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/2.png)

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
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/3.png)

   3. Вивів результат роботи вбудованих функцій:
   - abs(x) - повертає абсолютне значення числа
  ```python
print(abs(-5), f"є рівним {abs(5)}")
```
   Програма вивела:
```text
<< 5 є рівним 5>>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/blob/main/1_lab/4.png)

### Висновок: 
> У цій роботі я навчився завантажувати роботи у репозиторій.

