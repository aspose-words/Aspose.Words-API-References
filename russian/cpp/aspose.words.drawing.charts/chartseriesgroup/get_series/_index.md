---
title: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Series method"
linktitle: "get_Series"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Series method. Возвращает коллекцию серий, принадлежащих этой группе серий, в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.drawing.charts/chartseriesgroup/get_series/
---
## ChartSeriesGroup::get_Series method


Получает коллекцию серий, принадлежащих этой группе серий.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> Aspose::Words::Drawing::Charts::ChartSeriesGroup::get_Series()
```


## Примеры



Показывает, как работать со вторичной осью диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 450, 250);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();

// Удалить автоматически сгенерированную серию.
series->Clear();

auto categories = System::MakeArray<System::String>({u"Category 1", u"Category 2", u"Category 3"});
series->Add(u"Series 1 of primary series group", categories, System::MakeArray<double>({2, 3, 4}));
series->Add(u"Series 2 of primary series group", categories, System::MakeArray<double>({5, 2, 3}));

// Создайте дополнительную группу серий, также линейного типа.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesGroup> newSeriesGroup = chart->get_SeriesGroups()->Add(Aspose::Words::Drawing::Charts::ChartSeriesType::Line);
// Укажите использование вторичных осей для новой группы серий.
newSeriesGroup->set_AxisGroup(Aspose::Words::Drawing::Charts::AxisGroup::Secondary);
// Скрыть вторичную ось X.
newSeriesGroup->get_AxisX()->set_Hidden(true);
// Определить заголовок вторичной оси Y.
newSeriesGroup->get_AxisY()->get_Title()->set_Show(true);
newSeriesGroup->get_AxisY()->get_Title()->set_Text(u"Secondary Y axis");

ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartSeriesType::Line, newSeriesGroup->get_SeriesType());

// Добавьте серию в новую группу серий.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series3 = newSeriesGroup->get_Series()->Add(u"Series of secondary series group", categories, System::MakeArray<double>({13, 11, 16}));
series3->get_Format()->get_Stroke()->set_Weight(3.5);

doc->Save(get_ArtifactsDir() + u"Charts.SecondaryAxis.docx");
```

## См. также

* Class [ChartSeriesCollection](../../chartseriescollection/)
* Class [ChartSeriesGroup](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
