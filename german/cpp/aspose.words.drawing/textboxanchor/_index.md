---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. Gibt Werte an, die für die vertikale Ausrichtung von Formtext in C++ verwendet werden."
type: docs
weight: 39000
url: /de/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Gibt die für die vertikale Ausrichtung von Formtext verwendeten Werte an.

```cpp
enum class TextBoxAnchor
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Oben | 0 | Der Text ist am oberen Rand des Textfelds ausgerichtet. |
| Mitte | 1 | Der Text ist in der Mitte des Textfelds ausgerichtet. |
| Unten | 2 | Der Text ist am unteren Rand des Textfelds ausgerichtet. |
| TopCentered | 3 | Der Text ist oben zentriert im Textfeld ausgerichtet. |
| MiddleCentered | 4 | Der Text ist mittig zentriert im Textfeld ausgerichtet. |
| BottomCentered | 5 | Der Text ist unten zentriert im Textfeld ausgerichtet. |
| TopBaseline | 6 | Der Text ist an der oberen Grundlinie des Textfelds ausgerichtet. |
| BottomBaseline | 7 | Der Text ist an der unteren Grundlinie des Textfelds ausgerichtet. |
| TopCenteredBaseline | 8 | Der Text ist an der oben zentrierten Grundlinie des Textfelds ausgerichtet. |
| BottomCenteredBaseline | 9 | Der Text ist an der unten zentrierten Grundlinie des Textfelds ausgerichtet. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
