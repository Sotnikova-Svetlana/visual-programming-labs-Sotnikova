```

flowchart TD

&#x20;   Start(\[Старт: Пациент пришел]) --> Check{Есть в базе?}

&#x20;   Check -- Нет --> Create\[Создать карту] --> ChooseDoc

&#x20;   Check -- Да --> ChooseDoc\[Выбор врача]

&#x20;   ChooseDoc --> CheckSlots{Есть талоны?}

&#x20;   CheckSlots -- Нет --> OtherDay\[Запись на другой день] --> Print

&#x20;   CheckSlots -- Да --> Print\[Печать талона]

&#x20;   Print --> Finish(\[Конец: Талон выдан])

```

