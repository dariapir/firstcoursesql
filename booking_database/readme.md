# booking_database

Всем доброго времени суток! Выполнив тестовое задание для компании, разрабатывающих платформы для отелей, я решила познакомиться с приложением Power Bi.
Написала несложные запросы, чтобы просто разобраться в функционале.

[Получился дашборд](https://github.com/dariapir/sql/blob/main/booking_database/firstpowerbi.pdf)

Запросы, написанные мною для этой работы:
[Создание таблиц](https://github.com/dariapir/sql/blob/main/booking_database/tables),
[Запись данных](https://github.com/dariapir/sql/blob/main/booking_database/Insert),
[Views](https://github.com/dariapir/sql/blob/main/booking_database/views),
[Запросы для Power Bi](https://github.com/dariapir/sql/blob/main/booking_database/queries%20for%20power%20bi).

## Задания:

### 1.	Заполнить таблицы данными.
#### [dbo].[booking] 
	Кол-во данных: 500 000
	creation_date: 01.01.2018 - 01.03.2018
	id_provider: соответствует набору в таблице [dbo].[provider]
id_currency: должны быть брони с различными валютами (коды валют можно посмотреть тут http://vch.ru/zifrovye_i_bukvennye_kody_valyut_mira.html)
creator:  если source_name != ‘BS-CHANNEL_MANAGER’ , то значение пустая строка (‘’). В случае, когда source_name = ‘BS-CHANNEL_MANAGER’ должы быть записи со значением ‘BGC’ (но не все).
	остальные данные могут быть заполнены рандомно
#### [dbo].[provider]
	Кол-во данных: 10 000
	id_country: соответствует набору в таблице [dbo].[country]
id_city: соответствует набору в таблице [dbo].[city]
остальные данные могут быть заполнены рандомно
#### [dbo].[country]
	Кол-во данных: 20
#### [dbo].[city]
	Кол-во данных: 300
#### [dbo].[source]
	Кол-во данных: 10
	Должен содержать ‘BS-CHANNEL_MANAGER’, остальное может быть заполнено рандомно
#### [dbo].[currency_rate]
	Кол-во данных: на каждую дату создания брони (01.01.2018 - 01.03.2018) должна быть запись перевода в валюты, которые имеются в таблице [dbo].[booking]
	id_currency: можно посмотреть тут http://vch.ru/zifrovye_i_bukvennye_kody_valyut_mira.html
	date: в пределах 01.01.2018 - 01.03.2018
	остальные данные могут быть заполнены рандомно

### 2.	Создать view, где будет содержаться следующая информация:
ID провайдера

Название провайдера

Страна

Город

Дата создания брони

Дата заезда в брони

Количество ночей

Сумма брони в исходной валюте

Валюта брони

Сумма брони в рублях (конвертация происходит по дате создания брони)

### 3.	Создать view, который содержал бы следующую информацию:
ID провайдера

Название провайдера

Страна

Город

Год создания брони

Месяц создания брони

Доля броней среди всех броней провайдера, где source_name =  ‘BS-CHANNEL_MANAGER’

Доля броней среди всех броней провайдера, где source_name =  ‘BS-CHANNEL_MANAGER’ и creator = ‘BGC’ 

### 4.	Подсчитать среднее количество броней и среднюю сумму броней в месяц с условием, что у провайдера есть хотя бы одна бронь каждый месяц. Если в какой-то из месяцев броней нет, такой провайдер не должен выводится.
ID провайдера

Название провайдера

Страна

Город

Год создания брони

Месяц создания брони

Среднее количество броней

Средняя сумма броней

Каждый скрипт не должен выполняться дольше минуты. 

Для оптимизации можно создавать индексы.
