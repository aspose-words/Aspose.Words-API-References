---
title: "Aspose::Words::Drawing::Charts::ChartDataTable class"
linktitle: "ChartDataTable"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataTable class. Ermöglicht die Angabe von Eigenschaften einer Diagrammdatentabelle in C++."
type: docs
weight: 9500
url: /de/cpp/aspose.words.drawing.charts/chartdatatable/
---
## ChartDataTable class


Ermöglicht die Angabe von Eigenschaften einer Diagrammdatentabelle.

```cpp
class ChartDataTable : public Aspose::Words::Drawing::Charts::Core::IChartItemTextProperties,
                       public Aspose::Words::Drawing::Charts::Core::IChartFormatSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_Font](./get_font/)() | Stellt Zugriff auf die Schriftformatierung der Datentabelle bereit. |
| [get_Format](./get_format/)() | Stellt Zugriff auf die Füllung des Texthintergrunds und die Rahmenformatierung der Datentabelle bereit. |
| [get_HasHorizontalBorder](./get_hashorizontalborder/)() const | Liest oder legt ein Flag fest, das angibt, ob ein horizontaler Rahmen der Datentabelle angezeigt wird. Der Standardwert ist **true**. |
| [get_HasLegendKeys](./get_haslegendkeys/)() const | Liest oder legt ein Flag fest, das angibt, ob Legenden‑Schlüssel in der Datentabelle angezeigt werden. Der Standardwert ist **true**. |
| [get_HasOutlineBorder](./get_hasoutlineborder/)() const | Liest oder legt ein Flag fest, das angibt, ob ein Umrissrahmen, d. h. ein Rahmen um Serien‑ und Kategorienamen, angezeigt wird. Der Standardwert ist **true**. |
| [get_HasVerticalBorder](./get_hasverticalborder/)() const | Liest oder legt ein Flag fest, das angibt, ob ein vertikaler Rahmen der Datentabelle angezeigt wird. Der Standardwert ist **true**. |
| [get_Show](./get_show/)() const | Liest oder legt ein Flag fest, das angibt, ob die Datentabelle für das Diagramm angezeigt wird. Der Standardwert ist **false**. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_HasHorizontalBorder](./set_hashorizontalborder/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasHorizontalBorder](./get_hashorizontalborder/). |
| [set_HasLegendKeys](./set_haslegendkeys/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasLegendKeys](./get_haslegendkeys/). |
| [set_HasOutlineBorder](./set_hasoutlineborder/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasOutlineBorder](./get_hasoutlineborder/). |
| [set_HasVerticalBorder](./set_hasverticalborder/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataTable::get_HasVerticalBorder](./get_hasverticalborder/). |
| [set_Show](./set_show/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartDataTable::get_Show](./get_show/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
