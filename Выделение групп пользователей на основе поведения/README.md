# Мобильные приложения. Выделение групп пользователей на основе поведения

### Цель заказчика: 
Создать более точный механизм взаимодействия с пользователями и повысить вовлеченность

### Задача исследователя:
Проанализировать поведение пользователей в мобильном приложениии и сегментировать их на разные группы

### Подготовила материалы:
- [💾 Ссылка на презентацию](https://disk.yandex.ru/d/kIH4x8kS24CWoQ)
- [📊 Tableau](https://public.tableau.com/app/profile/ekaterina.koroleva/viz/final_project_16872159046860/sheet2?publish=yes)

# Выводы

### EDA:
 - В нашем распоряжении данные с 7 октября 2019 г. по 3 ноября 2019 г. (4 293 уникальных пользователя)
 - Они распределены по источникам: `yandex` (45.1% - 1 934), `other` (28.7% - 1 230), `google` (26.3% - 1 129)  
 - В целом можно сказать, что после скачивания приложения, пользователи довольно часто возвращаются в него
 - Общая конверсия растёт: от 17.99% в первый день «жизни» пользователей до 22.22% на пятнадцатый день
 - Среднее время, которое пользователь проводит в приложении, составляет - 16 минут. За это время он совершает примерно 2 сессии с перерывом >40 минут. Среднее время одной такой сессии - около 6 минут
 - Характер распределения данных по датам, дням недели и событиям достаточно ровный, аномалий не выявлено
 
### Сегментировала пользователей на 3 группы по источникам установки приложения:

Ожидала, что пользователи из `yandex` покажут лучший результат, чем остальные, тк это самая многочисленная группа пользователей. Но вот что вышло:

- 🙂 пользователи из `yandex` чаще остальных делают целевое событие
- 🤔 однако все источники в совокупности показывают примерно одинаковые показатели удержания

### Проверила гипотезы:

1. Группы `yandex` и `google` демонстрируют разную конверсию в просмотры контактов:
> высока вероятность, что между пользователями, установившими приложение из yandex или google, нет значимой разницы. Делаю вывод, что источник установки на конверсию не влияет
    

2. Среднее время, проведенное в приложении, у групп пользователей, совершивших целевое действие (просмотр контактов) и не совершивших его - равно:  
> отвергаю нулевую гипотезу и предполагаю, что среднее время, проведенное в приложении, у групп пользователей, совершивших целевое действие (просмотр контактов) и не совершивших его - различается


# Рекомендации:

- проверить корелляцию времени в приложении и отдельных событий - так можно понять на что пользователи тратят больше всего времени и как оптимизировать его
- проверить оказывают ли влияние определенные события (или их отсутствие) на совершение целевого действия
- сравнить стоимость привлечения пользователей из разных источников. Не слишком ли она велика?
- стимулировать активность пользователей в выходные

- количество событий, связанных с просмотром объявления, почти в 4 раза больше, чем действий с просмотром фото. Здесь вероятны 3 сценария:
    - Пользователь не считает нужным просматривать фото, так как объявление содержит достаточно информации для принятия решения о покупке
    - Пользователь предпочитает просматривать только объявления, а не фотографии
    - Фото нет в объявлении - а это уже может оказывать существенное влияние на принятие решения. Рекомендую исследовать это дополнительно
