# Приложение для передачи файлов

Этот проект реализует простое приложение для передачи файлов с использованием C++ и API Winsock. Он состоит из клиента и сервера, которые могут отправлять и получать файлы через TCP-соединение. Приложение демонстрирует основные концепции программирования сокетов и операции ввода-вывода файлов.






https://github.com/user-attachments/assets/5e062e66-5ec1-438c-8698-223dc262f49c






## Особенности

- **Отправка файлов**: Клиент может отправлять файлы на сервер.
- **Получение файлов**: Клиент может получать файлы с сервера.
- **Интерфейс с меню**: Пользователи могут легко перемещаться по опциям для отправки или получения файлов или выхода из приложения.

## Требования

- Компилятор C++ (например, Microsoft Visual Studio)
- Операционная система Windows (так как используется Winsock)
- Базовые знания C++ и сетевых концепций

## Файлы

- `client.cpp`: Содержит реализацию клиентской стороны для отправки и получения файлов.
- `server.cpp`: Содержит реализацию серверной стороны для обработки передачи файлов.
- `README.md`: Этот файл документации.

## Как скомпилировать и запустить

### Шаг 1: Настройка сервера

1. Откройте файл `server.cpp` в вашей IDE C++.
2. Скомпилируйте код сервера.
3. Запустите приложение сервера. Оно будет слушать входящие соединения на порту 4321.

### Шаг 2: Настройка клиента

1. Откройте файл `client.cpp` в вашей IDE C++.
2. Скомпилируйте код клиента.
3. Запустите приложение клиента. Оно попытается подключиться к серверу, работающему на `127.0.0.1` (localhost) на порту 4321.

### Шаг 3: Использование приложения

После того как клиент запущен и подключен к серверу, вы увидите меню с следующими опциями:

- **Опция 1**: Введите имя файла, который вы хотите отправить на сервер. Клиент прочитает файл и отправит его на сервер.
- **Опция 2**: Введите имя файла, который вы хотите получить с сервера. Сервер отправит запрашиваемый файл клиенту.
- **Опция 3**: Выйти из приложения клиента.

### Пример взаимодействия
=== КЛИЕНТ ===
Соединение с сервером установлено.
--- МЕНЮ ---

1. Отправить файл на сервер
2. Получить файл с сервера
3. Выйти
Введите ваш выбор: 1
Введите имя файла для отправки на сервер: example.txt
Файл "example.txt" успешно отправлен на сервер.
--- МЕНЮ ---

1. Отправить файл на сервер
2. Получить файл с сервера
3. Выйти
Введите ваш выбор: 2
Введите имя файла для загрузки: example.txt
Файл "example.txt" успешно получен с сервера.
--- МЕНЮ ---

1. Отправить файл на сервер
2. Получить файл с сервера
3. Выйти
Введите ваш выбор: 3
Клиент завершает работу.


## Обработка ошибок

- Если указанный файл для отправки не существует, клиент отобразит сообщение об ошибке: `Ошибка: файл не найден.`
- Если возникла проблема с сохранением полученного файла, клиент отобразит: `Ошибка сохранения файла.`
- Если клиент не может подключиться к серверу, он отобразит: `Ошибка подключения к серверу.`
