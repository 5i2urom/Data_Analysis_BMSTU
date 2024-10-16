# Лабораторная работа №2  
## Бинарная классификация демографических трендов

### Описание

В данной лабораторной работе вы решаете задачу бинарной классификации, используя таргет `Ybin`, который представляет собой бинарную переменную. Значение 1 обозначает регион с выраженностью демографических трендов.

### Этапы выполнения работы

1. **Разделение данных**  
   Разделите данные на обучающую (85%) и тестовую (15%) выборки случайным образом. Желательно использовать метод, который сохраняет распределение таргета в каждой подвыборке.

2. **Нормирование (масштабирование) данных**  
   Выполните нормирование (масштабирование) исходных данных. Учтите, что данные для нормализации рассчитываются только на основе обучающей выборки.

3. **Модель kNN**  
   - Используйте библиотеку `sklearn` для выполнения fit-predict модели k ближайших соседей (kNN).
   - Переберите по сетке параметр числа соседей для определения наилучшего значения на тестовой выборке.

4. **Модель логистической регрессии**  
   - С помощью библиотеки `sklearn` выполните fit-predict модели логистической регрессии.
   - Переберите по сетке параметр регуляризации для определения наилучшего значения на тестовой выборке.

5. **Модель дерева решений**  
   - Используйте библиотеку `sklearn` для выполнения fit-predict модели дерева решений.
   - Переберите по сетке параметр глубины дерева для определения наилучшего значения на тестовой выборке.

6. **Дополнительно: Случайный лес**  
   - С помощью библиотеки `sklearn` выполните fit-predict модели случайного леса.
   - Переберите по сетке параметр глубины дерева для определения наилучшего значения на тестовой выборке (желательно, но не обязательно).

7. **Сравнение качества моделей**  
   - Сравните качество всех моделей на обучающей и тестовой выборках по следующим метрикам: Accuracy, ROC-AUC, Precision, Recall, F1-мера.
   - Учтите, что 4 из 5 метрик требуют определения порога отсечения по вероятности. Рекомендуется использовать среднее значение полученных вероятностей.

8. **Анализ качества моделей**  
   - Проанализируйте различия в качестве между моделями и определите, какие модели сильно выражают переобучение.

9. **Сравнение важности признаков**  
   - Сравните полученную важность признаков в модели логистической регрессии, в модели деревьев решений и в случайном лесе.
   - Для деревьев решений используйте ключ `feature_importances` у обученной модели для анализа важности признаков.

### Используемые технологии

- **Python**
- **pandas**
- **NumPy**
- **scikit-learn**
