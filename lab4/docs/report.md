# Отчет по лабораторной работе №4 (n8n)
Студентка: Сотникова

## 1. Краткое описание выполненного
Я развернула платформу автоматизации n8n и in-memory СУБД Redis через Docker. Реализовала базовые workflow с использованием нод Manual Trigger, Code, Set, If, HTTP Request и Schedule Trigger. Настроила интеграцию с Redis для CRUD-операций с ключами.

## 2. Способ установки и версии
* Установка: Docker Desktop (проброс портов 5678 для n8n и 6379 для Redis).
* Версия n8n: 1.15.0 (или latest на момент установки).
* Версия Node.js: встроенная в официальный образ n8nio/n8n.
![Версия n8n](../screenshots/01-version.png)

## 3. Освоенные ноды и скриншоты потоков

### 3.1 Manual Trigger, Set и Code
Создание переменных payload и topic, вывод полного объекта.
![Manual Set](../screenshots/01-manual-set.png)

### 3.2 Логика в ноде Code
Написание кастомной логики на JavaScript (циклы, массивы, условия).
![Code node](../screenshots/02-code.png)

### 3.3 Ветвление (IF)
Настройка ветвления (true/false) на основе проверки payload > 5.
![IF node](../screenshots/03-if.png)

### 3.4 Set node (Изменение полей)
Изменение структуры payload и генерация timestamp.
![Set node](../screenshots/04-set.png)

### 3.5 HTTP Request
GET-запросы к публичным API (получение шуток).
![HTTP Request](../screenshots/05-http.png)

### 3.6 Schedule Trigger
Запуск задач по расписанию (раз в минуту).
![Schedule](../screenshots/06-schedule.png)

### 3.7 Работа с Redis
Операции Set и Get (запись и чтение по ключу).
![Redis Set/Get](../screenshots/09-redis.png)

Удаление ключа и проверка его отсутствия (возврат пустого объекта).
![Redis Delete](../screenshots/10-redis-delete.png)

## 4. Выводы
В ходе выполнения работы я изучила платформу n8n. Я научилась строить цепочки автоматизации, писать кастомный JS-код внутри нод, делать внешние HTTP-запросы и работать с кэш-базой Redis для кратковременного хранения данных. Все workflow успешно протестированы.
