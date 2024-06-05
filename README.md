**README.md удалить перед видео!!**

1. Качаем Python: https://www.python.org/downloads/
2. При установке добавляем галочку в PATH
3. Если команда pip в терминале все равно не работает, то загружаем отсюда: https://disk.yandex.ru/d/E4wGXGnRhlw3Hw . Далее заходим в терминал и пишем 
   > py(в macOS python3) путь_к_файлу. Пример: py C:\get-pip-2.py
4. Открываем проект в PyCharm
5. Открываем консоль в PyCharm, пишем
   > py -m venv djvenv
6. Запускаем виртуальное окружение
   > Windows: .\djvenv\Scripts\activate

   > macOS и Linux: source djvenv/bin/activate
7. Далее вводим 
   > pip install -r requirements.txt
8. Помечаем корневую папку со всеми файлами как sources root в PyCharm: ПКМ на корневую папку -> в самом низу Mark directory as -> Sources root
9. Абсолютно не понимаю почему, но чтобы запустить проект, делаем так:
    > Вверху справа перед кнопкой запустить есть кнопка current file. Нажимаем и проваливаемся в edit configurations -> add a new configuration -> python -> создаем 4 конфигурации как на скринах: runserver, migrate, makemigrations, shell. Самое главное там выбрать интерпретатор Python из djvenv, указать путь к manage.py и script parameters написать правильное слово
    
   > Скрины: https://disk.yandex.ru/d/giPavHIDh8Br0A
    
10. Закрываем окно конфигураций
11. Выбираем из конфигураций вверху справа возле кнопки запустить конфигурацию migrate. Потом нажимаем запустить
12. Затем выбираем конфигурацию shell и запускаем
13. (Вводим в командную строку по одной команде: 
    > from women.models import Women

    > Women(title='Анджелика Джоли', content='Биография Анджелины Джоли')

    > w1 = _

    > w1.save()

    > from django.db import connection

    > connection.queries

    > exit()
    
    **Примечание**: возможно, нужно потом будет просто вводить from women.models import Women, w1, from django.db import connection, connection.queries)
14. 