# Документация REST API (Лабораторная работа №2)

Студентка: Сотникова

### 1\. GET /api/text

Ответ (200 OK): Привет, это текстовый ответ от Sotnikova!

### 2\. GET /api/info

Ответ (200 OK): {"student": "Sotnikova", "status": "online"}

### 3\. GET /api/items

Успешный запрос (?id=1): 200 OK -> {"id": 1, "name": "Ноутбук", "owner": "Sotnikova"}
Ошибка (?id=999): 404 Not Found -> {"error": "Товар не найден (404 Not Found)"}

\---



\## JWT Authentication (Achievement 3)



\### POST /login



Аутентификация пользователя. Возвращает JWT при верных учётных данных.



Request:

{

&#x20; "username": "student",

&#x20; "password": "lab2pass"

}



Response 200:

{

&#x20; "token": "eyJhbGciOiJIUzI1NiIsInR5cCI6IkpXVCJ9..."

}



Response 401:

{

&#x20; "error": "Invalid credentials"

}



Пример:

curl -X POST http://localhost:1880/login -H "Content-Type: application/json" -d "{\\"username\\":\\"student\\",\\"password\\":\\"lab2pass\\"}"



\---



\### GET /me



Защищённый эндпоинт. Требует JWT в заголовке Authorization: Bearer <token>.



Response 200:

{

&#x20; "username": "student",

&#x20; "role": "user",

&#x20; "iat": 1791575000,

&#x20; "exp": 1791578600

}



Response 401:

{

&#x20; "error": "Missing token"

}



Пример:

TOKEN=$(curl -s -X POST http://localhost:1880/login -H "Content-Type: application/json" -d "{\\"username\\":\\"student\\",\\"password\\":\\"lab2pass\\"}")

curl http://localhost:1880/me -H "Authorization: Bearer $TOKEN"



Параметры JWT:

\- Алгоритм: HS256

\- Срок действия: 3600 секунд

\- Secret: lab\_secret\_key\_2026

