# systems-analysis
Домашнее задание для курса "Анализ систем" (Школа Сильных программистов).

## Структура проекта
```
├── .gitignore
├── LICENCE
├── README.md
├── docs                    # дополнительные материалы
└── system
    ├── Data.svg            # модель данных и коммуникаций
    ├── ES.svg              # event storming модель проекта 
    ├── FinalArch.svg       # итоговый набор характеристик, выбранный стиль и описание реализации
    ├── OldES.svg           # event storming модель проекта из домашки предыдущего урока
    ├── Stakeholders.svg    # группы стейкхолдеров и их консерны
    ├── Submonains.svg      # поддомены, bounded-контексты, core domain model
    ├── Week0-Redesign      # переделка системы из домашки нулевой недели
    ├── adr.md              # ADR для одного из элементов системы
    ├── aftermath.md        # рефлексия после завершения основной части курса
    ├── characteristics.md  # основные характеристики проекта (урок 2) и fitness-функции (урок 3)
    ├── docs                # вспомогательные материалы и полезные ссылки
    ├── src                 # исходники диаграмм
    └── task.md             # задание
```

## Глоссарий
- `Коты-тестировщики (КТ)` - сотрудники компании `Happy Cat Box`, клиенты продукта.
- `Клиент` - кот-тестировщик (в первой версии продукта).
- `Коты-менеджеры (КМ)` - сотрудники компании `Make Cats Free`, администраторы продукта.
- `Услуга` - рутинные задачи по тыгыдыканию и скидыванию стаканов.
- `Котоединицы (ке)` - условные денежные единицы для оплаты `услуг`.
- `Кот-воркер (КВ)` - исполнитель `услуги`.
- `Исполнитель` - синоним `КВ`.
- `Эталонный образец` - синоним `клиента`, используется командной матчинга.
- `Обычный образец` - синоним `кота-воркера`, используется командной матчинга.
- `Сотрудник отдела расходников` - отвечает за выдачу расходников для выполнения заказа.
- `Расходники` - набор кошачьих инструментов, жизненно необходимых для выполнения заказов, и печенье.
- `Business domain (Домен)` - часть поля проблем, которую решает компания (см. `Domain Driven Design`).
- `Subdomain (Поддомен)` - часть домена, конкретная проблема меньшего размера, которую необходимо решить компании (см. `Domain Driven Design`).
- `Bounded context` - контекст предметной области, граница, окружающая решение конкретной проблемы (см. `Domain Driven Design`).
- `Консёрн` - от английского `concern` (интерес, проблема, озабоченность).
- `Скоринг` - процесс отбора 3% лучших `КВ`.
- `Матчинг` - процесс подбора идеального `КВ` под `услугу`.

## Спорные и критичные места
1. Система ставок выглядит подозрительно, могут быть проблемы с законом.
2. Утверждается, что система ставок меняться не будет. Это утверждение ничем не подкреплено, вероятно все же будет.
3. Если поставщик печенья не будет выполнять обязательства в срок, возможны задержки в выдаче расходников и провал заказов по времени выполнения. 
4. Не найдем подходящий готовый сервис тестирования. Тогда придется писать самим и Том вырастет.
5. В первой версии коты-воркеры могут обойтись сайтом/дашбордом при работе над заказом. В будущем стоит сделать мобильное приложение, это удобно.
