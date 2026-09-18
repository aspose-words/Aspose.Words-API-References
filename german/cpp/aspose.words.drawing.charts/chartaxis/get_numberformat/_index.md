---
title: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat Methode"
linktitle: "get_NumberFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat Methode. Gibt ein ChartNumberFormat‑Objekt zurück, das die Definition von Zahlenformaten für die Achse in C++ ermöglicht."
type: docs
weight: 20000
url: /de/cpp/aspose.words.drawing.charts/chartaxis/get_numberformat/
---
## ChartAxis::get_NumberFormat method


Gibt ein [ChartNumberFormat](../../chartnumberformat/) Objekt zurück, das die Definition von Zahlenformaten für die Achse ermöglicht.

```cpp
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartNumberFormat> Aspose::Words::Drawing::Charts::ChartAxis::get_NumberFormat()
```


## Beispiele



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

* Class [ChartNumberFormat](../../chartnumberformat/)
* Class [ChartAxis](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
