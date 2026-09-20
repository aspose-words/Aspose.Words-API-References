---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize method"
linktitle: "get_SecondSectionSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize метод. Получает или задает размер вторичной секции круговой диаграммы в процентах в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroup/get_secondsectionsize/
---
## ChartSeriesGroup::get_SecondSectionSize method


Получает или задает размер вторичной секции круговой диаграммы в процентах.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_SecondSectionSize()
```

## Примечания


Применяется к группам серий типов [PieOfPie](../../chartseriestype/) и [PieOfBar](../../chartseriestype/).

Диапазон допустимых значений от 5 до 200 включительно. Значение по умолчанию — 75.

## Примеры



Показывает, как создать и отформатировать диаграмму Pie of Pie.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::PieOfPie, 440, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
// Удалить автоматически сгенерированную серию.
chart->get_Series()->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3", u"Category 4"});
chart->get_Series()->Add(u"Series 1", categories, System::MakeArray<double>({11, 8, 4, 3}));

// Отформатировать диаграмму Pie of Pie.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> seriesGroup = chart->get_SeriesGroups()->idx_get(0);
seriesGroup->set_GapWidth(10);
seriesGroup->set_SecondSectionSize(77);

doc->Save(get_ArtifactsDir() + u"Charts.PieOfPieChart.docx");
```

## См. также

* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
