---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode Methode"
linktitle: "get_FormatCode"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode Methode. Liest den Formatcode aus oder legt ihn fest, der auf ein Datenbeschriftungselement in C++ angewendet wird."
type: docs
weight: 2000
url: /de/cpp/aspose.words.drawing.charts/chartnumberformat/get_formatcode/
---
## ChartNumberFormat::get_FormatCode method


Liest oder setzt den Formatcode, der auf ein Datenbeschriftung angewendet wird.

```cpp
System::String Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode()
```

## Hinweise


Die Zahlenformatierung wird verwendet, um die Darstellung eines Wertes in einer Datenbeschriftung zu ändern und kann auf sehr kreative Weise eingesetzt werden. Beispiele für Zahlenformate:

Zahl - "#,##0.00"

Währung - "\"\$\\"#,##0.00"

Zeit - "[$-x-systime]h:mm:ss AM/PM"

Datum - "d/mm/yyyy"

Prozent - "0.00%"

Bruch - "# ?/?"

Wissenschaftlich - "0.00E+00"

Text - "@"

Buchhaltung - "_-\"\$\\"* #,##0.00_-;-\"\$\\"* #,##0.00_-;_-\"\$\\"* \"-\\"??_-;_-@_-"

Benutzerdefiniert mit Farbe - "[Red]-#,##0.0"

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


Zeigt, wie die Formatierung für Diagrammwerte festgelegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 500, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie dem Diagramm eine benutzerdefinierte Serie mit Kategorien für die X-Achse hinzu,
// und große entsprechende numerische Werte für die Y-Achse.
chart->get_Series()->Add(u"Aspose Test Series", System::MakeArray<System::String>({u"Word", u"PDF", u"Excel", u"GoogleDocs", u"Note"}), System::MakeArray<double>({1900000, 850000, 2100000, 600000, 1500000}));

// Setzen Sie das Zahlenformat der Y-Achsen‑Tick‑Beschriftungen so, dass Ziffern nicht mit Kommas gruppiert werden.
chart->get_AxisY()->get_NumberFormat()->set_FormatCode(u"#,##0");

// Dieses Flag kann den obigen Wert überschreiben und das Zahlenformat aus der Quellzelle übernehmen.
ASSERT_FALSE(chart->get_AxisY()->get_NumberFormat()->get_IsLinkedToSource());

doc->Save(get_ArtifactsDir() + u"Charts.SetNumberFormatToChartAxis.docx");
```

## Siehe auch

* Class [ChartNumberFormat](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
