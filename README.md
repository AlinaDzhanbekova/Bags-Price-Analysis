## Анализ стоимости брендовых сумок 
В ходе этого проекта я беру данные о сумках с сайта https://oskelly.ru . Особенность этого сайта заключается в том, что это не просто интернет-магазин, а там содержится большое количество предложений от частных продавцов. Кто-то из них специально закупает сумки, которые в Росии не купить, в других странах, а кто-то перепродает сумки, которыми они пользовались, а кто-то продает те сумки, для получения возможности купить которые в бутике необходимо иметь впечатляющую историю покупок определенного бренда. Так или иначе рынок брендовых сумок на перепродаже не сильно отличается от того же рынка машин, так как есть множество факторов, влияющих на цену сумки.

В последнее время можно все чаще встретить людей, которые утверждают, что дорогие сумки, часы, ювелирные украшения - это хорошие инвестиции, так как с годами они только дорожают (при этом эти люди хоть и хранят такие вещи в хороших условиях, но тем не менее не перестают пользоваться ими). В связи с чем было бы особенно интересно посмотреть как цены б/у сумок отличаются от новых из бутика. 

Основной целью моего проекта является  разработка модели предсказания стоимости брендовых сумок на перепродаже, основанной на проверенных гипотезах и выявленных закономерностях, вытекающих из собранных данных. Мой проект состоит из 6 ключевых этапов, каждый из которых предоставляет из себя отдельную осмысленную часть, решающую определенную задачу исследования.

____
## Шаг 1. Сбор данных
> [parcing.ipynb](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/Parcing.ipynb)

Данные я собирала с помощью requests и selenium, так как для получения необходимой мне информации было необходимо нажать на кнопку на странице товара. Полученные данные я собрала в [таблицу](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/bag_data.csv) 

____
## Шаг 2. Предварительная обработка данных
Полученные данные подверглись дополнительной обработке, включающей заполнение пустых ячеек, приведение бинарных признаков к удобному для обработки виду. 
> [Предобработка данных.ipynb](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/%D0%9F%D1%80%D0%B5%D0%B4%D0%BE%D0%B1%D1%80%D0%B0%D0%B1%D0%BE%D1%82%D0%BA%D0%B0%20%D0%B4%D0%B0%D0%BD%D0%BD%D1%8B%D1%85.ipynb)

В ходе этого этапа была получена новая обработанная [таблица](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/bags_df_process.csv) 

____
## Шаг 3. EDA
В ходе этого этапа я визаулизировала данные по разным признакам, тем самым выявила несколько неожиданных взаимосвязей, натолкнувших меня на идеи по новым признакам.
> [EDA.ipynb](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/EDA.ipynb)

Также графики показали мне, что мой датасет стоит подредактировать для более хорошей визуализации и удачной дальнейшей работы. [Отредактированный датасет](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/df_afterEDA.csv) 

____
## Шаг 4. Создание новых признаков
В ходе этого этапа были созданы и визуализированы два категориальных признака (метод производства сумки и ценовая категория её бренда) и один бинарный - легендарность сумки
> [Создание новых признаков.ipynb](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/%D0%A1%D0%BE%D0%B7%D0%B4%D0%B0%D0%BD%D0%B8%D0%B5%20%D0%BD%D0%BE%D0%B2%D1%8B%D1%85%20%D0%BF%D1%80%D0%B8%D0%B7%D0%BD%D0%B0%D0%BA%D0%BE%D0%B2.ipynb)

Был получен [отредактированный датасет](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/df_new_factors.csv) 

____
## Шаг 5. Гипотезы
Исследуемые ранее закономерности помогли мне выдвинуть ряд гипотез, которые были проверены с помощью различных статистических методов.
> [Гипотезы.ipynb](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/%D0%93%D0%B8%D0%BF%D0%BE%D1%82%D0%B5%D0%B7%D1%8B.ipynb)

____
## Шаг 6. Машинное обучение
И в конце концов, я обучила ряд моделей: базовая модель линейной регрессии, Lasso-регрессию, Ridge-регрессию, Стохастический градиентный спуск (т.к. он вычислительно эффективней на большом наборе данных), Случайный лес и Градиентный бустинг. Проанализировала результаты работы моделей и заключила, что лучше всего с задачей предсказания цены сумки по заданным характеристикам справился градиентный бустинг.
> [Машинное обучение.ipynb](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/%D0%9C%D0%B0%D1%88%D0%B8%D0%BD%D0%BD%D0%BE%D0%B5%20%D0%BE%D0%B1%D1%83%D1%87%D0%B5%D0%BD%D0%B8%D0%B5.ipynb)

____
## Вывод
Гланвая цель моего проекта была успешно выполнена. Я построила модель, которая оценивает стоимость сумки по заданным параметрам. Также было выяснено, что сумки в отличном состоянии действительно не отличаются по цене от сумок из бутика всреднем. А также я выяснила, что 
1. В среднем люксовые сумки из кожи и ткани стоят одинаково;
2. Не менее 40% сумок Hermes являются легендарными моделями бренда;
3. Сумки без пыльника, в среднем стоят дешевле на 30% и более;
4. Среди сумок класса люкс сумки из бутика и сумки в отличном состоянии стоят всреднем одинаково;
5. Люксовые сумки без пыльника, в среднем стоят дешевле на 40% и более ;
6. Сумки Hermes без сертефиката подлинности в среднем стоят дешевле на 60% и более;
7. Люксовые сумки легендарных моделей без сертефиката подлинности в среднем стоят дешевле на 40% и более.
