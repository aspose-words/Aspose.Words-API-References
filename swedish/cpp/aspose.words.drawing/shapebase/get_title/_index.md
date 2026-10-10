---
title: "Aspose::Words::Drawing::ShapeBase::get_Title metod"
linktitle: "get_Title"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_Title metod. Hämtar eller anger titeln (rubriken) för det aktuella formobjektet i C++."
type: docs
weight: 51000
url: /sv/cpp/aspose.words.drawing/shapebase/get_title/
---
## ShapeBase::get_Title method


Hämtar eller anger titeln (rubriken) för det aktuella formobjektet.

```cpp
System::String Aspose::Words::Drawing::ShapeBase::get_Title()
```

## Anmärkningar


Standard är en tom sträng.

Kan inte vara **null**, men kan vara en tom sträng.

## Exempel



Visar hur man anger titeln på en form.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Skapa en form, ge den en titel och lägg sedan till den i dokumentet.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Cube);
shape->set_Width(200);
shape->set_Height(200);
shape->set_Title(u"My cube");

builder->InsertNode(shape);

// När vi sparar ett dokument med en form som har en titel,
// Aspose.Words kommer att lagra den titeln i formens Alt Text.
doc->Save(get_ArtifactsDir() + u"Shape.Title.docx");

doc = System::MakeObject<Aspose::Words::Document>(get_ArtifactsDir() + u"Shape.Title.docx");
shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

ASSERT_EQ(System::String::Empty, shape->get_Title());
ASSERT_EQ(u"Title: My cube", shape->get_AlternativeText());
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
