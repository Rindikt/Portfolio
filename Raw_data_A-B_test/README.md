# Проведение А/B теста

В моём распоряжении есть датасет с действиями пользователей, техническое задание и несколько вспомогательных датасетов.
Нужно оценить корректность проведения теста и проанализировать его результаты.
## Цель A/B теста
Проверить ожидаемый эффект: за 14 дней с момента регистрации в системе пользователи покажут улучшение каждой метрики не менее, чем на 10%:

## Задачи
1)Подключение библиотек, выгрузка, осмотр данных

2)Подготовка, предобработка данных

3)Оценка корректности проведения теста

3.1)Проверка пользователей попавших в обе группы

3.2)Проверка распределения пользователей по региону и устройствам регистрации

3.3)Проверка времени проведения теста на совпадение с маркетинговыми событиями

4)Проведение исследования

4.1)Количество событий на пользователя и нормальность распределения в выборках по дням

4.2)Распределение пользователей по датам регистрации

4.3)Количество событий на пользователя распределённые по эвентам

4.4)Построение воронки для группы А

4.5)построение воронки для группы B

5)А/B тест

### Были использованы библиотеки:
pandas, numpy, matplotlib, pyplot, math, scipy, stats, seaborn, plotly

### Итог
Я получил и предобработал данные.

Провел исследование и выяснил что распределения пользователей по устройствам регистрации между группами было равномерно, большинство пользователей предпочитают Android в два раза меньше PC и iPhone и меньше всего Mac.

Если смотреть по регионам, то у нас участвовали можно сказать только европейцы

Группы, а и b в тесте плохо сбалансированные так же у них разняться среднее количество событий на человека 6.9 против 5.5

Я построил воронки событий, они выглядят нормально, за исключением последнего шага в группе А. В ней больше покупок чем захода в корзину. Я пологою или системный сбой, или то что можно совершать покупки не заходя в корзину напрямую со страницы продукта.

Данных было мало, заявлено было что до 4‐го числа, но было лишь до 30го так же с 25го проходило маркетинговое событие и с 25го было заметно меньше пользователей

проведя z-test я обнаружил что есть статистическое различия в конверсии

Я посчитал конверсию и увидел её рост в группе B, но он ниже чем предполагалось прирост в просмотр карточек и конверсию в покупки составляет ~8.6, а вот конверсия в корзину продуктов увеличилась на ~14.5% и оправдала наши ожидания.

Как итог хочу сказать что тест скорее успешный, но группы были не сбалансированные и это вероятно повлияло на полученные выводы
