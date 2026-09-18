---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor Methode"
linktitle: "get_VerticalAnchor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor Methode. Gibt die vertikale Ausrichtung des Textes innerhalb einer Form in C++ an."
type: docs
weight: 14000
url: /de/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Gibt die vertikale Ausrichtung des Textes innerhalb einer Form an.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Hinweise


Der Standardwert ist [Top](../../textboxanchor/).

## Beispiele



Zeigt, wie der Textinhalt einer Textbox vertikal ausgerichtet wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Top", um
// den Text in dieser Textbox mit der oberen Seite der Form auszurichten.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Middle", um
// den Text in dieser Textbox in der Mitte der Form auszurichten.
// Setzen Sie die Eigenschaft "VerticalAnchor" auf "TextBoxAnchor.Bottom", um
// den Text in dieser Textbox an der Unterseite der Form auszurichten.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Die vertikale Ausrichtung von Text in Textboxen ist ab Microsoft Word 2007 verfügbar.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Siehe auch

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
