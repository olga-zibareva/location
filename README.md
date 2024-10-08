Обучение линейной модели МО. Расчёт метрик бизнеса. Анализ возможной прибыли и рисков техникой `Bootstrap`. Библиотеки `pandas`, `numpy`, `matplotlib`, `seaborn`, `sklearn`.  

## Выбор локации для скважины

Мы работаем в добывающей компании «ГлавРосГосНефть». Нужно решить, где бурить новую скважину.  

Нам предоставлены пробы нефти в трёх регионах: в каждом 10 000 месторождений, где измерили качество нефти и объём её запасов. Нужно построить модель машинного обучения, которая поможет определить регион, где добыча принесёт наибольшую прибыль. Необходимо проанализировать возможную прибыль и риски.  

Шаги для выбора локации:  
- В избранном регионе ищут месторождения, для каждого определяют значения признаков;  
- Строят модель и оценивают объём запасов;  
- Выбирают месторождения с самым высокими оценками значений. Количество месторождений зависит от бюджета компании и стоимости разработки одной скважины;  
- Прибыль равна суммарной прибыли отобранных месторождений.  

**Ход работы**  

1. Данные загружены, получена первичная информация.  
2. Выполнена предобработка данных (проверка на пропуски, дубликаты, некорректный тип данных).  
3. Выполнен исследовательский анализ данных (проверено распределение, корреляция). Предполагаем, что линейная модель сработает хорошо.  
4. По каждому региону обучена модель `LinearRegression`, её качество оценено метрикой `mse`, рассчитан прогнозный запас сырья в каждом регионе.  
5. Рассчитаны показатели прибыли и рисков в каждом регионе техникой `Bootstrap`.  
6. Выбран лучший регион для разработки.  

**Основные выводы:** Второй регион лучше всего подходит для разработки, так как риск убытков во втором регионе самый низкий, а ожидаемая прибыль самая высокая.