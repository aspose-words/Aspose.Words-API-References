---
title: "Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder‑Methode"
linktitle: "get_HasOutlineBorder"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder‑Methode. Gibt ein Flag zurück oder setzt es, das angibt, ob ein Umrandungsrahmen, d. h. ein Rahmen um Serien‑ und Kategorienamen, angezeigt wird. Der Standardwert ist true in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/chartdatatable/get_hasoutlineborder/
---
## ChartDataTable::get_HasOutlineBorder method


Liest oder legt ein Flag fest, das angibt, ob ein Umrissrahmen, d. h. ein Rahmen um Serien‑ und Kategorienamen, angezeigt wird. Der Standardwert ist **true**.

```cpp
bool Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder() const
```


## Beispiele



Zeigt, wie man eine Datentabelle mit Diagrammseriendaten anzeigt.
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

## Siehe auch

* Class [ChartDataTable](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
