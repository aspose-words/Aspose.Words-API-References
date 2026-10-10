---
title: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor‑metod"
linktitle: "get_VerticalAnchor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBox::get_VerticalAnchor‑metod. Anger den vertikala justeringen av texten inom en form i C++."
type: docs
weight: 14000
url: /sv/cpp/aspose.words.drawing/textbox/get_verticalanchor/
---
## TextBox::get_VerticalAnchor method


Anger den vertikala justeringen av texten inom en form.

```cpp
Aspose::Words::Drawing::TextBoxAnchor Aspose::Words::Drawing::TextBox::get_VerticalAnchor()
```

## Anmärkningar


Standardvärdet är [Top](../../textboxanchor/).

## Exempel



Visar hur man vertikalt justerar textinnehållet i en textruta.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> shape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 200, 200);

// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Top" för att
// justera texten i den här textrutan med den övre sidan av formen.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Middle" för att
// justera texten i den här textrutan till mitten av formen.
// Ställ in egenskapen "VerticalAnchor" till "TextBoxAnchor.Bottom" för att
// justera texten i den här textrutan till botten av formen.
shape->get_TextBox()->set_VerticalAnchor(verticalAnchor);

builder->MoveTo(shape->get_FirstParagraph());
builder->Write(u"Hello world!");

// Den vertikala justeringen av text i textrutor är tillgänglig från Microsoft Word 2007 och framåt.
doc->get_CompatibilityOptions()->OptimizeFor(Aspose::Words::Settings::MsWordVersion::Word2007);
doc->Save(get_ArtifactsDir() + u"Shape.VerticalAnchor.docx");
```

## Se även

* Enum [TextBoxAnchor](../../textboxanchor/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
