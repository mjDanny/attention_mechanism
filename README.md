# Модель последовательного перевода текста с использованием внимания

## Описание

Этот проект реализует нейронную сеть для перевода текстов на основе последовательностей с использованием механизма внимания (Bahdanau, Luong). Проект включает код для загрузки данных, обработки текста, обучения модели и визуализации работы механизма внимания.

---

## Функционал

- Загрузка и очистка данных диалогов.
- Токенизация и подготовка текстов.
- Реализация механизма внимания (Bahdanau, Luong).
- Обучение модели кодировщика-декодировщика (encoder-decoder).
- Визуализация карты внимания для анализа переводов.
- Перевод введённых пользователем предложений.

---

## Используемые технологии

- **Python**
- **TensorFlow**
- **NumPy**
- **Matplotlib**
- **Scikit-learn**

---

## Установка и запуск

1. Установите зависимости:
   ```bash
   pip install tensorflow numpy matplotlib scikit-learn

    Загрузите данные:

```wget https://storage.yandexcloud.net/academy.ai/LLM/dialogs.txt```

Запустите обучение модели:

    python main.py

Пример использования

После обучения модели можно перевести предложение:
```
sentence = "how did you become a senior developer?"
result, attention_plot = evaluate_sentence(sentence)
print('Перевод:', result)
```

# Визуализация карты внимания
```
plot_attention_map(attention_plot, sentence, result)
```
Структура кода

    AttentionMechanism: Реализация механизмов внимания (Bahdanau, Luong general, Luong concat).
    TextEncoder: Кодировщик текста на основе LSTM.
    TextDecoder: Декодировщик текста с интеграцией механизма внимания.
    Обработка данных:
        clean_sentence: Очистка текста.
        load_dialogs: Загрузка текстов диалогов.
        tokenize_texts: Токенизация и преобразование текста в последовательности.
    Обучение:
        Реализация функции потерь.
        Петля обучения с использованием GradientTape.
    Перевод:
        Функция для генерации перевода.
        Визуализация карты внимания.
