https://github.com/SB44444/ArhDz8.git
**Архитектура ПО (семинары)**

*Урок 8. Типы архитектур прикладных приложений (мобильные): MVC, MVP, MVVM*
Задание: Создание UML диаграммы классов для веб-приложения(Любого, но лучше взять за основу прошлую работу)
__
Пример. Вы работаете над проектированием веб-приложения для онлайн-магазина книг. Вам нужно создать UML-диаграмму классов, отображающую связи между основными классами вашего приложения. Вам также необходимо создать YAML-диаграмму для этой диаграммы классов.
__
Инструкции:
__
Определите основные классы, которые будут присутствовать в вашем веб-приложении. Например, классы "Пользователь", "Книга", "Корзина", "Заказ" и другие.
Определите связи между этими классами. Например, класс "Пользователь" может иметь ассоциацию с классом "Корзина", а класс "Корзина" может иметь ассоциацию с классом "Книга".
Создайте UML-диаграмму классов, на которой отобразите классы и связи между ними. Не включайте методы и поля, только связи между классами.
Создайте YAML-диаграмму для этой UML-диаграммы классов. В YAML-диаграмме укажите только имена классов и связи между ними.
Примечание:
__
Ваша UML-диаграмма должна визуализировать связи между классами, такие как ассоциации, агрегации и композиции.
Ваша YAML-диаграмма должна быть валидным YAML-файлом и отражать связи между классами.
Вы можете использовать любой инструмент для создания диаграмм, такой как draw.io, Lucidchart или даже бумагу и карандаш.

*Выполнение:*

За основу принята прошлая работа: "Подготовительный этап создания сайта заказа пиццы" 

На Use-Case диаграмме отражены возмжные взаимодействия пользователя с ситемой заказа.
UML-диаграмма отображает связи между классами.
Идея реализации: 
Ядро программы  package_domain содержит два абстрактных класса Cilent и Goods.
От класса Cilent наследуюся класс FastClient для формирования клиентов без регистрации.
И класс RegisteredClient для формирования клиентов прошедших регистрацию.
Размещены в пакете package_data. Каждый тип клиентов обладает своими свойствами. 
Сохранится возможность добавить дополнительные типы клиентов при необходимости. 
Поведение каждого класса реализуется через соответствующие интерфейсы ActiveCilent и CurrentCilent.
От класса Goods наследуюся класс Piza для создания экземпляров класса, содержит список экземпляров (меню).
От класса Goods наследуюся ещё один класс Delivery содержит список доставок и их свойства.
Поведение каждого класса реализуется через соответствующие интерфейсы ActiveDelivery и ActiveMenu.
Исполльзование абстрактного класса Goods предоставит возможность добавлять новые услуги не затрагивая существующие.
В пакет package_presentation содержит класс Order, который содержит поля определяющие свойства заказа.
Методы интерфейса Promotion изменяет поведение методов рассчета стоимости пиццы, доставки общей стоимости.
Метод Main запускает приложение.
 

































