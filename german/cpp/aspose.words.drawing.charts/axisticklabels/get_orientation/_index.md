---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation-Methode"
linktitle: "get_Orientation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation-Methode. Ruft die Orientierung des Textes der Achsenbeschriftungen ab oder legt sie fest in C++."
type: docs
weight: 6000
url: /de/cpp/aspose.words.drawing.charts/axisticklabels/get_orientation/
---
## AxisTickLabels::get_Orientation method


Ermittelt oder setzt die Ausrichtung des Tick‑Label‑Texts.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation()
```

## Hinweise


Der Standardwert ist [Horizontal](../../../aspose.words.drawing/shapetextorientation/).

Beachten Sie, dass einige [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/) Werte die Ausrichtung des Tick-Label-Textes in den Werteachsen nicht beeinflussen.

## Beispiele



Zeigt, wie die Orientierung und Drehung von Achsenbeschriftungen geändert werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein Säulendiagramm ein.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Setzen Sie die Orientierung und Drehung der Achsenbeschriftungen.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## Siehe auch

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
