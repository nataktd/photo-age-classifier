# Обработка фотографий покупателя
# Описание проекта
В проекте рассматривается задача определения приблизительного возраста человека на фотографиях с помощью компьютерного зрения. Задача имеет практическое применение для сетевого супермаркета "Хлеб-Соль", который хочет использовать фотофиксацию в прикассовой зоне для определения возраста клиентов. Это позволит анализировать покупки, предлагать товары, соответствующие возрастной группе, и контролировать продажу алкоголя.

# Цель:
Целью проекта является создание модели машинного обучения, которая по фотографии человека определит его приблизительный возраст. Метрикой качества модели будет `Mean Absolute Error` (MAE).

# Описание данных

Данные взяты с сайта ChaLearn Looking at People и состоят из изображений лиц людей с указанием их реального возраста. Данные представлены в формате:

- Папка `final_files` с изображениями лиц.
- CSV-файл `labels.csv`, содержащий две колонки:
- `file_name` (имя файла с изображением) 
- `real_age` (реальный возраст человека на фотографии).

# Краткий план работы:

- Исследовательский анализ данных.
- Подготовка данных к обучению.
- Обучение нейронной сети для определения возраста.
- Оценка качества модели с использованием `MAE`.
- Выводы и анализ результатов обучения модели.

# Использованные библиотеки для обработки изображений:
- `pandas`- обработка и анализ данных.
- `numpy` - вычислительные операции над массивами.
- `matplotlib.pyplot` - визуализация данных в виде графиков.
- `seaborn` - улучшенная визуализация данных.
- `tensorflow.keras.preprocessing.image.ImageDataGenerator` - библиотека для генерации увеличенных данных, включая масштабирование, что применяется для предобработки изображений перед обучением нейронных сетей.
- `tensorflow.keras.applications.ResNet50` - предварительно обученная модель ResNet50, используемая для определения возраста. ResNet50 — это глубокая сверточная нейронная сеть, предназначенная для работы с изображениями.

# Итоги

Проект успешно решает задачу определения возраста на фотографиях. Модель достигла MAE равного 6.18, удовлетворяя поставленным требованиям.

В ходе анализа данных были выявлены некоторые проблемы, такие как разнородность и качество фотографий, наличие выбросов и недостаток данных для возрастной группы старше 60 лет.

При внедрении модели в бизнес следует учитывать, что она может допускать ошибки в предсказании возраста на несколько лет (6лет).

