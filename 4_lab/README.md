# Звіт до роботи
## Тема: _Віртуальні середовища_
### Мета роботи: _Навчитися працювати у віртуальному середовищі_
---
### Виконання роботи
    1. За допомогою команди pip -V перевірив і переконався, що PIP (Python Install Package) встановлений на моєму комп'ютері.
    Після успішного виконання команди виконав:
```text
pip -heip
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/1.png)
 
    2. Встановив бібліотеку requests:
```text
pip install requests
python #Зайшов у пайтон інтерпретатор
>>> import requests
>>> r = requests.get('https://google.com')
>>> r.status_code
>>> exit()
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/2.png)

    3. Виконав такі команди:
```text
pip show requests
pip install requests==2.1
pip show requests
pip uninstall requests
```
    Результат виконання команд:
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/3.png)

    4. Для створення VENV та його активації виконав команди:
```text
python -m venv ./my_env
source my_env/Scripts/activate
pip install requests
deactivate
pip show requests
```
    Остання команда вивела:
   ![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/5.png)
    











    
```python
 ??? Why {MyName.total_names}?")

```
   Програма вивела:
```text
<< Let's Start!
We are done. We create 4 names! ??? Why 4? >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/3_lab/screenshots/1.png)

    3. Ознайомився з кодом, розібрався, за що відповідає кожен з рядків.
    4. Модифікував програму, додавши своє ім’я в список:

![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/3_lab/screenshots/2.png)

   5. Відповіді на запитання:
      
   A. Чому, коли передаємо значення None, створюється об`єкт з іменем Anonymous?
   Коли передаємо значення None, створюється об`єкт з іменем Anonymous вiдповідно до коду:
   self.name = name if name is not None else self.anonymous_user().name #Class attributes / Instance variables

   B. Як змінити текст привітання при виклику методу say_hello()? Допишіть цю частину коду.
   
   ```python
This is static {type(MyName.say_hello)} with my prompt: {me.say_hello("Привіт!")}
```

   C. Допишіть функцію в класі, яка порахує кількість букв в імені.
   
   ```python
    def name_length(self):
        return len(self.name)

The number of letters in the name: {me.name_length()}
```
    Програма вивела:
```text
<< Let's Start!

We are done. We create 5 names! ??? Why 5? >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/3_lab/screenshots/3.png)
 
   D. Порахуйте кількість імен у списку names та порівняйте із виведеним результатом. Дайте відповідь, чому маємо різну кількість імен?
   У виведеному результаті кількість імен більша, тому що у списку присутній user None. 
   У конструкторі класу, якщо name is None, метод anonymous_user() створює ще один об’єкт.
   
### Висновок: 
> У цій роботі я навчився встановлювати сторонні бібліотеки, працювати у віртуальному середовищі: працювати з Pipenv, параметризувати середовища за допомогою змінних середовища. 
