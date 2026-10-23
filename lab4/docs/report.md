
## 5. Выполнение ачивки (REST API)
Выбрана Ачивка 5.1: Написать Rest API для работы с заметками, используя встроенную БД n8n (Static Data).
Был создан один Workflow с двумя Webhook-нодами:
* POST /webhook/notes — принимает JSON с текстом заметки, с помощью ноды Code сохраняет её в $getWorkflowStaticData("global").
* GET /webhook/notes — возвращает массив всех сохраненных заметок.

![Архитектура API](../screenshots/achieve-api-flows.png)
![Тестирование через cURL](../screenshots/achieve-api-terminal.png)

## 5. Выполнение ачивки (REST API)
Выбрана Ачивка 5.1: Написать Rest API для работы с заметками, используя встроенную БД n8n (Static Data).
Был создан один Workflow с двумя Webhook-нодами:
* POST /webhook/notes — принимает JSON с текстом заметки, с помощью ноды Code сохраняет её в $getWorkflowStaticData("global").
* GET /webhook/notes — возвращает массив всех сохраненных заметок.

![Архитектура API](../screenshots/achieve-api-flows.png)
![Тестирование через cURL](../screenshots/achieve-api-terminal.png)
