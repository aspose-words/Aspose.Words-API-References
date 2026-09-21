---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative metod"
linktitle: "get_IsDecorative"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative metod. Hämtar eller anger flaggan som specificerar om formen är dekorativ i dokumentet i C++."
type: docs
weight: 25000
url: /sv/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Hämtar eller anger flaggan som specificerar om formen är dekorativ i dokumentet.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Exempel



Visar hur man anger att formen är dekorativ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// Om "AlternativeText" inte är tomt kan formen inte vara dekorativ.
// Det är därför vårt värde har ändrats till 'false'.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Skapa en ny form som dekorativ.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## Se även

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
