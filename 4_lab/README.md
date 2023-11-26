# Звіт до роботи
## Тема: _Віртуальні середовища_
### Мета роботи: _Навчитися працювати у віртуальному середовищі_
---
### Виконання роботи
    1. Створив два python файли: lab_3.ipynb та lab_3.py.
    2. Скопіював Python код у ці файли і виконав їх, натиснувши Run Python File:
```python
class MyName:
    """Опис класу / Документація
    """
    total_names = 0 #Class Variable

    def __init__(self, name=None) -> None:
        self.name = name if name is not None else self.anonymous_user().name #Class attributes / Instance variables
        MyName.total_names += 1 #modify class variable
        self.my_id = self.total_names

    @property
    def whoami(self): 
        """Class property
        return: повертаємо імя 
        """
        return f"My name is {self.name}"
    
    @property
    def my_email(self) -> str:
        """Class property
        return: повертаємо емейл
        """
        return self.create_email()
    
    def create_email(self) -> str:
        """Instance method
        """
        return f"{self.name}@itcollege.lviv.ua"

    @classmethod
    def anonymous_user(cls):
        """Classs method
        """
        return cls("Anonymous")
    
    @staticmethod
    def say_hello(message="Hello to everyone!"):
        """Static method
        """
        return f"You say: {message}"


print("Let's Start!")

names = ("Bohdan", "Marta", None)
all_names = {name: MyName(name) for name in names}

for name, me in all_names.items():
    print(f"""{">*<"*20}
This is object: {me} 
This is object attribute: {me.name} / {me.my_id}
This is {type(MyName.whoami)}: {me.whoami} / {me.my_email}
This is {type(me.create_email)} call: {me.create_email()}
This is static {type(MyName.say_hello)} with defaults: {me.say_hello()} 
This is class variable {type(MyName.total_names)}: from class {MyName.total_names} / from object {me.total_names}
{"<*>"*20}""")

print(f"We are done. We create {me.total_names} names! ??? Why {MyName.total_names}?")

```
   Програма вивела:
```text
<< Let's Start!
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x7f5eee92a580> 
This is object attribute: Bohdan / 1
This is <class 'property'>: My name is Bohdan / Bohdan@itcollege.lviv.ua
This is <class 'method'> call: Bohdan@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is class variable <class 'int'>: from class 4 / from object 4
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x7f5eee92a5e0> 
This is object attribute: Marta / 2
This is <class 'property'>: My name is Marta / Marta@itcollege.lviv.ua
This is <class 'method'> call: Marta@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is class variable <class 'int'>: from class 4 / from object 4
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x7f5eee92a640> 
This is object attribute: Anonymous / 4
This is <class 'property'>: My name is Anonymous / Anonymous@itcollege.lviv.ua
This is <class 'method'> call: Anonymous@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is class variable <class 'int'>: from class 4 / from object 4
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
We are done. We create 4 names! ??? Why 4? >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/3_lab/screenshots/1.png)

    3. Ознайомився з кодом, розібрався, за що відповідає кожен з рядків.
    4. Модифікував програму, додавши своє ім’я в список:
```python
class MyName:
    """Опис класу / Документація
    """
    total_names = 0 #Class Variable

    def __init__(self, name=None) -> None:
        self.name = name if name is not None else self.anonymous_user().name #Class attributes / Instance variables
        MyName.total_names += 1 #modify class variable
        self.my_id = self.total_names

    @property
    def whoami(self): 
        """Class property
        return: повертаємо імя 
        """
        return f"My name is {self.name}"
    
    @property
    def my_email(self) -> str:
        """Class property
        return: повертаємо емейл
        """
        return self.create_email()
    
    def create_email(self) -> str:
        """Instance method
        """
        return f"{self.name}@itcollege.lviv.ua"

    @classmethod
    def anonymous_user(cls):
        """Classs method
        """
        return cls("Anonymous")
    
    @staticmethod
    def say_hello(message="Hello to everyone!"):
        """Static method
        """
        return f"You say: {message}"


print("Let's Start!")

names = ("Bohdan", "Marta", "Oleksandr", None)
all_names = {name: MyName(name) for name in names}

for name, me in all_names.items():
    print(f"""{">*<"*20}
This is object: {me} 
This is object attribute: {me.name} / {me.my_id}
This is {type(MyName.whoami)}: {me.whoami} / {me.my_email}
This is {type(me.create_email)} call: {me.create_email()}
This is static {type(MyName.say_hello)} with defaults: {me.say_hello()} 
This is class variable {type(MyName.total_names)}: from class {MyName.total_names} / from object {me.total_names}
{"<*>"*20}""")

print(f"We are done. We create {me.total_names} names! ??? Why {MyName.total_names}?")

```
    Програма вивела:
```text
<< Let's Start!
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x7f6f10424580> 
This is object attribute: Bohdan / 1
This is <class 'property'>: My name is Bohdan / Bohdan@itcollege.lviv.ua
This is <class 'method'> call: Bohdan@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is class variable <class 'int'>: from class 5 / from object 5
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x7f6f104245e0> 
This is object attribute: Marta / 2
This is <class 'property'>: My name is Marta / Marta@itcollege.lviv.ua
This is <class 'method'> call: Marta@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is class variable <class 'int'>: from class 5 / from object 5
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x7f6f10424640> 
This is object attribute: Oleksandr / 3
This is <class 'property'>: My name is Oleksandr / Oleksandr@itcollege.lviv.ua
This is <class 'method'> call: Oleksandr@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is class variable <class 'int'>: from class 5 / from object 5
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x7f6f10424730> 
This is object attribute: Anonymous / 5
This is <class 'property'>: My name is Anonymous / Anonymous@itcollege.lviv.ua
This is <class 'method'> call: Anonymous@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is class variable <class 'int'>: from class 5 / from object 5
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
We are done. We create 5 names! ??? Why 5? >>
```
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
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x0000021C8D47E200> 
This is object attribute: Bohdan / 1
This is <class 'property'>: My name is Bohdan / Bohdan@itcollege.lviv.ua
This is <class 'method'> call: Bohdan@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is static <class 'function'> with my prompt: You say: Привіт! 
This is class variable <class 'int'>: from class 5 / from object 5
The number of letters in the name: 6
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x0000021C8D47EB00> 
This is object attribute: Marta / 2
This is <class 'property'>: My name is Marta / Marta@itcollege.lviv.ua
This is <class 'method'> call: Marta@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is static <class 'function'> with my prompt: You say: Привіт! 
This is class variable <class 'int'>: from class 5 / from object 5
The number of letters in the name: 5
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x0000021C8D47E5C0> 
This is object attribute: Oleksandr / 3
This is <class 'property'>: My name is Oleksandr / Oleksandr@itcollege.lviv.ua
This is <class 'method'> call: Oleksandr@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is static <class 'function'> with my prompt: You say: Привіт! 
This is class variable <class 'int'>: from class 5 / from object 5
The number of letters in the name: 9
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<>*<
This is object: <__main__.MyName object at 0x0000021C8D47E8C0> 
This is object attribute: Anonymous / 5
This is <class 'property'>: My name is Anonymous / Anonymous@itcollege.lviv.ua
This is <class 'method'> call: Anonymous@itcollege.lviv.ua
This is static <class 'function'> with defaults: You say: Hello to everyone! 
This is static <class 'function'> with my prompt: You say: Привіт! 
This is class variable <class 'int'>: from class 5 / from object 5
The number of letters in the name: 9
<*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*><*>
We are done. We create 5 names! ??? Why 5? >>
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/3_lab/screenshots/3.png)
 
   D. Порахуйте кількість імен у списку names та порівняйте із виведеним результатом. Дайте відповідь, чому маємо різну кількість імен?
   У виведеному результаті кількість імен більша, тому що у списку присутній user None. 
   У конструкторі класу, якщо name is None, метод anonymous_user() створює ще один об’єкт.
   
### Висновок: 
> У цій роботі я навчився встановлювати сторонні бібліотеки, працювати у віртуальному середовищі: працювати з Pipenv, параметризувати середовища за допомогою змінних середовища. 
