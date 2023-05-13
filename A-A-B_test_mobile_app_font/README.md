# Исследование поведения пользователей на изменение шрифта
Работая в стартапе(обучение), который продаёт продукты питания. Нужно разобраться, как ведут себя пользователи нашего мобильного приложения. Дизайнеры захотели поменять шрифты во всём приложении но что бы узнать как скажется на приложении нужно провести тесты и принять решение по результатам A/A/B-теста. Пользователей разбили на 3 группы: 2 контрольные со старыми шрифтами и одну экспериментальную — с новыми.

## Задачи
Подготовить и предобработать данные

Изучить и проверить данные

Изучить воронку продаж.

Изучу результаты эксперимента и провести A/A/B тест

### Были использованны библиотеки :
pandas, seaborn, matplotlib, scipy, numpy, plotly

### Итог

Были получены, проверены, подготовлены данные и проведены исследования

Была построена воронка на которой мы видили как пользователи не доходили но оплаты

Проверил что бы данные не пересекались

Так же я проверил и не нашел статистически значимых различий между группами А/А и после этого сделал A/B тест а так же с объединённой контрольной групп. Различий выявлено не было а это значит что гипотеза о том что изменение шрифта повлияет на метрики конверсии не подтвердилась.

Но так как пришлось отсеить данные за неделю у нас осталась только половинна времени изначально планированного иследования, я рекомендовал бы продлить иследования на неделю что бы накопить больше данных хотя я не ожидаю кардинальных изменений учитывая что p_value был давольно высок и не опускался ниже 0.42

### Проект был завершен