# Лабораторная работа 4  
## Определение семантической окраски твитов

### Описание

Цель данной лабораторной работы — подготовка и анализ набора данных для обучения моделей классификации текста с использованием различных методов предобработки. Вы будете работать с данными из набора твитов для определения их семантической окраски (положительной или отрицательной).

### Исходные данные

Обучающие и тестовые выборки можно найти по ссылке: [Rusentitweet GitHub](https://github.com/sismetanin/rusentitweet).

### Этапы выполнения

1. **Фильтрация данных**  
   Оставьте в выборках только строки с классами `positive` и `negative`.

2. **Очистка данных**  
   Определите и реализуйте методы очистки набора данных, удаляя избыточную информацию, например, ссылки на аккаунты других пользователей.

3. **Стемминг и мешок слов**  
   - Осуществите стемминг подготовленного набора данных и преобразуйте каждый твит в мешок слов.
   - Кастомные преобразования обучайте только на **обучающей выборке**. Если преобразование необучаемое, применяйте его в одинаковой форме для обеих выборок.

4. **Count-матрица и tf-idf**  
   - Составьте Count-матрицу и рассчитайте на ней **tf-idf**.
   - tf-idf — это обучаемое преобразование, которое нужно **зафитить на обучающих данных** и применить к тестовым.

5. **Обучение моделей**  
   Обучите модели логистической регрессии и случайного леса на обучающей выборке и примените их к тестовым данным. 
   - Посчитайте качество на обеих выборках и сравните результаты.
   - Определите наиболее важные признаки (слова).

6. **Лемматизация вместо стемминга**  
   Вместо стемминга осуществите лемматизацию и повторите пункты 3-5 с учетом нового типа подготовки данных.

7. **Сравнение результатов**  
   Сравните результаты по качеству и по наиболее важным признакам (словам) между двумя подходами (стемминг и лемматизация).

### Используемые технологии

- **Python** 
- **pandas**
- **scikit-learn** 
- **NLTK/Spacy** 
