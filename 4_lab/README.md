# Звіт до роботи
## Тема: _Віртуальні середовища_
### Мета роботи: _Навчитися працювати у віртуальному середовищі_
---
### Виконання роботи
    1. За допомогою команди pip -V перевірив і переконався, що PIP (Python Install Package) встановлений на моєму комп'ютері.
    Після успішного виконання команди виконав:
```text
pip -help
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

    5. Для інсталяції Pipenv (інструмента для спрощення інсталяції сторонніх бібліотек та створення віруального середовища для кожного проєкту) 
    застосував команду:
```text
pip install pipenv
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/6.png)

     6. Після успішного виконання команди виконав:
```text
pipenv –help
```
     За допомогою pipenv можна виконати такі команди:
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/7.png)
    
     7. Для створення нового середовища та інсталяції бібліотек виконав такі команди:
```text
pipenv --python 3.10
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/8.png)

```text
pipenv –venv
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/9.png)

```text
pipenv run python –V
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/10.png)

```text
pipenv install requests
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/11.png)

     8. Переконався, що створились файли Pipfile та Pipfile.lock:
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/12.png)
   
     - файл Pipfile:
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/13.png)     

     - файл Pipfile.lock:
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/14.png)    
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/14a.png)

     9. Створив пайтон файл і записав у нього програму:
```python
import requests

response = requests.get('https://httpbin.org/')
for line in response.iter_lines():
    print(line)
```
   10. Запустити програму з Visual Studio:
        
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/15.png)
   
   12.  Запустив програму, зайшовши у віртуальне середовище за допомогою команди pipenv shell.
        
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/16.png) 
  
   14. Вибрав бібліотеку graphic-verification-code 1.1.1 на Pypi:
       
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/18.png)
     
   16. Інсталював її:
       
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/19.png)
   
   18. Знайшов документацію цієї бібліотеки:
       
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/20.png)

   20. Записав програму, яка генерує графічний код верифікації в однойменний png-файл:
```python
import gvcode
import base64  

gvcode.generate()

v = gvcode.base64()
print(v[1])
b = base64.b64decode( v[0] )

f = open(v[1] + '.png', 'wb')
f.write(b)
f.close()
```
   Програма вивела:
   
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/21.png)


![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/KEky.png)

![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/Hh5v.png)

![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/Y3kQ.png)

![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/Cm9G.png)

  17. Запустив програму в Visual Studio:
      
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/22.png)

![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/WxnN.png)

![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/wKVb.png)

 18. Змінив інтерпретатор Python із середовища та виконав скрипт через кнопку Run.
     Виникла помилка виконання, оскільки стороння бібліотека gvcode була інстальована
     у віртуальному середовищі, а не глобально:
     
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/23.png)   
   
  20. Створив файл .env та виконав код: 
  ```text
import os
os.environ['HELLO']
```
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/24.png)   

  20. Якщо виконати скрипт без активації віртуального середовища, то видасть помилку:
      
![Image alt](https://github.com/OLexandr-Martyniuk/OLexandr-Martyniuk/raw/main/4_lab/screenshots/25.png)   
       
   ### Висновок: 
> У цій роботі я навчився встановлювати сторонні бібліотеки, працювати у віртуальному середовищі: працювати з Pipenv, параметризувати середовища за допомогою змінних середовища. 
