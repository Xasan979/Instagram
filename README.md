# Coursework_3.1
```
╭═══════════════╮   ╭═══════════════╮
│ Made by V_E_K │   │ version 0.0.1 │
╰───────────────╯   ╰───────────────╯
```
## Задание 
    https://disk.yandex.ru/d/5Qx3bKTA7gVAug

## Содержание
* [Setup](#setup)
* [Short description](#description)
* [TODO](#todo)


<a id="setup"></a>
## Setup
### Как запустить:
   Создайте venv и установите требования
   
   cd (путь к папки с проектом)
       
       Mac OS
          python3 -m venv env
          source env/bin/activate - for Unix or MacOS
          pip install -r requirements.txt
  
        Windows
          py -m venv env
          .\env\Scripts\activate
          py -m pip install -r requirements.txt
          
## Получение отчетов: 
   Установка allure 
   
   В командной строке
   
       Mac OS
          brew install allure

       Windows 
          scoop install allure
          
## Провести тест:
   *в папке config.py поменять пути
   
   В командной строке
   
          python -m pytest --alluredir=test_results/ tests/comments_dao_test.py tests/api_test.py 
          
## Сгенерировать отчет:
   В командной строке 
   
          cd (путь к папки с проектом)  
          allure serve test_results/          

### Примечания
После запуска, нужно перейти в браузере по адресу <a href="http://127.0.0.1:5000/" target="_blank">http://127.0.0.1:5000/</a>.



<a id="description"></a>
##  Краткое описание:

### Главная страница
`url = "/"`

![image](https://user-images.githubusercontent.com/98303243/169661739-455fd571-7955-417e-8a3c-6bcc3abc2600.png)
Все посты.
В верхнем углу имеются две кнопки (по условию была одна), это поиск и страница с bookmarks (закладками)

---
### Страница поста
`url = "/posts/<post_id>"`

Полный текст поста, фотка и комментарии.

---
### Страница пользователя
`url = "/users/<user_name>"`

Все посты определенного пользователя.

---
### Страница поиска
`url = "/search"`

![image](https://user-images.githubusercontent.com/98303243/169661810-5484fa0b-416b-4493-9929-3570fd13d5fd.png)
Просто поиск по постам)

---
### Страница закладок
`url = "/bookmarks"`

Все посты которые добавил пользователь.
Есть возможность их удаления.

---
### Страница тегов
`url = "/tag/<tag_name>"`

Все посты у которых имеется данный тэг.

<a id="todo"></a>
## TODO
- [x] Основные функции реализованны 
- [ ] Достаточно комментариев к коду
- [x] Страницы
  - [x] Главная
    - [x] Отображаются все посты 
    - [x] Кнопка поиска
    - [x] Кнопка bookmarks
    - [x] Все ссылки работают
  - [x] Пост
    - [x] Подсветка тегов
    - [x] Разделение текста на `<p></p>` по `\n`
    - [x] Комментарии
    - [ ] Возможность писать свои комментарии (этого нет в задании, но хотелось бы понять как это сделать)
  - [x] Страница пользователя
    - [x] Посты только этого пользователя
  - [x] Поиск по контенту
    - [x] Не зависит от регистра
  - [x] Поиск по тегу
    - [x] Ищет только теги (`#teg`)
  - [x] Закладки
    - [x] Можно удалять
    - [x] Можно добавлять (на страницах с постами)
  - [x] api
    - [x] Возвращаются верные данные, в нужном формате
      - [x] Сохранение log-ов
  - [x] Страницы об ошибках (404, 500)
    - [x] `Красивые`
- [x] Тесты работают
  - [x] Тесты для api
  - [x] Тесты для comments_dao
  - [x] Тесты для posts_dao

