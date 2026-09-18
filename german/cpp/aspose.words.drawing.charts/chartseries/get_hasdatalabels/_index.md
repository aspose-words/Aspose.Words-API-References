---
title: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels-Methode"
linktitle: "get_HasDataLabels"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels-Methode. Gibt ein Flag zurück oder setzt es, das angibt, ob Datenbeschriftungen für die Serie in C++ angezeigt werden."
type: docs
weight: 7000
url: /de/cpp/aspose.words.drawing.charts/chartseries/get_hasdatalabels/
---
## ChartSeries::get_HasDataLabels method


Ermittelt oder legt ein Flag fest, das angibt, ob Datenbeschriftungen für die Serie angezeigt werden.

```cpp
bool Aspose::Words::Drawing::Charts::ChartSeries::get_HasDataLabels() const
```


## Beispiele



Zeigt, wie man Datenbeschriftungen für eine Diagrammserie aktiviert und konfiguriert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Liniendiagramm hinzu, löschen Sie dann seine Demo-Datenserie, um mit einem leeren Diagramm zu beginnen,
// und setzen Sie anschließend einen Titel.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Line, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();
chart->get_Series()->Clear();
chart->get_Title()->set_Text(u"Monthly sales report");

// Fügen Sie eine benutzerdefinierte Diagrammserie mit Monaten als Kategorien für die X‑Achse ein,
// und die entsprechenden Dezimalbeträge für die Y‑Achse.
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = chart->get_Series()->Add(u"Revenue", System::MakeArray<System::String>({u"January", u"February", u"March"}), System::MakeArray<double>({25.611, 21.439, 33.750}));

// Aktivieren Sie Datenbeschriftungen und wenden Sie anschließend ein benutzerdefiniertes Zahlenformat für die in den Datenbeschriftungen angezeigten Werte an.
// Dieses Format behandelt die angezeigten Dezimalwerte als Millionen US‑Dollar.
series->set_HasDataLabels(true);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();
dataLabels->set_ShowValue(true);
dataLabels->get_NumberFormat()->set_FormatCode(u"\"US$\" #,##0.000\"M\"");
dataLabels->get_Font()->set_Size(12);

doc->Save(get_ArtifactsDir() + u"Charts.DataLabelNumberFormat.docx");
```

## Siehe auch

* Class [ChartSeries](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
