---
title: "Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation Methode"
linktitle: "get_Orientation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation Methode. Liest oder setzt die Ausrichtung des Diagrammtiteltextes in C++."
type: docs
weight: 1875
url: /de/cpp/aspose.words.drawing.charts/charttitle/get_orientation/
---
## ChartTitle::get_Orientation method


Liest oder setzt die Ausrichtung des Diagrammtiteltextes.

```cpp
Aspose::Words::Drawing::ShapeTextOrientation Aspose::Words::Drawing::Charts::ChartTitle::get_Orientation()
```


## Beispiele



Zeigt, wie die Ausrichtung und Drehung von Diagramm- und Achsentiteln festgelegt werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Drawing::Shape> chartShape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 400, 300);
System::SharedPtr<Aspose::Words::Drawing::Charts::Chart> chart = chartShape->get_Chart();

chart->get_Title()->set_Text(u"Sample Chart");
chart->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_Title()->set_Rotation(90);

// Stellen Sie vor dem Festlegen von Titel-Eigenschaften sicher, dass dieser Titel angezeigt wird.
chart->get_AxisX()->get_Title()->set_Show(true);
chart->get_AxisX()->get_Title()->set_Text(u"X Axis");
chart->get_AxisX()->get_Title()->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
chart->get_AxisX()->get_Title()->set_Rotation(-90);

doc->Save(get_ArtifactsDir() + u"Charts.TitleOrientation.docx");
```

## Siehe auch

* Enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* Class [ChartTitle](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
