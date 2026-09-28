---
title: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class"
linktitle: "BubbleSizeCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::BubbleSizeCollection class. Представляет коллекцию размеров пузырей для серии диаграммы на C++."
type: docs
weight: 3500
url: /ru/cpp/aspose.words.drawing.charts/bubblesizecollection/
---
## BubbleSizeCollection class


Представляет коллекцию размеров пузырей для серии диаграммы.

```cpp
class BubbleSizeCollection : public System::Collections::Generic::IEnumerable<double>
```

## Методы

| Метод | Описание |
| --- | --- |
| [get_Count](./get_count/)() | Возвращает количество элементов в этой коллекции. |
| [get_FormatCode](./get_formatcode/)() | Получает или задает код формата, применяемый к размерам пузырей. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект перечислителя. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Получает или задает значение размера пузыря по указанному индексу. |
| [idx_set](./idx_set/)(int32_t, double) | Получает или задает значение размера пузыря по указанному индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Сеттер для [Aspose::Words::Drawing::Charts::BubbleSizeCollection::get_FormatCode](./get_formatcode/). |
| static [Type](./type/)() |  |
## Примечания


Коллекция позволяет только изменять размеры пузырей. Чтобы добавить или вставить новые значения в серию диаграммы, или удалить значения, можно использовать соответствующие методы класса [ChartSeries](../chartseries/).

Пустые значения размеров пузырей представлены как **NaN**.

## См. также

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
