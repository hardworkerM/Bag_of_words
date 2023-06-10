# Мешок слов

Классический алгоритм для классификации текстов (документов) на основе частоты встречающихся в нём слов\
Реализовано при помощи Python, классификация осуществлялось логистической регрессией.

## Принцип алгоритма
Это метод классификации документа на основе его содержания.\
Сначала текст разбивается на слова, убираются символы, не дающие смысловую нагрузку слова - частотность которых не зависит от темы документы (часто это предлоги "и", "или" и тд.). 
Далее подсчитывается частота упоминания слова во всех документах обучающей выборки и создаётся таблица с признаками - словами и частотой по каждому документу.
В конце можно отобрать тов 25% слов по частоте и включить их в обучающую выборку.

<img src='https://github.com/hardworkerM/Bag_of_words/blob/main/Dict_example.png' width="600">

Эти данные используются для обучения классифицирующих ML моделей.

В моем примере я использовал LogisticRegression, RandomForest тоже подходит. 

### Вывод

Алгоритм прост в реализации, интуитивно понятен, с задачей классификации справляется, но не способен уловить сочетания слов и сложные структуры.
