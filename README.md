Распознавание ИИ этапов строительства.

Написать код на Python для внешней модели, чтобы обучить ее распознавать фотографии со стройплощадок
и определять этапы строительства ЖК для застройщиков, дольщиков и потенциальных покупателей.
Использует ее для контроля за внутренним состоянием квартир, ведет мультикамерный трекинг техники и не только.

• Решение должно быть воспроизводимо и запускаться под ОС Linux.

• Решение должно запускаться и работать на
CPU без использования GPU.

• В каждом изображении из тестовой выборки изображено не более одного здания. Кроме того, гарантируется, что крен (roll) камеры относительно здания не превышает
45 градусов.

• Не допускается использование специфичных
для Windows и macOS программ.

• Решение не должно обращаться к сторонним
ресурсам.

 // Рекомендации
1. Попробуйте использовать данные из открытых источников и/или сгенерировать синтетические
изображения.
2. Проанализируйте задачу и возможные проблемы. Например, влияет ли наличие эффекта рыбьего глаза (визуального эффекта, когда изображение сильно изменяется, становится вогнутым
при приближении к наблюдателю) на качество моделей или поворот камеры? Если да, то как это
исправить автоматически?

 // Наборы данных
Для обучения вам будет предоставлен небольшой размеченный датасет и дополнительный набор
неразмеченных изображений.
Датасет. Содержит 252 размеченных изображения для задачи Object Detection в формате COCO.
Разметка содержит следующие классы:
id  Класс   Описание
1   window  Кладка со светопрозрачной конструкцией (окном)
2   empty   Проем без кладки
3   filled  Проем с кладкой и оконным проемом
Дополнительный набор данных. Содержит набор неразмеченных изображений с камер. Вы можете воспользоваться им по своему усмотрению.

// Формат решения
Решения участников будут оцениваться автоматически тестирующей системой на публичном
и приватном тестовых датасетах.
В качестве решения от каждой команды ожидается:
1) ссылка на репозиторий с кодом решения с докер-контейнером (+ код для обучения моделей),
2) веса моделей,
3) презентация.

 // Критерии оценивания
Объективные критерии оценивания
Значение метрики качества на тестовом наборе данных. Основная метрика – mAP@.50 (mean
Average Precision) на тестовом наборе данных
Субъективные критерии оценивания
Субъективные критерии оценивания включают следующие критерии:
1. Насколько эффективно команда смогла идентифицировать и решить потенциальные проблемы,
такие как влияние искажений, шумов и погодных условий на качество работы алгоритмов.
2. Баланс между сложностью модели и качеством предсказаний: насколько оптимизирована модель с точки зрения вычислительных ресурсов и времени обработки.
3. Обоснование выбора архитектур моделей и алгоритмов.
4. Чистота и структура кода.

Проект не закончен т.к. не прошли 1й этап хакатона из-за этого не получили доступ к тестовой выборке и не хватает опыта закончить его самому.
Так же выяснилось что мощности моего ПК не хватает для быстрого обучения и переобучения модели.
