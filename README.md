# Анализ развлекательного приложения Procrastinate Pro+

## Описание проекта

Вы — маркетинговый аналитик развлекательного приложения Procrastinate Pro+. Несмотря на огромные вложения в рекламу, последние несколько месяцев компания терпит убытки. Ваша задача — разобраться в причинах и помочь компании выйти в плюс.
Есть данные о пользователях, привлечённых с 1 мая по 27 октября 2019 года:
- лог сервера с данными об их посещениях,
- выгрузка их покупок за этот период,
- рекламные расходы.

Вам предстоит изучить:
- откуда приходят пользователи и какими устройствами они пользуются,
- сколько стоит привлечение пользователей из различных рекламных каналов;
- сколько денег приносит каждый клиент,
- когда расходы на привлечение клиента окупаются,
- какие факторы мешают привлечению клиентов.

### Описание данных

В вашем распоряжении три датасета:
- visits_info_short.csv — хранит лог сервера с информацией о посещениях сайта
- orders_info_short.csv — информацию о заказах
- costs_info_short.csv — информацию о расходах на рекламу.

Структура visits_info_short.csv:
- User Id — уникальный идентификатор пользователя,
- Region — страна пользователя,
- Device — тип устройства пользователя,
- Channel — идентификатор источника перехода,
- Session Start — дата и время начала сессии,
- Session End — дата и время окончания сессии.

Структура orders_info_short.csv:
- User Id — уникальный идентификатор пользователя,
- Event Dt — дата и время покупки,
- Revenue — сумма заказа.

Структура costs_info_short.csv:
- dt — дата проведения рекламной кампании,
- Channel — идентификатор рекламного источника,
- costs — расходы на эту кампанию.

### Инструкция по выполнению проекта

#### Шаг 1. Загрузите данные и подготовьте их к анализу
- загрузите данные о визитах, заказах и рекламных расходах из CSV-файлов в переменные. Пути к файлам:
    - /datasets/visits_info_short.csv. Скачать датасет;
    - /datasets/orders_info_short.csv. Скачать датасет;
    - /datasets/costs_info_short.csv. Скачать датасет.
- изучите данные и выполните предобработку. Есть ли в данных пропуски и дубликаты? Убедитесь, что типы данных во всех колонках соответствуют сохранённым в них значениям. Обратите внимание на столбцы с датой и временем.

#### Шаг 2. Задайте функции для расчёта и анализа LTV, ROI, удержания и конверсии.
- разрешается использовать функции, с которыми вы познакомились в теоретических уроках. Это функции для вычисления значений метрик, а также функции для построения графиков:
    - get_profiles() — для создания профилей пользователей,
    - get_retention() — для подсчёта Retention Rate,
    - get_conversion() — для подсчёта конверсии,
    - get_ltv() — для подсчёта LTV,
    - filter_data() — для сглаживания данных,
    - plot_retention() — для построения графика Retention Rate,
    - plot_conversion() — для построения графика конверсии,
    - plot_ltv_roi — для визуализации LTV и ROI.
    
#### Шаг 3. Исследовательский анализ данных
- составьте профили пользователей. Определите минимальную и максимальную даты привлечения пользователей.
- выясните, из каких стран пользователи приходят в приложение и на какую страну приходится больше всего платящих пользователей. - постройте таблицу, отражающую количество пользователей и долю платящих из каждой страны.
- узнайте, какими устройствами пользуются клиенты и какие устройства предпочитают платящие пользователи. Постройте таблицу, отражающую количество пользователей и долю платящих для каждого устройства.
- изучите рекламные источники привлечения и определите каналы, из которых пришло больше всего платящих пользователей. Постройте таблицу, отражающую количество пользователей и долю платящих для каждого канала привлечения.
- после каждого пункта сформулируйте выводы.

#### Шаг 4. Маркетинг
- посчитайте общую сумму расходов на маркетинг.
- выясните, как траты распределены по рекламным источникам, то есть сколько денег потратили на каждый источник.
- постройте график с визуализацией динамики изменения расходов во времени по неделям по каждому источнику. Затем на другом графике визуализируйте динамику изменения расходов во времени по месяцам по каждому источнику.
- узнайте, сколько в среднем стоило привлечение одного пользователя (CAC) из каждого источника. Используйте профили пользователей.
- напишите промежуточные выводы.

#### Шаг 5. Оцените окупаемость рекламы
- используя графики LTV, ROI и CAC, проанализируйте окупаемость рекламы. Считайте, что на календаре 1 ноября 2019 года, а в бизнес-плане заложено, что пользователи должны окупаться не позднее чем через две недели после привлечения. Необходимость включения в анализ органических пользователей определите самостоятельно.
- проанализируйте окупаемость рекламы c помощью графиков LTV и ROI, а также графики динамики LTV, CAC и ROI.
- проверьте конверсию пользователей и динамику её изменения. То же самое сделайте с удержанием пользователей. Постройте и изучите графики конверсии и удержания.
- проанализируйте окупаемость рекламы с разбивкой по устройствам. Постройте графики LTV и ROI, а также графики динамики LTV, CAC и ROI.
- проанализируйте окупаемость рекламы с разбивкой по странам. Постройте графики LTV и ROI, а также графики динамики LTV, CAC и ROI.
- проанализируйте окупаемость рекламы с разбивкой по рекламным каналам. Постройте графики LTV и ROI, а также графики динамики LTV, CAC и ROI.
- ответьте на такие вопросы:
    - окупается ли реклама, направленная на привлечение пользователей в целом?
    - какие устройства, страны и рекламные каналы могут оказывать негативное влияние на окупаемость рекламы?
    - чем могут быть вызваны проблемы окупаемости?
    - напишите вывод, опишите возможные причины обнаруженных проблем и промежуточные рекомендации для рекламного отдела.

#### Шаг 6. Напишите выводы
- выделите причины неэффективности привлечения пользователей.
- сформулируйте рекомендации для отдела маркетинга.
