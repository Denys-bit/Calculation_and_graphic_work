# Розрахунково-графічна робота
**«Шаблони проектування»**

## Creational pattern: Абстрактна фабрика (Abstract Factory)

**Призначення**:

Породжувальний шаблон проектування, що дозволяє створювати сімейства пов'язаних об'єктів, не прив'язуючись до їх конкретних класів.

**Проблема**:

 * Потрібно створювати групи залежних продуктів, які повинні бути сумісними між собою.
 * Необхідно підтримувати різні варіації цих груп продуктів.
 * Важливо уникати змін у коді при додаванні нових продуктів або варіацій.

**Рішення**:

 * Визначити абстрактні інтерфейси для кожного типу продукту в сімействі.
 * Створити абстрактну фабрику з методами для створення кожного типу продукту.
 * Реалізувати конкретні фабрики для кожної варіації сімейства продуктів.
 * Клієнтський код працює з абстрактними інтерфейсами фабрик та продуктів.

**Структура**:

 * Абстрактні продукти: Інтерфейси для кожного типу продукту.
 * Конкретні продукти: Реалізації абстрактних продуктів для різних варіацій.
 * Абстрактна фабрика: Інтерфейс з методами для створення абстрактних продуктів.
 * Конкретні фабрики: Реалізації абстрактної фабрики, що створюють конкретні продукти певної варіації.

**Переваги**:

 * Гарантує сумісність продуктів.
 * Звільняє клієнтський код від залежностей до конкретних класів.
 * Полегшує додавання нових продуктів та варіацій.

**Недоліки**:

 * Збільшує складність коду через додаткові класи.
 * Вимагає наявності всіх типів продуктів у кожній варіації.

**Застосування**:

 * Коли потрібно працювати з різними видами пов'язаних продуктів незалежно від їх конкретних класів.
 * Коли необхідно підтримувати різні варіації сімейств продуктів.
 * Коли потрібно уникнути змін у коді при додаванні нових продуктів або варіацій.

**Приклад**:

Крос-платформовий графічний інтерфейс, де елементи відображаються по-різному залежно від операційної системи. Абстрактна фабрика створює елементи інтерфейсу відповідно до обраної ОС.

![image_abstract_factory](https://github.com/Denys-bit/Calculation_and_graphic_work/assets/104843082/15ebe0ac-4866-4b98-b559-074f0515cf07)

[**Посилання на джерело.**](https://refactoring.guru/uk/design-patterns/abstract-factory).

## Structural pattern: Фасад (Facade)

**Шаблон проектування Фасад**

**Фасад** - це структурний шаблон проектування, який надає простий інтерфейс до складної підсистеми. Він приховує складність підсистеми від клієнтського коду, роблячи його більш зрозумілим та зручним для обслуговування. Фасад також може використовуватися для зменшення кількості залежностей, які має клієнтський код.

**Переваги**:

 * Спрощує клієнтський код, надаючи простий інтерфейс до складної підсистеми.
 * Зменшує кількість залежностей, які має клієнтський код.
 * Робить клієнтський код більш зрозумілим та зручним для обслуговування.
Недоліки використання шаблону проектування 

**Можливості**:

 * Може створити "божественний" об'єкт, який знає про всі класи в підсистемі.
 * Може ускладнити тестування клієнтського коду, оскільки клас фасаду приховує складність підсистеми.
Застосування шаблону проектування Фасад:
 * Коли потрібно надати простий інтерфейс до складної підсистеми.
 * Коли потрібно зменшити кількість залежностей, які має клієнтський код.
 * Коли потрібно зробити клієнтський код більш зрозумілим та зручним для обслуговування.

**Приклад використання**:

Наприклад, є веб-сайт з електронною комерцією. Клієнтський код, який використовується для оформлення замовлення, може бути дуже складним, оскільки він повинен взаємодіяти з багатьма різними підсистемами, такими як система кошика, система оплати та система доставки. Використовуючи шаблон проектування Фасад, ви можете створити клас фасаду, який надає простий інтерфейс для оформлення замовлення. Це зробить клієнтський код більш зрозумілим та зручним для обслуговування.

**Mermaid** діаграма фасаду:

![image_facade](https://github.com/Denys-bit/Calculation_and_graphic_work/assets/104843082/1a05c79f-4ce6-40f1-9e30-a9cd81181c2c)

[**Посилання на джерело.**](https://refactoring.guru/uk/design-patterns/facade)

## Behavioral pattern: Шаблонний метод (Template method)

**Шаблонний метод** - це поведінковий шаблон проектування, який дозволяє розбити алгоритм на кроки, дозволяючи підкласам визначати конкретні кроки без зміни загальної структури. Це сприяє повторному використанню коду.

**Переваги використання**:

 * Сприяє повторному використанню коду.
 * Покращує гнучкість коду.
 * Полегшує розширення коду.

**Недоліки використання**:

 * Може призвести до надмірного узагальнення.
 * Може ускладнити розуміння коду.

**Застосування**:

 * Коли ви маєте кілька класів з подібною функціональністю, але з незначними відмінностями.
 * Коли ви хочете, щоб алгоритм можна було розширювати без зміни його основної структури.

**Приклад використання**:

Наприклад, є будівельники, а є будівельна компанія, яка може мати стандартний процес, оформлений як шаблонний метод. Цей шаблонний метод може включати кроки, такі як заливка фундаменту, каркас стін та монтаж даху. Однак залежно від уподобань клієнта можуть бути внесені деякі налаштування. Наприклад, у розкішному будинку можуть бути додаткові кроки в шаблоні методу, такі як встановлення системи безпеки.

> Шаблон проектування може бути корисний, коли у вас є кілька класів з подібною функціональністю, але з незначними відмінностями. Це дозволяє уникнути дублювання коду та сприяє підтримці.

**Mermaid** діаграма шаблонного методу:

![image_template_method](https://github.com/Denys-bit/Calculation_and_graphic_work/assets/104843082/96d7db34-c1b5-450f-8212-74bdab6ff098)

[Посилання на джерело.](https://refactoring.guru/uk/design-patterns/template-method)

## Concurrency pattern: Блокування (Lock)

**Блокування** - це шаблон паралельності, який забезпечує синхронізований доступ до спільного ресурсу в багатопотоковому середовищі. Він запобігає виникненню race condition (стан гонки), коли кілька потоків одночасно намагаються змінити спільний ресурс, що може призвести до непередбачуваних результатів.

**Переваги використання**:

 * Забезпечує безпечний доступ до спільних ресурсів у багатопотоковому середовищі.
 * Запобігає виникненню race condition (стан гонки), гарантуючи, що лише один потік може змінювати ресурс у певний момент часу.

**Недоліки використання**:

 * Може призвести до зниження продуктивності, оскільки потоки можуть блокуватися під час очікування звільнення блокування.
 * Може призвести до deadlock (взаємного блокування), якщо потоки блокують один одного, очікуючи звільнення блокувань.
Застосування шаблону Lock:
 * Коли кілька потоків одночасно отримують доступ до спільного ресурсу, і необхідно забезпечити синхронізацію їх дій.
 * Коли потрібно запобігти виникненню race condition (стан гонки).

> **Приклад використання**:
Наприклад, є банківський рахунок, до якого одночасно звертаються кілька клієнтів. Якщо не використовувати блокування, то можлива ситуація, коли два клієнти одночасно знімають гроші, і баланс рахунку стане некоректним. Застосування блокування гарантує, що лише один клієнт може змінювати баланс рахунку в певний момент часу.

![image_lock](https://github.com/Denys-bit/Calculation_and_graphic_work/assets/104843082/faef6579-4e28-468e-ad6d-bf561bb49f50)

[Посилання на джерело.](https://www.studocu.com/en-us/document/the-university-of-texas-at-arlington/software-design-patterns/understanding-the-concurrency-pattern-lock/52444388)
