---
title: "Метод Aspose::Words::Drawing::Charts::Chart::get_DataTable"
linktitle: "get_DataTable"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::Chart::get_DataTable. Предоставляет доступ к свойствам таблицы данных этой диаграммы. Таблица данных может быть отображена с помощью свойства Show в C++."
type: docs
weight: 4500
url: /ru/cpp/aspose.words.drawing.charts/chart/get_datatable/
---
## Chart::get_DataTable method


Предоставляет доступ к свойствам таблицы данных этой диаграммы. Таблица данных может быть отображена с помощью свойства [Show](../../chartdatatable/get_show/).

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> Aspose::Words::Drawing::Charts::Chart::get_DataTable()
```


## Примеры



Показывает, как отобразить таблицу данных с данными рядов диаграммы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeriesCollection> series = chart->get_Series();
series->Clear();
auto xValues = System::MakeArray<double>({2020, 2021, 2022, 2023});
series->Add(u"Series1", xValues, System::MakeArray<double>({5, 11, 2, 7}));
series->Add(u"Series2", xValues, System::MakeArray<double>({6, 5.5, 7, 7.8}));
series->Add(u"Series3", xValues, System::MakeArray<double>({10, 8, 7, 9}));

System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataTable> dataTable = chart->get_DataTable();
dataTable->set_Show(true);

dataTable->set_HasLegendKeys(false);
dataTable->set_HasHorizontalBorder(false);
dataTable->set_HasVerticalBorder(false);
dataTable->set_HasOutlineBorder(false);

dataTable->get_Font()->set_Italic(true);
dataTable->get_Format()->get_Stroke()->set_Weight(1);
dataTable->get_Format()->get_Stroke()->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDot);
dataTable->get_Format()->get_Stroke()->set_Color(System::Drawing::Color::get_DarkBlue());

doc->Save(get_ArtifactsDir() + u"Charts.DataTable.docx");
```

## См. также

* Class [ChartDataTable](../../chartdatatable/)
* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
