## Анализ стоимости брендовых сумок 
В ходе этого проекта я беру данные о сумках с сайта https://oskelly.ru . Особенность этого сайта заключается в том, что это не просто интернет-магазин, а там содержится большое количество предложений от частных продавцов. Кто-то из них специально закупает сумки, которые в Росии не купить, в других странах, а кто-то перепродает сумки, которыми они пользовались, а кто-то продает те сумки, для получения возможности купить которые в бутике необходимо иметь впечатляющую историю покупок определенного бренда. Так или иначе рынок брендовых сумок на перепродаже не сильно отличается от того же рынка машин, так как есть множество факторов, влияющих на цену сумки.

В последнее время можно все чаще встретить людей, которые утверждают, что дорогие сумки, часы, ювелирные украшения - это хорошие инвестиции, так как с годами они только дорожают (при этом эти люди хоть и хранят такие вещи в хороших условиях, но тем не менее не перестают пользоваться ими). В связи с чем было бы особенно интересно посмотреть как цены б/у сумок отличаются от новых из бутика. 

Основной целью моего проекта является  разработка модели предсказания стоимости брендовых сумок на перепродаже, основанной на проверенных гипотезах и выявленных закономерностях, вытекающих из собранных данных. Мой проект состоит из 6 ключевых этапов, каждый из которых предоставляет из себя отдельную осмысленную часть, решающую определенную задачу исследования.

____
## `Сбор данных`
> [parcing.ipynb](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/Parcing.ipynb)

Данные я собирала с помощью requests и selenium, так как для получения необходимой мне информации было необходимо нажать на кнопку на странице товара. Полученные данные я собрала в [таблицу](https://github.com/AlinaDzhanbekova/Bags-Price-Analysis/blob/main/bag_data.csv) 
