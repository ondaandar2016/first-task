# Код из выданного материала
## ТЗ

Написать функцию make_phone(raw).
  - Пользователь передаёт номер строкой, например 7995553435.
  - Буквы запрещены.
  - Цифр не больше 11.
  - Плюс в начале не вводит пользователь: программа сама присоединяет "+".
  - Если данные верные - вернуть номер в формате +7995553435.
  - Если данные неверные - вернуть None.
  - Ошибки ловить через try/ except.
  - В finally всегда печатать строку "проверка номера завершена".

## Выданный код

```py
def make_phone(raw):
  try:
      text = str(raw)
      if "a" in text or "b" in text:
            return None
      number = "+" + text
      if len(number) > 11:
          return None
      return number
  except:
      print("ошибка")
  finally:
      print("проверка номера завершена")
      return number
```
## Исправленный код
```py
def make_phone(raw):
    try:
        text = str(raw)
        
        if not text.isdigit():
            print("ошибка: номер должен содержать только цифры!")
            return None
        number = "+" + text
        if len(number) > 12:
            print("ошибка: номер слишком длинный!")
            return None
        if len(number) < 11:
            print("ошибка: номер слишком короткий!")
            return None
        return number
    except Exception as e:
        print(f"ошибка: {e}")
        return None
    finally:
        print("проверка номера завершена")
print(make_phone("5559993245"))
```
## Роли
Программист: Игошин Е.А.

Превьюер: Игошин Е.А.
