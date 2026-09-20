---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth метод"
linktitle: "get_GapWidth"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth метод. Получает или задает процент ширины промежутка между элементами диаграммы в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroup/get_gapwidth/
---
## ChartSeriesGroup::get_GapWidth method


Получает или задает процент ширины промежутка между элементами диаграммы.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_GapWidth()
```

## Примечания


Применяется только к группам рядов типов bar, column, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall и funnel.

Диапазон допустимых значений от 0 до 500 включительно. Для групп рядов на основе bar/column свойство представляет собой расстояние между кластерами столбцов в процентах от их ширины. Для диаграмм pie-of-pie и bar-of-pie это расстояние между первичной и вторичной секциями диаграммы.

## Примеры



Покажите, как настроить ширину промежутка и перекрытие.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = shape->get_Chart()->get_SeriesGroups()->idx_get(0);

// Установите ширину промежутка столбцов и перекрытие.
seriesGroup->set_GapWidth(450);
seriesGroup->set_Overlap(-75);

doc->Save(get_ArtifactsDir() + u"Charts.ConfigureGapOverlap.docx");
```

## См. также

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
