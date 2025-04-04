1.1. Название объекта в системе:
1.1.1. Карточка сотрудника в ИС Кадры

1.2. Уровень конфиденциальности хранимой информации в ИС: 3

1.3. Условия отбора:
1.3.1. Поле "Form" принимает значение "1"
1.3.2. Поле "ReserveDate" ПУСТО
1.3.3. Поле "status" принимает значение "2" или "3"
1.3.4. Поле "DOPUSKENDDATE" содержит дату < даты запуска выгрузки 	'отбираем только просроченные допуска
1.3.5. Поле "Dopuskcategory" принимает все значения, кроме "" (пустота), "-2".

1.4. Выгружаемые данные:
1.4.1. Поля "sur_name", "first_name" , "mid_name"  выгружается ФИО сотрудника
1.4.2. Поле "UNID" выгружается ссылка на карточку сотрудника
1.4.3. Поле "DOPUSKCATEGORY" выгружается персональный уровень допуска безопасности сотрудника
1.4.4. Поле "DOPUSKCATEGORYPERIOD" выгружается частота пересмотра
1.4.5. Поле "DopuskApproveDate" выгружается дата решения о присвоении персонального допуска безопасности сотруднику
1.4.6. Поле "DOPUSKENDDATE" выгружается срок действия персонального допуска безопасности сотрудника

1.5. Вычисляемые значения:
1.5.1. Вычисляется общее количество найденных карточек сотрудников (в соотв. с условиями отбора п.1.3)



2.1 Название объекта в системе:
карточка частной должности в ИС Структура
2.2. Уровень конфиденциальности хранимой информации в ИС: 3

2.3. Условия отбора:
2.3.1. Поле "Active" принимает значение "1". 
2.3.2. Поле StfUid <>"" (не пусто),  выгружается идентификатор карточки сотрудника.
2.4. Выгружаемые данные:
2.4.1. Поле "Полный иерархический путь (аббревиатуры)" выгружается наименование должности
2.4.2. Поле "UNID" выгружается ссылка на карточку должности
2.4.3. Поле "TargetAccess" выгружается уровень допуска должности


2.5. Вычисляемые значения:
2.5.1. Вычисляемые значения отсутствуют


3.1. Название объекта в системе:
3.1.1. Карточка сотрудника в ИС Кадры
3.2. Уровень конфиденциальности хранимой информации в ИС: 3

3.3. Условия отбора:
3.3.1. Поле "Form" принимает значение "1"
3.3.2. Поле "ReserveDate"  ПУСТО
3.3.3. Поле "status" принимает значен_ие "2" или "3"
3.3.4. Поле "DOPUSKENDDATE" содержит дату, которая еще не наступила по отношению к дате запуска выгрузки (дату запуска выгрузки включаем в выборку)	'исключаем просроченные допуска
3.3.5. Поле "DopuskCategory" карточки сотрудника содержит значение больше, чем значение поля "TargetAccess" (п. 2.4.3. Выборки 2) карточки частной должности, на которую назначен сотрудник. (например, значение "DopuskCategory" = 3, значение "TargetAccess" = "1")
3.3.6. Значение в поле "universalid" соответствует значению поля "StfUID" п. (2.3.2) в карточке должности из Выборки 2


3.4. Выгружаемые данные:
3.4.1. Поля "sur_name", "first_name" , "mid_name"  выгружается ФИО сотрудника
3.4.2. Поле "UNID" выгружается ссылка на карточку сотрудника
3.4.3. Поле "DOPUSKCATEGORY" выгружается персональный уровень допуска безопасности сотрудника
3.4.4. Поле "DOPUSKCATEGORYPERIOD" выгружается частота пересмотра
3.4.5. Поле "ShortPath" выгружается частная должность, на которую назначен сотрудник
3.4.6. Поля "TargetAccess", "TargetAccessPeriod" выгружается целевой допуск безопасности частной должности (через разделитель "точка", например "5.2"), на которую назначен сотрудник

3.5. Вычисляемые значения:
3.5.1. Вычисляется общее количество найденных карточек сотрудников (в соотв. с условиями отбора п.3.3)

3.1. Название объекта в системе:
3.1.1. Карточка сотрудника в ИС Кадры
3.2. Уровень конфиденциальности хранимой информации в ИС: 3

3.3. Условия отбора:
3.3.1. Поле "Form" принимает значение "1"
3.3.2. Поле "ReserveDate"  ПУСТО
3.3.3. Поле "status" принимает значен_ие "2" или "3"
3.3.4. Поле "DOPUSKENDDATE" содержит дату, которая еще не наступила по отношению к дате запуска выгрузки (дату запуска выгрузки включаем в выборку)	'исключаем просроченные допуска
3.3.5. Поле "DopuskCategory" карточки сотрудника содержит значение больше, чем значение поля "TargetAccess" (п. 2.4.3. Выборки 2) карточки частной должности, на которую назначен сотрудник. (например, значение "DopuskCategory" = 3, значение "TargetAccess" = "1")
3.3.6. Значение в поле "universalid" соответствует значению поля "StfUID" п. (2.3.2) в карточке должности из Выборки 2


3.4. Выгружаемые данные:
3.4.1. Поля "sur_name", "first_name" , "mid_name"  выгружается ФИО сотрудника
3.4.2. Поле "UNID" выгружается ссылка на карточку сотрудника
3.4.3. Поле "DOPUSKCATEGORY" выгружается персональный уровень допуска безопасности сотрудника
3.4.4. Поле "DOPUSKCATEGORYPERIOD" выгружается частота пересмотра
3.4.5. Поле "ShortPath" выгружается частная должность, на которую назначен сотрудник
3.4.6. Поля "TargetAccess", "TargetAccessPeriod" выгружается целевой допуск безопасности частной должности (через разделитель "точка", например "5.2"), на которую назначен сотрудник

3.5. Вычисляемые значения:
3.5.1. Вычисляется общее количество найденных карточек сотрудников (в соотв. с условиями отбора п.3.3)


4.1. Название объекта в системе:
4.1.1. Карточка категории должности в ИС Структура ("Справочник\Категория должности")

4.2. Уровень конфиденциальности хранимой информации в ИС: 3

4.3. Условия отбора:
4.3.1. Из документов"Справочник\Категория должности" фиксируем наименования категорий должностей (Поле "TypePosition_Name"), включенные в АШЧ: 
4.3.1.1. Поле "Form" принимает значение "profTypePosition"
4.3.1.2. Поле "ActiveStaff" принимает значение "1"

4.4. Выгружаемые данные:
4.4.1. Поле "PositionType_name" выгружается категория частной должности


4.5. Вычисляемые значения:
4.5.1. Вычисляемые значения отсутствуют


5.1 Название объекта в системе:
карточка частной должности  в ИС Структура

5.2. Уровень конфиденциальности хранимой информации в ИС: 3

5.3. Условия отбора:
5.3.1. Поле "Form" принимает значение "1"
5.3.2. Поле "Active" принимает значение "1"
5.3.3. Поле "TypeUnit" принимает значение "2"
5.3.4. Значение в поле "Категория должности" соответствует значению категории из выборки 4

5.4. Выгружаемые данные:
5.4.1. Поле "ShortPath" выгружается наименование частной должности
5.4.2. Поле "UNID" выгружается ссылка на частную должность
5.4.3. Поле "PositionType_name" выгружается категория частной должности
5.4.4. Поля "TargetAccess", "TargetAccessPeriod" выгружается целевой допуск безопасности частной должности (через разделитель "точка", например "5.2")


5.5. Вычисляемые значения:
5.5.1. Вычисляется общее количество найденных карточек частных должностей (в соотв. с условиями отбора п.5.3.)



DECLARE
	@datefrom DATETIME,
	@dateto DATETIME

SET @datefrom = dbo.svf_get_first_day_month_before(GETDATE())
SET @dateto = dbo.svf_get_last_day_month_before(GETDATE());


WITH cte AS (
SELECT	
	sur_name + first_name + mid_name as [fio]
	, unid
	, dopuskcategory
	, dopuskcategoryperiod
	, dopuskapprovedate
	, dopuskenddate
	, 1 cnt
FROM [(Кадры)_(1)] WITH (NOLOCK)
WHERE
	reservedate = ''
	and
	status = 2 or status = 3
	and
	dopuskenddate < GETDATE()
	AND
	dopuskcategory <> ''
	AND
	dopuskcategory <> '-2'
)
, cte2 AS (
SELECT
	path
	, dbo.svf_make_LN_link_desc(server_name, universalid, dbreplicaid, unid) as [link]
	, targetaccess
	, stfuid
FROM [(Структура)_(1)] with (NOLOCK)
WHERE
	active = '1'
	and
	stfuid <> ''
)
, cte3 AS (
SELECT
	sur_name + first_name + mid_name as [fio_cte3]
	,  dbo.svf_make_LN_link_desc(server_name, universalid, dbreplicaid, unid) as [link]
	, dopuskcategory
	, dopuskcategoryperiod
	, shortpath
	, kadr.targetaccess
FROM [(Кадры)_(1)] kadr  WITH (NOLOCK)
	JOIN cte2 ON kadr.universalid = cte2.stfuid AND kadr.dopuskcategory > cte2.targetaccess
WHERE
	reservedate <> ''
	AND
	status in ('2', '3')
	AND
	dopuskenddate > GETDATE()
)
, cte4 AS (
SELECT 
	typeposition_name
	, 1 ctn
FROM [(Структура)_(profTypePosition)] with (NOLOCK)
WHERE
	activestaff = '1'
)
, cte5 AS (
SELECT
	shortpath
	, dbo.svf_make_LN_link(server_name, dbreplicaid ,universalid) as [link]
FROM [(Структура)_(1)] stru WITH (NOLOCK)
	JOIN cte4 ON stru.positioncategory_name = cte4.typeposition_name
WHERE
	active = '1'
	AND
	typeunit = '2'
	AND
	typeunit = '2'
)







вот код собири cte result
1. Перечень данных, попадающих в отчет:
1.1. Выборка п.1.4 (все поля)
1.2. Выборка п.3.4 (все поля)
1.3. Выборка п.4.4. (все поля)










