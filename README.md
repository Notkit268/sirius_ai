# Сириус.ИИ, 2023

## sirius_ai.ipynb - основной ноутбук

Мы опробовали различные модели (в том числе глубокого обучения), но SVD показал отличные результаты за короткое время, поэтому мы выбрали его.
В ноутбуке сначала идет обработка данных.
Затем алгоритм SVD (с нахождением похожих фильмов и получением рекомендаций фильмов для пользователей).
В конце можно обучить DeepFM и FNN

Данных очень много (25 миллионов отзывов), поэтому пришлось взять 3 миллиона последних, иначе переполнялась бы память.

Результаты на тестовой выборке:
RMSE: 0.8692
MAE:  0.6677

Разбиение на train/val/test произведено по времени (отзывы из теста более новые, чем отзывы из валидации. Отзывы из валидации более новые, чем отзывы из трейна) для моделирования использования модели в реальных условиях. Если разбивать с перемешиванием, то метрики значительно растут.
