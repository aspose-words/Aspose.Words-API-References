---
title: "Aspose::Words::Drawing::Charts::AxisScaling::get_Type Methode"
linktitle: "get_Type"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::AxisScaling::get_Type Methode. Liest oder setzt den Skalierungstyp der Achse in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/axisscaling/get_type/
---
## AxisScaling::get_Type method


Liest oder setzt den Skalierungstyp der Achse.

```cpp
Aspose::Words::Drawing::Charts::AxisScaleType Aspose::Words::Drawing::Charts::AxisScaling::get_Type() const
```


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

* Enum [AxisScaleType](../../axisscaletype/)
* Class [AxisScaling](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
