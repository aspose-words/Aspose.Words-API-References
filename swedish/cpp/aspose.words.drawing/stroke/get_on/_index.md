---
title: "Aspose::Words::Drawing::Stroke::get_On-metod"
linktitle: "get_On"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::Stroke::get_On-metod. Definierar om vägen ska streckas i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.drawing/stroke/get_on/
---
## Stroke::get_On method


Definierar om vägen ska streckas.

```cpp
bool Aspose::Words::Drawing::Stroke::get_On()
```

## Anmärkningar


Standardvärdet för en [Shape](../../shape/) är **true**.

## Exempel



Visar hur man ändrar streckegenskaper.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 100, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 100, 200, 200, Aspose::Words::Drawing::WrapType::None);

// Grundläggande former, såsom rektangeln, har två synliga delar.
// 1 -  Fyllningen, som gäller området inom formens kontur:
shape->get_Fill()->set_ForeColor(System::Drawing::Color::get_White());

// 2 -  Strecket, som markerar formens kontur:
// Ändra olika egenskaper för detta forms streck.
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

## Se även

* Class [Stroke](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
