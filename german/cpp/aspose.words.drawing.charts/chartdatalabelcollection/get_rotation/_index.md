---
title: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation Methode"
linktitle: "get_Rotation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation Methode. Gibt die Drehung der Datenbeschriftungen der gesamten Serie in Grad zurück oder legt sie fest in C++."
type: docs
weight: 5667
url: /de/cpp/aspose.words.drawing.charts/chartdatalabelcollection/get_rotation/
---
## ChartDataLabelCollection::get_Rotation method


Liest oder legt die Drehung der Datenbeschriftungen der gesamten Serie in Grad fest.

```cpp
int32_t Aspose::Words::Drawing::Charts::ChartDataLabelCollection::get_Rotation()
```

## Hinweise


Der zulässige Wertebereich liegt zwischen -180 und 180 inklusive. Der Standardwert ist 0.

Wenn der Wert [Orientation](../get_orientation/) [Horizontal](../../../aspose.words.drawing/shapetextorientation/) ist, werden Beschriftungsformen, falls vorhanden, zusammen mit dem Beschriftungstext rotiert. Andernfalls wird nur der Beschriftungstext rotiert.

## Beispiele



Zeigt, wie die Ausrichtung und Drehung für Datenbeschriftungen geändert werden können.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertChart(Aspose::Words::Drawing::Charts::ChartType::Column, 432, 252);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartSeries> series = shape->get_Chart()->get_Series()->idx_get(0);
System::SharedPtr<Aspose::Words::Drawing::Charts::ChartDataLabelCollection> dataLabels = series->get_DataLabels();

// Datenbeschriftungen anzeigen.
series->set_HasDataLabels(true);
dataLabels->set_ShowValue(true);
dataLabels->set_ShowCategoryName(true);

// Datenbeschriftungsform definieren.
dataLabels->get_Format()->set_ShapeType(Aspose::Words::Drawing::Charts::ChartShapeType::UpArrow);
dataLabels->get_Format()->get_Stroke()->get_Fill()->Solid(System::Drawing::Color::get_DarkBlue());

// Setzt die Ausrichtung und Drehung der Datenbeschriftungen für die gesamte Serie.
dataLabels->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::VerticalFarEast);
dataLabels->set_Rotation(-45);

// Ändert die Ausrichtung und Drehung der ersten Datenbeschriftung.
dataLabels->idx_get(0)->set_Orientation(Aspose::Words::Drawing::ShapeTextOrientation::Horizontal);
dataLabels->idx_get(0)->set_Rotation(45);

doc->Save(get_ArtifactsDir() + u"Charts.LabelOrientationRotation.docx");
```

## Siehe auch

* Class [ChartDataLabelCollection](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
