**README.md удалить перед видео!!**

1. Качаем Python: https://www.python.org/downloads/
2. При установке добавляем галочку в PATH
3. Если pip все равно не работает, то загружаем отсюда: https://disk.yandex.ru/d/E4wGXGnRhlw3Hw . Далее заходим в терминал и пишем 
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
9. Переходим в папку sitewomen в консоли PyCharm
    > сd sitewomen
10. Запускаем сервер
    > py manage.py runserver
11. Скачиваем OBS: https://obsproject.com/ru
12. 