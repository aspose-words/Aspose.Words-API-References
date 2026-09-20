---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap метод"
linktitle: "get_Overlap"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap метод. Получает или задает процент перекрытия столбцов или полос рядов в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroup/get_overlap/
---
## ChartSeriesGroup::get_Overlap method


Получает или задает процент того, насколько перекрываются столбцы или колонки серии.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Overlap()
```

## Примечания


Применяется к группам рядов всех типов столбчатых и колонных диаграмм.

Диапазон допустимых значений от -100 до 100 включительно. Значение 0 указывает, что между столбцами/полосами нет промежутка. Если значение -100, расстояние между столбцами/полосами равно их ширине. Значение 100 означает, что столбцы/полосы полностью перекрываются.

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
