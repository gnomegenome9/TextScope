# Выявление трендов арктических исследований на основе открытых данных социальных сетей

Данный проект выполнен в рамках магистерской диссертации на тему:
**«Разработка методики выявления трендов арктических исследований на основе открытых данных социальных сетей»**.

Целью проекта является разработка методики для анализа текстовых данных из различных источников (социальные сети, новостные агрегаторы, научные статьи) с последующим выделением ключевых тем, прогнозированием их развития и сравнением полученных результатов между источниками.

## Структура проекта
```bash
01_collectors/
├── vk.ipynb # Сбор данных из VKontakte
├── cyberleninka.ipynb # Сбор данных из Cyberleninka
├── gnews.ipynb # Сбор данных из Google News
01_twitter_data.ipynb # Анализ готовых датасетов с Kaggle (Twitter)
02_preprocessing.ipynb # Предобработка данных из VK, Cyberleninka, Google News
03_keywords.ipynb # Выделение ключевых слов для Cyberleninka
04_topic_modeling.ipynb # Тематическое моделирование: BERTopic (VK, Google News) и LDA (Cyberleninka)
05_forecasting.ipynb # Прогнозирование трендов топ-5 тем для всех источников
06_comparison_between_sources.ipynb # Сравнение результатов между источниками по различным метрикам
```
## Порядок запуска ноутбуков

1. `01_collectors/vk.ipynb`
2. `01_collectors/cyberleninka.ipynb`
3. `01_collectors/gnews.ipynb`
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
- **Cyberleninka**
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

В корне Google Диска (`MyDrive`) должен находиться текстовый файл `keywords.txt`, содержащий ключевые слова или фразы для поиска.
Формат — по одному слову или фразе на строку:
```
изменение климата
Арктика
устойчивое развитие
```

Все результаты, графики и модели сохраняются в папку `TextScope`, которая создается автоматически.

Проект разрабатывался и тестировался в среде **Google Colab**. Все необходимые зависимости устанавливаются внутри ноутбуков. Для запуска:
1. Откройте каждый `.ipynb` файл в Google Colab.
2. Следуйте инструкциям в блокноте.
3. Запускайте ноутбуки строго в указанном выше порядке.

## Открыть в Google Colab

| Ноутбук | Ссылка |
|---------|--------|
| Сбор данных VK | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/01_collectors/vk.ipynb) |
| Сбор данных Cyberleninka | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/01_collectors/cyberleninka.ipynb) |
| Сбор данных Google News | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/01_collectors/gnews.ipynb) |
| Анализ Twitter данных | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/01_twitter_data.ipynb) |
| Предобработка данных | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/02_preprocessing.ipynb) |
| Выделение ключевых слов (Cyberleninka) | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/03_keywords.ipynb) |
| Тематическое моделирование | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/04_topic_modeling.ipynb) |
| Прогнозирование трендов | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/05_forecasting.ipynb) |
| Сравнение источников | [Открыть](https://colab.research.google.com/github/gnomegenome9/TextScope/blob/main/06_comparison_between_sources.ipynb) |
