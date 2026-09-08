# Вариант 2. Пароль
## ТЗ
Функция is_strong(password):
  - принимает строку пароля;
  - возвращает True, если длина пароля не меньше 8 символов;
  - возвращает False, если короче 8.

##  Код на ревью
```py
def is_strong(password):
    if len(password) > 8:
        return True
```
