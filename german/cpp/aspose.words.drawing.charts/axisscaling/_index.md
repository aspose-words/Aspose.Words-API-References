---
title: "Aspose::Words::Drawing::Charts::AxisScaling Klasse"
linktitle: "AxisScaling"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::AxisScaling Klasse. Stellt die Skalierungsoptionen der Achse dar. Weitere Informationen finden Sie im Dokumentationsartikel für C++."
type: docs
weight: 3000
url: /de/cpp/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class


Stellt die Skalierungsoptionen der Achse dar. Weitere Informationen finden Sie im Dokumentationsartikel [Working with Charts](https://docs.aspose.com/words/cpp/working-with-charts/).

```cpp
class AxisScaling : public Aspose::Words::Drawing::Core::Dml::IDmlExtensionListSource
```

## Methoden

| Methode | Beschreibung |
| --- | --- |
| [AxisScaling](./axisscaling/)() |  |
| [get_LogBase](./get_logbase/)() const | Liest oder setzt die logarithmische Basis für eine logarithmische Achse. |
| [get_Maximum](./get_maximum/)() | Liest oder setzt den Maximalwert der Achse. |
| [get_Minimum](./get_minimum/)() | Liest oder setzt den Minimalwert der Achse. |
| [get_Type](./get_type/)() const | Liest oder setzt den Skalierungstyp der Achse. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_LogBase](./set_logbase/)(double) | Setter für [Aspose::Words::Drawing::Charts::AxisScaling::get_LogBase](./get_logbase/). |
| [set_Maximum](./set_maximum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Setter für [Aspose::Words::Drawing::Charts::AxisScaling::get_Maximum](./get_maximum/). |
| [set_Minimum](./set_minimum/)(const System::SharedPtr\<Aspose::Words::Drawing::Charts::AxisBound\>\&) | Setter für [Aspose::Words::Drawing::Charts::AxisScaling::get_Minimum](./get_minimum/). |
| [set_Type](./set_type/)(Aspose::Words::Drawing::Charts::AxisScaleType) | Setter für [Aspose::Words::Drawing::Charts::AxisScaling::get_Type](./get_type/). |
| static [Type](./type/)() |  |

## Beispiele



Zeigt, wie man logarithmische Skalierung auf eine Diagrammachse anwendet.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Scatter, 450, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

// Löschen Sie die Demo-Datenreihe des Diagramms, um mit einem leeren Diagramm zu beginnen.
chart->get_Series()->Clear();

// Fügen Sie eine Reihe mit X/Y-Koordinaten für fünf Punkte ein.
chart->get_Series()->Add(u"Series 1", System::MakeArray<double>({1.0, 2.0, 3.0, 4.0, 5.0}), System::MakeArray<double>({1.0, 20.0, 400.0, 8000.0, 160000.0}));

// Die Skalierung der X-Achse ist standardmäßig linear,
// zeigt gleichmäßig ansteigende Werte, die unseren X-Wertbereich (0, 1, 2, 3...) abdecken.
// Eine lineare Achse ist für unsere Y-Werte nicht ideal
// da die Punkte mit kleineren Y-Werten schwerer zu lesen sind.
// Eine logarithmische Skalierung mit der Basis 20 (1, 20, 400, 8000...)
// verteilt die geplotteten Punkte, sodass wir ihre Werte im Diagramm leichter ablesen können.
chart->get_AxisY()->get_Scaling()->set_Type(Aspose::Words::Drawing::Charts::AxisScaleType::Logarithmic);
chart->get_AxisY()->get_Scaling()->set_LogBase(20);

doc->Save(get_ArtifactsDir() + u"Charts.AxisScaling.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing::Charts](../)
* Library [Aspose.Words for C++](../../)
