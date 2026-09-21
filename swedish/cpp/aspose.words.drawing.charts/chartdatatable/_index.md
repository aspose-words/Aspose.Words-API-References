---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::ChartDataTable class. Tillåter att ange egenskaper för en diagramdatatabell i C++."
type: docs
weight: 9500
url: /sv/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Tillåter att ange egenskaper för en diagramdatatabell.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Metoder

| Metod | Beskrivning |
| --- | --- |
| [get_Font](./get_font/)() | Tillhandahåller åtkomst till teckensnittsformatering för datatabellen. |
| [get_Format](./get_format/)() | Tillhandahåller åtkomst till fyllning av textbakgrund och kantformatering för datatabellen. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Hämtar eller anger en flagga som visar om en horisontell kant i datatabellen visas. Standardvärdet är **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Hämtar eller anger en flagga som visar om förklaringsnycklar visas i datatabellen. Standardvärdet är **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Hämtar eller anger en flagga som visar om en konturkant, det vill säga en kant runt serier och kategorinamnen, visas. Standardvärdet är **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Hämtar eller anger en flagga som visar om en vertikal kant i datatabellen visas. Standardvärdet är **true**. |
| [get_Show](./get_show/)() const | Hämtar eller anger en flagga som visar om datatabellen ska visas för diagrammet. Standardvärdet är **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | Sättare för [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

## Exempel



Visar hur man visar en datatabell med diagramseriedata.
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

## Se även

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
