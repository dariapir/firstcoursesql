# Конфигурация 1С:Отель 

Когда в университете сказали, что нужно самостоятельно создать конфигурацию 1С - глаза полезли на лоб. Но, глаза боятся, а руки делают.
Хочу оформить данную работу в небольшой проект, а для остальных студентов - помочь в этом нелегком деле.

Из основных функций настроены справочники гостиничных номеров, клиентов, сотрудников. 
Главная цель: не дать забронировать занятый номер. Для этого создан периодический регистр сведений.
В документах Бронирование и Заезд гостей осуществляется проверка, и если номер свободен - документ проводится. 
Также оформлен красивый отчет, который показывает статус номеров.

Скачать текст курсовой, ход работы [здесь](https://github.com/dariapir/projects/blob/main/1с/Текст%20курсовой/Курсовая%20для%20git.docx).
Скачать выгрузку БД [здесь](https://github.com/dariapir/projects/blob/main/1с/Конфигурация%20"Отель"/Курсовая%20работа.dt).
### Регистр сведений "Статус Номеров"
Значение 1 - номер свободен, 2 - забронирован, 3 - заселен.

![Alt text](pictures/РегистрСведений.png?raw=true "Title")
### Отчет "Статус Номеров"
Зеленым - свободные номера, желтым - забронированные, красным - заселенные.

![Alt text](pictures/ОтчетСтатусНомеров.png?raw=true "Title")
### Отчет "Рейтинг Продаж" по номенклатуре
И гостиничные номера, и услуги.

![Alt text](pictures/РейтингПродажНоменклатура.png?raw=true "Title")
### Отчет "Рейтинг Продаж" по сотрудникам
![Alt text](pictures/РейтингПродажСотрудники.png?raw=true "Title")
### Отчет "Оборотно-Сальдовая Ведомость" 
![Alt text](pictures/ОборотноСальдоваяВедомость.png?raw=true "Title")
