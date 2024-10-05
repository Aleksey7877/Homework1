```python
try:
    x = int(input("Введите число: "))
    y = int(input("Введите делитель: "))
    result = x / y
except Exception:
    print("Возникла ошибка")
else:
    print("Результат: ", result)
```

    Введите число:  dsf
    

    Возникла ошибка
    


```python
class CustomError (Exception):
    pass

spisok = input(print("Введите числа: "))
spisok=spisok.split()
i=0
try:
    for number in spisok:
        number=int(number)
        if number % 2 == 0:
            raise CustomError("В списке есть четное число")
        elif  number <0:
            raise CustomError("В списке есть отрицательное число")
        else:
            i+=number
            
except CustomError as e: 
    print(e)
else:
    print(f"Сумма чисел {i}")
```

    Введите числа: 
    

    None 11 35 7 -1
    

    ['11', '35', '7', '-1']
    В списке есть отрицательное число
    


```python
documents = [1, 2, 5, 76, 87, 8, 756, '7']

class IndexError (Exception):
    pass
def index_number(i):
    if i >= len(documents):
        raise IndexError("Индекс элемента выходит за пределы списка.")
    else:
        return documents[i]
try:
    i = int(input(print("Введите индекс: ")))
except IndexError as e:
    print (e)
else:
    print(f"Результат: {index_number(i)}")
```

    Введите индекс: 
    

    None 5
    

    Результат: 8
    


```python
number = list(input(print("Введите число: ")))
n=""
for i in number:
    if i == ",":
        i="."
    n+=i
try:
    float(n)
except Exception:
    print("Возникла ошибка")
else:
    print(n)
```

    Введите число: 
    

    None 2345fd
    

    Возникла ошибка
    


```python
class ValueError (Exception):
    pass
try:
    import math
except Exception:
    print("Не получилось импортировать модуль Math")
    def sqr (x):
        if x<0:
            raise ValueError("Невозможно извлечь корень отрицательного числа.")
        else:
            result=math.sqrt(x)
            print(result)
            return result
else:
    number = int(input(print("Введите число: ")))
    try: sqr(number)
    except ValueError as e:
        print(e)
```

    Введите число: 
    

    None 234
    

    15.297058540778355
    


```python

```

VVV