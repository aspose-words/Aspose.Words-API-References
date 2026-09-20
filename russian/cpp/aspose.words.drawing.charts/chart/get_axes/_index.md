---
title: "Aspose::Words::Drawing::Charts::Chart::get_Axes метод"
linktitle: "get_Axes"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::Chart::get_Axes метод. Возвращает коллекцию всех осей этой диаграммы в C++."
type: docs
weight: 1500
url: /ru/cpp/aspose.words.drawing.charts/chart/get_axes/
---
## Chart::get_Axes method


Получает коллекцию всех осей этой диаграммы.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartAxisCollection> Aspose::Words::Drawing::Charts::Chart::get_Axes()
```


## Примеры



Показывает, как работать с коллекцией осей.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Скрыть основные линии сетки на первичной и вторичной осях Y.
for (auto&& axis : System::IterateOver(chart->get_Axes()))
{
    if (axis->get_Type() == Aspose::Words::Drawing::Charts::ChartAxisType::Value)
    {
        axis->set_HasMajorGridlines(false);
    }
}

doc->Save(get_ArtifactsDir() + u"Charts.AxisCollection.docx");
```

## См. также

* Class [ChartAxisCollection](../../chartaxiscollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
