---
title: "Aspose::Words::Drawing::Charts::ChartStyle Enum"
linktitle: "ChartStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartStyle Enum. Gibt vordefinierte Stile eines Diagramms in C++ an."
type: docs
weight: 27875
url: /de/cpp/aspose.words.drawing.charts/chartstyle/
---
## ChartStyle enum


Gibt vordefinierte Stile eines Diagramms an.

```cpp
enum class ChartStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Normal | 0 | Stellt den Standard-Diagrammstil dar. |
| Gedämpft | 1 | Ein Stil mit gedämpften Farben. |
| Gesättigt | 2 | Ein Stil mit stärker gesättigten Farben. |
| Schattiert | 3 | Ein Stil mit schattierten Datenpunkten. |
| Flat | 4 | Ein Stil mit flachen Datenpunkten ohne Verlauf. |
| Beschattet | 5 | Ein Stil mit Datenpunkten, die einen Schatten haben. |
| Gradient | 6 | Ein Stil mit Farbverlauffüllung der Datenpunkte. |
| Original | 7 | Ein Stil mit dem ursprünglichen Aussehen eines Diagramms. |
| Transparent1 | 8 | Ein Stil mit transparenten Datenpunkten. |
| Transparent2 | 9 | Ein Stil mit transparenten Datenpunkten. |
| Umriss | 10 | Ein Stil mit Datenpunkten ohne Füllung, sondern nur einer Kontur. |
| OutlineBlack | 11 | Ein Stil mit schwarzem Diagrammhintergrund, bei dem Datenpunkte keine Füllung haben, sondern nur eine Kontur. |
| Schwarz | 12 | Ein Stil mit schwarzem Diagrammhintergrund. |
| Grau | 13 | Ein Stil mit grauem Farbverlauf-Diagrammhintergrund. |
| Blau | 14 | Ein Stil mit blauem Diagrammhintergrund. |
| ShadedPlot | 15 | Ein Stil, bei dem der Plot‑Bereich schattiert ist. |


## Beispiele



Zeigt, wie man den Diagrammstil festlegt und abruft.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Diagramm im Black-Stil ein.
builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 250, Aspose::Words::Drawing::Charts::ChartStyle::Black);

doc->Save(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Charts.SetChartStyle.docx");

// Holen Sie ein Diagramm zum Aktualisieren.
auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = shape->get_Chart();

// Holen Sie den Diagrammstil.
ASSERT_EQ(Aspose::Words::Drawing::Charts::ChartStyle::Black, chart->get_Style());
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
