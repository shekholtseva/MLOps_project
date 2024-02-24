# MLOps_project
  1. Формулировка задачи: что вы делаете и зачем это нужно?\
     
     Сервис автоматической фильтрации новостей для автоматического выявления риск-факторов по компаниям с целью переоценки банковских резервов и капитала в реальном времени.
  3. Данные: откуда вы их собираетесь брать (конкретные ссылки), какие у них есть особенности, что может стать проблемой, почему этих данных достаточно для решения поставленной задачи?\
     Новостной поток - выгрузка компании интерфакс. Целовое событие дефолта - база банкротств "Коммерсант" и база кредитной истории ОКБ
  4. Подоход к моделированию: какие модели (имена нейросетей, библиотек) вы будете использовать в решении вашей задачи, какова будет конфигурация решения? Можно приложить схему.\
     Архитектура найронной сети в проработке. Пробуем различные варианты реализации. Это будет pytorch.
  5. Способ предсказания: после обучения модели вам нужно будет обернуть модель в продакшен пайплайн - какие шаги в нём необходимы, как вы видите финальное применение? Схема также не будет лишней.\
     Данные будут поступать по api скан-интерфакс. Запрос происходит по ИНН компании. Далее модель обрабатывает новости и выдает вероятностную оценку дефолта на основе новостей. Эта оценка встраивается в основную модель на rf или бустинге и получается финальная оценка вероятности дефолта компании.
