---
title: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative-Methode"
linktitle: "get_IsDecorative"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::ShapeBase::get_IsDecorative-Methode. Ruft das Flag ab oder legt es fest, das angibt, ob die Form im Dokument dekorativ ist, in C++."
type: docs
weight: 25000
url: /de/cpp/aspose.words.drawing/shapebase/get_isdecorative/
---
## ShapeBase::get_IsDecorative method


Liest oder legt das Flag fest, das angibt, ob die Form im Dokument dekorativ ist.

```cpp
bool Aspose::Words::Drawing::ShapeBase::get_IsDecorative()
```


## Beispiele



Zeigt, wie man festlegt, dass die Form dekorativ ist.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Decorative shapes.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->idx_get(0));
ASSERT_TRUE(shape->get_IsDecorative());

// Wenn \"AlternativeText\" nicht leer ist, kann die Form nicht dekorativ sein.
// Deshalb wurde unser Wert auf 'false' geändert.
shape->set_AlternativeText(u"Alternative text.");
ASSERT_FALSE(shape->get_IsDecorative());

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->MoveToDocumentEnd();
// Erstelle eine neue Form als dekorativ.
shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::Rectangle, 100, 100);
shape->set_IsDecorative(true);

doc->Save(get_ArtifactsDir() + u"Shape.IsDecorative.docx");
```

## Siehe auch

* Class [ShapeBase](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
