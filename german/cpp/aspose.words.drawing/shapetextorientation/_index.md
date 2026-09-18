---
title: "Aspose::Words::Drawing::ShapeTextOrientation enum"
linktitle: "ShapeTextOrientation"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeTextOrientation enum. Gibt die Ausrichtung von Text in Formen in C++ an."
type: docs
weight: 37500
url: /de/cpp/aspose.words.drawing/shapetextorientation/
---
## ShapeTextOrientation enum


Gibt die Ausrichtung des Textes in Formen an.

```cpp
enum class ShapeTextOrientation
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | 0 | Text wird horizontal angeordnet (lr-tb). |
| Abwärts | 1 | Text wird um 90 Grad nach rechts gedreht, sodass er von oben nach unten erscheint (tb-rl). |
| Aufwärts | 2 | Der Text ist um 90 Grad nach links gedreht, um von unten nach oben zu erscheinen (bt-lr). |
| VerticalFarEast | 3 | Zeichen aus Fernost erscheinen vertikal, anderer Text ist um 90 Grad nach rechts gedreht, um von oben nach unten zu erscheinen (tb-rl-v). |
| VerticalRotatedFarEast | 4 | Zeichen aus Fernost erscheinen vertikal, anderer Text ist um 90 Grad nach rechts gedreht, um vertikal von oben nach unten zu erscheinen, dann horizontal von links nach rechts (tb-lr-v). |
| WordArtVertical | 5 | Der Text ist vertikal, wobei ein Buchstabe über dem anderen steht. |
| WordArtVerticalRightToLeft | 6 | Der Text ist vertikal, wobei ein Buchstabe über dem anderen steht, dann von rechts nach links horizontal. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
