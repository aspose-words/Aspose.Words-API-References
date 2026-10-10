---
title: "Aspose::Words::Drawing::ShapeBase::get_IsInline metod"
linktitle: "get_IsInline"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_IsInline metod. Ett snabbt sätt att avgöra om denna form är placerad i linje med text i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words.drawing/shapebase/get_isinline/
---
## ShapeBase::get_IsInline method


Ett snabbt sätt att avgöra om denna form är placerad i linje med text.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsInline()
```

## Anmärkningar


Har endast effekt för former på toppnivå.

## Exempel



Visar hur man avgör om en form är i linje eller flytande.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Nedan är två omslagstyper som former kan ha.
// 1 -  I linje:
builder->Write(u"Hello world! ");
System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_FillColor(System::Drawing::Color::get_LightBlue());
builder->Write(u" Hello again.");

// En form i linje sitter i ett stycke bland andra stycke‑element, såsom textsekvenser.
// I Microsoft Word kan vi klicka och dra formen till vilket stycke som helst som om den vore ett tecken.
// Om formen är stor kommer den att påverka vertikal styckeavstånd.
// Vi kan inte flytta den här formen till en plats utan stycke.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::Inline, shape->get_WrapType());
ASSERT_TRUE(shape->get_IsInline());

// 2 -  Flytande:
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, Aspose::Words::Drawing::RelativeHorizontalPosition::LeftMargin, 200, Aspose::Words::Drawing::RelativeVerticalPosition::TopMargin, 200, 100, 100, Aspose::Words::Drawing::WrapType::None);
shape->set_FillColor(System::Drawing::Color::get_Orange());

// En flytande form tillhör det stycke som vi infogar den i,
// vilket vi kan avgöra genom en ankarsymbol som visas när vi klickar på formen.
// Om formen inte har en synlig ankarsymbol till vänster,
// behöver vi aktivera synliga ankare via "Options" -> "Display" -> "Object Anchors".
// I Microsoft Word kan vi vänsterklicka och dra den här formen fritt till vilken plats som helst.
ASSERT_EQ(Aspose::Words::Drawing::WrapType::None, shape->get_WrapType());
ASSERT_FALSE(shape->get_IsInline());

doc->Save(get_ArtifactsDir() + u"Shape.IsInline.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
