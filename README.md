# Выявление трендов арктических исследований на основе открытых данных социальных сетей

Данный проект выполнен в рамках магистерской диссертации на тему:
**«Разработка методики выявления трендов арктических исследований на основе открытых данных социальных сетей»**.

Целью проекта является разработка методики для анализа текстовых данных из различных источников (социальные сети, новостные агрегаторы, научные статьи) с последующим выделением ключевых тем, прогнозированием их развития и сравнением полученных результатов между источниками.

## Структура проекта

01_collectors/
├── 01_vk_data.ipynb # Сбор данных из VKontakte
├── 02_cyberleninka_data.ipynb # Сбор данных из Cyberleninka
├── 03_google_news_data.ipynb # Сбор данных из Google News
01_twitter_data.ipynb # Анализ готовых датасетов с Kaggle (Twitter)
02_preprocessing.ipynb # Предобработка данных из VK, Cyberleninka, Google News
03_keywords.ipynb # Выделение ключевых слов для Cyberleninka
04_topic_modeling.ipynb # Тематическое моделирование: BERTopic (VK, Google News) и LDA (Cyberleninka)
05_forecasting.ipynb # Прогнозирование трендов топ-5 тем для всех источников
06_comparison_between_sources.ipynb # Сравнение результатов между источниками по различным метрикам

## Порядок запуска ноутбуков

1. `01_collectors/01_vk_data.ipynb`
2. `01_collectors/02_cyberleninka_data.ipynb`
3. `01_collectors/03_google_news_data.ipynb`
4. `01_twitter_data.ipynb`
5. `02_preprocessing.ipynb`
6. `03_keywords.ipynb`
7. `04_topic_modeling.ipynb`
8. `05_forecasting.ipynb`
9. `06_comparison_between_sources.ipynb`

> Все необходимые библиотеки устанавливаются непосредственно внутри каждого Jupyter Notebook (Google Colab).

## Используемые данные и ресурсы

- **VK API**
- **Google News**
- **Cyberleninka API**
- **Kaggle Datasets**:
  - [Sentiment140](https://www.kaggle.com/datasets/kazanova/sentiment140)
  - [Tweets Dataset](https://www.kaggle.com/datasets/bhavikjikadara/tweets-dataset)
  - [Climate Change Twitter Dataset](https://www.kaggle.com/datasets/edqian/twitter-climate-change-sentiment-dataset)
  - [Climate Sentiment Twitter](https://www.kaggle.com/datasets/joseguzman/climate-sentiment-in-twitter)
  - [Climate Change Tweets](https://www.kaggle.com/datasets/die9origephit/climate-change-tweets)

## Используемые библиотеки

- **Сбор и обработка данных**:  
  `VK API`, `gdown`, `chardet`, `pandas`, `googletrans`, `Selenium`, `chromeDriver`, `fake-useragent`, `aiohttp`

- **Обработка текста**:  
  `NLTK`, `pymorphy2`, `summa`, `SentenceTransformer`

- **Анализ и моделирование**:  
  `sklearn`, `BERTopic`, `Gensim`, `pyLDAvis`

- **Визуализация**:  
  `Plotly`, `ipywidgets`

## Инструкции по запуску

Проект разрабатывался и тестировался в среде **Google Colab**. Все необходимые зависимости устанавливаются внутри ноутбуков. Для запуска:
1. Откройте каждый `.ipynb` файл в Google Colab.
2. Следуйте инструкциям в блокноте.
3. Запускайте ноутбуки строго в указанном выше порядке.
