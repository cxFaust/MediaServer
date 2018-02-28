# MediaServer

Разработать веб-систему согласно требованиям.

<h4> Общие требования к проекту:</h4>

Приложение реализовать применяя технологии Servlet и JSP.

Архитектура приложения должна соответствовать шаблонам Layered architecture и Model-View-Controller. 
Controller может быть только двух видов: контроллер роли или контроллер приложения.

Информация о предметной области должна хранится в БД:

данные в базе хранятся на кириллице, рекомендуется применять кодировку utf-8

технология доступа к БД – JDBC (только JDBC)

для работы с БД в приложении должен быть реализован потокобезопасный пул соединений,использовать слово synchronized запрещено.

при проектировании БД рекомендуется не использовать более 6-8 таблиц

доступ к данным в приложении осуществлять с использованием шаблона DAO.

Интерфейс приложения должен быть локализован; выбор из двух или более языков: (английский, белорусский, и т д.).

Приложение должно корректно обрабатывать возникающие исключительные ситуации, в том числе вести их логи.
В качестве логгера использовать Log4J или SLF4J.

Классы и другие сущности приложения должны быть грамотно структурированы по пакетам и иметь отражающую их функциональность название.

При реализации бизнес-логики приложения следует при необходимости использовать шаблоны проектирования 
(например, шаблоны GoF: Factory Method, Command, Builder, Strategy, State, Observer, Singleton, Proxy etc).

Для хранения пользовательской информации между запросами использовать сессию.

Для перехвата и корректировки объектов запроса (request) и ответа (response) применить фильтры.

При реализации страниц JSP следует использовать теги библиотеки JSTL, использовать скриплеты запрещено. 
Обязательным требованием является реализация и использование пользовательских тегов. 
Просмотр “длинных списков” желательно организовывать в постраничном режиме.

Валидацию входных данных производить на клиенте и на сервере.

Документацию к проекту необходимо оформить согласно требованиям javadoc.

Оформление кода должно соответствовать Java Code Convention.

Разрешается использовать технологию Maven.

Приложение должно содержать 3-4 теста JUnit, Mockito или EasyMock.

<h4>Общие требования к функциональности проекта:</h4>

1) Авторизация(sign in) и выход(sign out) в/из системы.

2) Регистрация пользователя или добавление артефакта предметной области системы.

3) Просмотр информации (например: просмотр всех курсов, имеющихся кредитных карт, счетов и т.д.)

4) Удаление информации (например: отмена заказа, медицинского назначения, отказ от курса обучения и т.д.)

5) Добавление и модификация информации (например: создать и отредактировать курс, создать и отредактировать заказ и т.д.)

# Предметная область:

Система Заказ АудиоТреков. Клиент заказывает и оплачивает АудиоТрек(и). Оставляет отзывы об АудиоТреке.
Администратор добавляет новые АудиоТреки, корректирует информацию о существующих, управляет Клиентами, назначая им бонусы, скидки и пр.
