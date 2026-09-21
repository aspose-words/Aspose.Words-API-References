---
title: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation metod"
linktitle: "get_Orientation"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation metod. Hämtar eller anger orienteringen för tick‑etiketttexten i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.drawing.charts/axisticklabels/get_orientation/
---
## AxisTickLabels::get_Orientation method


Hämtar eller anger orienteringen för tick-etiketttexten.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::AxisTickLabels::get_Orientation()
```

## Anmärkningar


Standardvärdet är [Horizontal](../../../aspose.words.drawing/shapetextorientation/).

Observera att vissa [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)-värden inte påverkar orienteringen av tick‑etiketttexten i värdeaxlar.

## Exempel



Visar hur man ändrar orientering och rotation för axelns tick‑etiketter.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga ett stapeldiagram.
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> xTickLabels = shape->get_Chart()->get_AxisX()->get_TickLabels();
System::SharedPtr<Aspose::Words::Drawing::Charts::AxisTickLabels> yTickLabels = shape->get_Chart()->get_AxisY()->get_TickLabels();

// Ställ in orientering och rotation för axelns tick‑etiketter.
xTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
xTickLabels->set_Rotation(-30);
yTickLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
yTickLabels->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.TickLabelsOrientationRotation.docx");
```

## Se även

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [AxisTickLabels](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
