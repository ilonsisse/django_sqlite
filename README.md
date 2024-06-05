# Примечание
**README.md удалить перед видео!!**
# Алгоритм
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
7. Далее вводим и перегазгружаем PyCharm
   > pip install -r requirements.txt
8. Помечаем корневую папку со всеми файлами как sources root в PyCharm: ПКМ на корневую папку -> в самом низу Mark directory as -> Sources root
9. Абсолютно не понимаю почему, но чтобы запустить проект, делаем так:
    > Вверху справа перед кнопкой запустить есть кнопка current file. Нажимаем и проваливаемся в edit configurations -> add a new configuration -> python -> создаем 5 конфигураций как на скринах: runserver, migrate, makemigrations, shell, shell_plus. Самое главное там выбрать интерпретатор Python из djvenv, указать путь к manage.py и script parameters написать правильное слово
    
   > Скрины: https://disk.yandex.ru/d/giPavHIDh8Br0A
    
10. Закрываем окно конфигураций
11. Выбираем из конфигураций вверху справа возле кнопки запустить конфигурацию migrate. Потом нажимаем запустить
12. Затем выбираем конфигурацию shell_plus и запускаем
13. Вводим в командую строку:
    
    __Вывести все объекты__:
    > Women.objects.all()  

    __Примеры фильтров__: 
    > Women.objects.filter(title='Энн Хэтэуэй')

    >Women.objects.filter(title__contains='ли') 

      __Изменение записи__:
    > wu = Women.objects.get(pk=2)
    
    > wu.title = 'Марго Робби'

    > wu.content = 'Биография Марго Робби'

    > wu.save()

    __Удаление записи__:
    > wd = Women.objects.filter(pk__gte=5)

    > wd.delete()
14. Выходим из shell_plus:
    > exit()
15. Скачиваем OBS: https://obsproject.com/ru
16. Во втором разделе Sources добавляем **Screen Capture** и **Audio Input Capture**
17. Если хотим записать весь экран, а не программу, то нужно убедиться, что OBS захватывает весь экран. Заходим в настройки -> video -> Base и Output Resoluiton должны быть в одном разрешении
18. В третьем разделе нажимаем **Start Recording**
19. Там же потом нажимаем на **Stop Recording**
20. После записи внизу OBS покажет, куда он сохранил видео 
# Что говорить на видео
**Примечание**: не открывать сайт проекта, он не работает нормально
- Я установил Django и необходимые библиотеки. Показываем файл в корневой папке **requirements.txt**
- Cоздал проект sitewomen и приложение women. Показываем файл в sitewomen **settings.py**
- Создал модель ORM Women в базе данных SQLite. Показываем файл в women **models.py**. Говорим, что эта модель создает таблицу в БД.
- Применил миграцию(указываем на файл в папке women/migrations **0001_initial.py**), чтобы изменения в базе данных вступили в силу
- К этой базе данных можно применять CRUD(крад)-операции(меняем конфигурацию на shell_plus и запускаем). Показываем примеры п.13