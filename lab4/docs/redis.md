# Работа с Redis
В ходе лабораторной работы был поднят in-memory кеш Redis через Docker. В n8n созданы credentials с параметрами host.docker.internal:6379.
Собраны два workflow:
1. Запись ключа tachguliev со значением пароля и его последующее чтение (Get).
2. Удаление ключа tachguliev (Delete) и проверка его отсутствия (база возвращает пустой объект).
