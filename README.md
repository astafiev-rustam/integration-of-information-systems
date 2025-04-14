|||
|---|---|
|ДИСЦИПЛИНА|Интеграция информационных систем с использованием API и микросервисов|
|ИНСТИТУТ|ИПТИП|
|КАФЕДРА|Индустриального программирования|
|ВИД УЧЕБНОГО МАТЕРИАЛА|Методические указания к практическим занятиям|
|ПРЕПОДАВАТЕЛЬ|Астафьев Рустам Уралович|
|СЕМЕСТР|1 семестр, 2024/2025 уч. год|

Ссылка на GitHub репозиторий:
https://github.com/astafiev-rustam/Integration-of-information-systems/tree/Practice-1-2

## Практическое занятие №2 - Архитектура ПО и паттерны проектирования

**Формат:** Групповая работа (3–4 человека) → Решение кейсов → Короткие презентации (5–7 мин)  

---  

### **Задание 1. Выбор архитектурного стиля для системы**  
**Цель:** Сравнить монолитную, микросервисную и сервис-ориентированную (SOA) архитектуры и обосновать выбор для конкретного кейса.  

**Кейс:**  
Компания разрабатывает платформу для онлайн-образования с функционалом:  
- Видеолекции (стриминг)  
- Тесты и проверка заданий (сложная логика)  
- Личный кабинет (профиль, прогресс)  
- Интеграция с платежными системами.  

**Задачи:**  
1. Опишите плюсы/минусы каждой архитектуры для этого кейса.  
2. Предложите оптимальный вариант, учитывая:  
   - Масштабируемость видеосервиса.  
   - Независимость обновлений модуля тестов.  
   - Надежность платежей.  
3. Подготовьте слайды с сравнительной таблицей и схемой выбранной архитектуры.  

**Результат:** Презентация с обоснованием выбора архитектуры.  

---  

### **Задание 2. Применение паттернов проектирования для API**  
**Цель:** Научиться применять паттерны (например, Facade, Adapter, Singleton) для решения проблем интеграции.  

**Кейс:**  
У компании есть legacy-система бухгалтерии (SOAP API), но новый мобильный клиент требует REST API. Также нужно:  
- Кэшировать запросы к справочнику товаров.  
- Упростить сложный интерфейс отчетности для фронтенда.  

**Задачи:**  
1. Определите, какие паттерны помогут решить эти проблемы (например, *Adapter* для SOAP→REST, *Facade* для отчетности, *Singleton* для кэша).  
2. Нарисуйте UML-диаграмму взаимодействия компонентов.  
3. Объясните, как выбранные паттерны улучшают поддерживаемость кода.  

**Результат:** Презентация с диаграммами и примерами кода (псевдокод).  

---  

### **Задание 3. Оптимизация микросервисов с помощью паттернов**  
**Цель:** Разобрать паттерны для микросервисов (Saga, API Gateway, Circuit Breaker).  

**Кейс:**  
Сервис доставки еды состоит из микросервисов:  
- Заказы (Order)  
- Оплата (Payment)  
- Доставка (Delivery)  

**Проблемы:**  
- При отмене заказа нужно откатывать оплату и доставку.  
- Фронтенд делает 10+ запросов к разным сервисам.  
- Сервис оплаты иногда "падает".  

**Задачи:**  
1. Предложите паттерны для решения этих проблем (например, *Saga* для транзакций, *API Gateway* для агрегации запросов, *Circuit Breaker* для оплаты).  
2. Опишите сценарий работы системы при отмене заказа.  
3. Покажите на схеме, как паттерны уменьшают связность сервисов.  

**Результат:** Презентация с архитектурной схемой и описанием сценариев.  

---  

### **Логистика выполнения:**  
- **15 мин** – Разбор кейсов в группах.  
- **30 мин** – Подготовка решений и слайдов.  
- **45 мин** – Презентации (по 5–7 мин на группу + вопросы).  

**Критерии оценки:**  
- Корректность применения паттернов.  
- Четкость архитектурных решений.  
- Практическая польза для кейса.  
