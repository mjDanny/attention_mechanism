# Проект: Генерация текста с использованием механизма внимания и LSTM

Этот проект демонстрирует, как можно использовать механизм внимания и LSTM для генерации текста на основе входных данных. В проекте реализована модель, которая обучается на наборе диалогов и способна генерировать ответы на заданные вопросы.

---

## 📋 Описание проекта

Проект состоит из нескольких ключевых компонентов:

1. **Загрузка и предобработка данных**  
   Данные загружаются из текстового файла, содержащего диалоги. Текст очищается и токенизируется для дальнейшего использования в модели.

2. **Механизм внимания**  
   Реализован механизм внимания, который помогает модели фокусироваться на важных частях входной последовательности при генерации текста.

3. **Кодировщик и декодировщик**  
   Используются LSTM слои для кодирования входных данных и декодирования их в выходные последовательности.

4. **Обучение модели**  
   Модель обучается на наборе диалогов, используя функцию потерь и оптимизатор Adam.

5. **Генерация текста**  
   После обучения модель может генерировать ответы на заданные вопросы, используя обученные параметры.

---

## 🛠 Используемые технологии

- **TensorFlow**: Основная библиотека для построения и обучения модели.
- **Keras**: Высокоуровневый API для работы с нейронными сетями.
- **NumPy**: Библиотека для работы с массивами и матрицами.
- **Sklearn**: Используется для разделения данных на обучающую и валидационную выборки.

---

## 🚀 Как использовать

### 1. Установка зависимостей
Убедитесь, что у вас установлены все необходимые библиотеки. Вы можете установить их с помощью pip:
```bash
pip install tensorflow numpy scikit-learn
```

### 2. Запуск обучения
Запустите блокнот `main(1).ipynb` для обучения модели. Обучение может занять некоторое время в зависимости от мощности вашего оборудования.

### 3. Генерация текста
После обучения модели вы можете использовать функцию `evaluate_sentence` для генерации ответов на заданные вопросы. Пример использования:
```python
sentence = "how did you become a senior developer?"
result, attention_plot = evaluate_sentence(sentence)
print('Перевод:', result)
```

### 4. Визуализация внимания
Вы также можете визуализировать карту внимания, чтобы увидеть, на какие части входного текста модель обращает больше внимания при генерации ответа:
```python
plot_attention_map(attention_plot, sentence, result)
```

---

## 📂 Структура проекта

- `main(1).ipynb`: Основной блокнот, содержащий весь код для загрузки данных, построения модели, обучения и генерации текста.
- `dialogs.txt`: Файл с диалогами, используемыми для обучения модели.

---

