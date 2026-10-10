---
title: "Aspose::Words::Drawing::ShapeLineStyle Enum"
linktitle: "ShapeLineStyle"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeLineStyle enum. Gibt den zusammengesetzten Linienstil eines Shape in C++ an."
type: docs
weight: 36000
url: /de/cpp/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enum


Gibt den zusammengesetzten Linienstil eines [Shape](../shape/) an.

```cpp
enum class ShapeLineStyle
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Single | 0 | Einzelne Linie. |
| Double | 1 | Doppelte Linien gleicher Breite. |
| ThickThin | 2 | Doppelte Linien, eine dick, eine dünn. |
| ThinThick | 3 | Doppelte Linien, eine dünn, eine dick. |
| Triple | 4 | Drei Linien, dünn, dick, dünn. |
| Default | n/a | Standardwert ist [Single](./). |


## Beispiele



Zeigt, wie Strich‑Eigenschaften geändert werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Grundformen, wie das Rechteck, haben zwei sichtbare Teile.
// 1 -  Die Füllung, die auf den Bereich innerhalb der Kontur der Form angewendet wird:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  Der Strich, der die Kontur der Form markiert:
// Verschiedene Eigenschaften dieses Form‑Strichs ändern.
System::SharedPtr<Aspose::Words::Drawing::Stroke> stroke = shape->get_Stroke();
stroke->set_On(true);
stroke->set_Weight(5);
stroke->set_Color(System::Drawing::Color::get_Red());
stroke->set_DashStyle(Aspose::Words::Drawing::DashStyle::ShortDashDotDot);
stroke->set_JoinStyle(Aspose::Words::Drawing::JoinStyle::Miter);
stroke->set_EndCap(Aspose::Words::Drawing::EndCap::Square);
stroke->set_LineStyle(Aspose::Words::Drawing::ShapeLineStyle::Triple);
stroke->get_Fill()->TwoColorGradient(System::Drawing::Color::get_Red(), System::Drawing::Color::get_Blue(), Aspose::Words::Drawing::GradientStyle::Vertical, Aspose::Words::Drawing::GradientVariant::Variant1);

doc->Save(get_ArtifactsDir() + u"Shape.Stroke.docx");
```

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
