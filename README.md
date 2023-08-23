# Программа записная книга
---
## Установка
python -v = 3.9.10 64-bit
pip -v = 23.1.2
#### openpyxl 
"pip install openpyxl"
Requirement already satisfied: openpyxl in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (3.1.2)

Requirement already satisfied: et-xmlfile in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (from openpyxl) (1.1.0)
#### Сборка программы через pyinstaller
"pip install pyinstaller"
команда "pyinstaller -F calllist.py"
Requirement already satisfied: pyinstaller in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (5.13.0)

Requirement already satisfied: setuptools>=42.0.0 in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (from pyinstaller) (68.0.0)

Requirement already satisfied: altgraph in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (from pyinstaller) (0.17.3)

Requirement already satisfied: pyinstaller-hooks-contrib>=2021.4 in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (from pyinstaller) (2023.6)

Requirement already satisfied: pefile>=2022.5.30 in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (from pyinstaller) (2023.2.7)

Requirement already satisfied: pywin32-ctypes>=0.2.1 in c:\users\user\appdata\local\programs\python\python39\lib\site-packages (from pyinstaller) (0.2.2)

---
# Код
Вообще весь код выглядит более менее (менее) читабельно, и все что я использовал в коде довольно понятно, также каждое действие имеет коментарии по которым можно понять что именно я там реализовывал
---
![scren1](https://github.com/SaidHelps/calllist/assets/99082063/3230e6ca-e087-4f10-9d2f-7db2bcd6157a)
---
![screen2](https://github.com/SaidHelps/calllist/assets/99082063/5425236a-5c63-432d-bf6f-dd1705630c16)
---
Так как программа консольная и интрефейса у неё нету, то 60% всего кода я проверял чтобы пользователь не вводил не подсотвляемые значения в параметры.
---
# Способ хранения данных. (База данных)
Решил использовать именно xlsx таблицы так как они могут практически бесконечно расшираться, в любые стороны, но я решил сделать так чтобы они бесконечно расли по вертикали, почему не горизонтально? - по большей части причиной этого являетсья то что xlsx таблицы используюьт для обозначения клеток цифро-буквенный тип названия обозначения позиции клеток, но это можно было обойти и сделать её горизонтальной через cell(row=row, column=column) фукнция которая уже принимает 2 числа для подставления значений в клетки. вообщем там уже я делал как было удобнее.
---
В начале программа сама создает базу данных если она не существует, и я ввожу любой текст чтобы её хоть чем то наполнить, потому-что если таблица пустая почему то библиотека openpyxl отказываеться её читать, ссылаясь на не верную архивацию, файла, также может возникнуть ошибка программы если вы будете пытаться с открытой редактируемой таблицей xlsx запустить программу, программа просто не сомжет её прчоитать так что перед использованием программы советуеться закрывать все открытые вкладки с раедактируемыми таблицами.
---

# Обзор программы
---
Попробуем заполнить строку из таблицы, и создадим 1 контакн.
---
![e15b7f83-16cf-45b7-81eb-70f8b2965088](https://github.com/SaidHelps/calllist/assets/99082063/1139ea34-a193-4dab-bf93-6f01eec65379)
---
если все получлось успешно то нас об этом уведомляют.

Зайдем в таблцу xlsx и проверим сохранилось ли всё там.
---
![afe859cd-7b21-45d7-b5f9-f4fc88c9f59d](https://github.com/SaidHelps/calllist/assets/99082063/ce0e87f9-2a45-4199-8209-5ee9fda7d03b)
---
Все успешно сохранилось теперь попробуем вывести эти данные.
---
![21890145-829d-4d43-941a-c4863bd08343](https://github.com/SaidHelps/calllist/assets/99082063/2e0f8301-4e36-4c35-a0a8-4073072e0c13)
---
программа успешно вывела по строке из таблицы нужные нам данные.

на этом всё.


