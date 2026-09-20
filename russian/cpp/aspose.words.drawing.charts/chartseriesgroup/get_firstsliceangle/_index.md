---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle method"
linktitle: "get_FirstSliceAngle"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle method. Получает или задает угол в градусах первой части родительской круговой диаграммы в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroup/get_firstsliceangle/
---
## ChartSeriesGroup::get_FirstSliceAngle method


Получает или задает угол, в градусах, первого сектора родительской круговой диаграммы.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_FirstSliceAngle()
```

## Примечания


Применяется к группам серий типов [Pie](../../chartseriestype/), [Pie3D](../../chartseriestype/) и [Doughnut](../../chartseriestype/).

Диапазон допустимых значений от 0 до 360 включительно. Значение по умолчанию — 0.

## Примеры



Показывает, как создать и отформатировать диаграмму Doughnut.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Doughnut, 400, 400);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Удалить автоматически сгенерированную серию.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({4, 2, 5}));

// Отформатировать диаграмму Doughnut.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_DoughnutHoleSize(10);
seriesGroup->set_FirstSliceAngle(270);

doc->Save(get_ArtifactsDir() + u"Charts.DoughnutChart.docx");
```

## См. также

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
