---
title: "Aspose::Words::Drawing::Charts::ChartNumberFormat Klasse"
linktitle: "ChartNumberFormat"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartNumberFormat Klasse. Stellt die Zahlenformatierung des übergeordneten Elements dar. Weitere Informationen finden Sie im Dokumentationsartikel in C++."
type: docs
weight: 15000
url: /de/cpp/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class


Stellt die Zahlenformatierung des übergeordneten Elements dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/) .

```cpp
class ChartNumberFormat : public System::Object
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [get_FormatCode](./get_formatcode/)() | Liest oder setzt den Formatcode, der auf ein Datenbeschriftung angewendet wird. |
| [get_IsLinkedToSource](./get_islinkedtosource/)() | Gibt an, ob der Formatcode mit einer Quellzelle verknüpft ist. Standard ist true. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_FormatCode](./set_formatcode/)(const System::String\&) | Setter für [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_FormatCode](./get_formatcode/). |
| [set_IsLinkedToSource](./set_islinkedtosource/)(bool) | Setter für [Aspose::Words::Drawing::Charts::ChartNumberFormat::get_IsLinkedToSource](./get_islinkedtosource/). |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
