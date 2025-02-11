**Проект: Генерация текстовых отзывов с использованием нейронной сети**


Краткое описание


Цель проекта — разработка нейронной сети, которая генерирует текстовые отзывы о различных местах (жилые комплексы, рестораны и другие объекты) на основе нескольких входных параметров, таких как категория места, средний рейтинг и ключевые слова. Модель будет использовать эти параметры для создания текстов, которые отражают общее впечатление о месте.

Данные
Для обучения использован датасет Geo Reviews Dataset 2023, содержащий информацию о различных объектах, включая категории, рейтинги и текстовые отзывы. Этот датасет служит основой для обучения модели, позволяя генерировать текстовые отзывы в ответ на входные данные, такие как категория, рейтинг и название объекта.

Описание модели
Для задачи генерации текстов используется модель RuGPT-3 Small. Модель обучена на данных с учетом категорий, рейтингов и ключевых слов, что позволяет генерировать релевантные и разнообразные текстовые отзывы, соответствующие различным входным данным.


Предобработка данных:

Данные были очищены от лишних элементов и приведены к единому формату.
Для токенизации был использован GPT2Tokenizer, что позволило преобразовать текст в числовые представления для обучения модели.
Обучение модели:

Для обучения использовалась библиотека transformers и предобученная модель RuGPT-3 Small.
Модель была дообучена на основе входных данных, что позволило улучшить её способность генерировать текстовые отзывы с учетом различных параметров.
Генерация текста:

Тексты генерировались с использованием различных параметров (например, temperature, top_k, top_p) для контроля стиля и разнообразия сгенерированного контента.
После генерации текста применялась очистка от категорий и других меток, что делало текст более естественным.
Оценка модели:

Модель была протестирована на тестовом наборе данных, сгенерированные тексты были оценены по качеству и разнообразию.
Состав команды
Единственный участник — все задачи выполнялись одним человеком, включая разработку модели, обработку данных и документацию.

Оценка архитектуры решения
Сильные стороны:

Использование предобученной модели: RuGPT-3 Small позволяет быстро обучить модель с учетом специфики русского языка.
Гибкость генерации: Параметры генерации, такие как temperature, top_k, и top_p, позволяют контролировать стилистику текста.
Отдельная очистка текста: Очистка сгенерированного текста от категорий и рейтингов повышает его естественность.
Области для улучшений:

Предобработка данных: Улучшение этапа предобработки данных, включая удаление шумовых слов и нормализацию текста.
Обогащение датасета: Добавление большего числа примеров для каждой категории и рейтинга может улучшить качество модели.
