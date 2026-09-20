---
title: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups метод"
linktitle: "get_SeriesGroups"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups метод. Предоставляет доступ к коллекции групп серий этой диаграммы в C++."
type: docs
weight: 6500
url: /ru/cpp/aspose.words.drawing.charts/chart/get_seriesgroups/
---
## Chart::get_SeriesGroups method


Обеспечивает доступ к коллекции групп рядов этой диаграммы.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroupCollection> Aspose::Words::Drawing::Charts::Chart::get_SeriesGroups()
```


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

* Class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
