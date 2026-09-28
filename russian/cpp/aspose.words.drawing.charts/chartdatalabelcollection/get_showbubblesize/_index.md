---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize метод"
linktitle: "get_ShowBubbleSize"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize метод. Позволяет указать, следует ли отображать размер пузыря в подписях данных всего ряда. Применяется только к пузырьковым диаграммам. Значение по умолчанию — false в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_showbubblesize/
---
## ChartDataLabelCollection::get_ShowBubbleSize method


Позволяет указать, следует ли отображать размер пузыря в подписях данных всей серии. Применяется только к пузырьковым диаграммам. Значение по умолчанию — **false**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_ShowBubbleSize()
```


## Примеры



Показывает, как работать с подписями данных пузырьковой диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Bubble, 500, 300)->get_Chart();

// Очистите демонстрационную серию данных диаграммы, чтобы начать с чистой диаграммы.
chart->get_Series()->Clear();

// Добавьте пользовательскую серию с координатами X/Y и диаметром каждого пузыря.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<double>({2.9, 3.5, 1.1, 4.0, 4.0}), System::MakeArray<double>({1.9, 8.5, 2.1, 6.0, 1.5}), System::MakeArray<double>({9.0, 4.5, 2.5, 8.0, 5.0}));

// Включите подписи данных, а затем измените их внешний вид.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowBubbleSize(true);
dataLabels->set_ShowCategoryName(true);
dataLabels->set_ShowSeriesName(true);
dataLabels->set_Separator(u" & ");

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelsBubbleChart.docx");
```

## См. также

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
