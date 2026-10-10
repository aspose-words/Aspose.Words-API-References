---
title: "Aspose::Words::Drawing::TextBoxAnchor enum"
linktitle: "TextBoxAnchor"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::TextBoxAnchor enum. Anger värden som används för vertikal justering av formtext i C++."
type: docs
weight: 39000
url: /sv/cpp/aspose.words.drawing/textboxanchor/
---
## TextBoxAnchor enum


Anger värden som används för vertikal justering av formtext.

```cpp
enum class TextBoxAnchor
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Top | 0 | Texten är justerad till toppen av textrutan. |
| Mitten | 1 | Texten är justerad till mitten av textrutan. |
| Bottom | 2 | Texten är justerad till botten av textrutan. |
| TopCentered | 3 | Texten är justerad till toppen centrerad i textrutan. |
| MiddleCentered | 4 | Texten är justerad till mitten centrerad i textrutan. |
| BottomCentered | 5 | Texten är justerad till botten centrerad i textrutan. |
| TopBaseline | 6 | Texten är justerad till toppens baslinje i textrutan. |
| BottomBaseline | 7 | Texten är justerad till bottnens baslinje i textrutan. |
| TopCenteredBaseline | 8 | Texten är justerad till den toppcentrerade baslinjen i textrutan. |
| BottomCenteredBaseline | 9 | Texten är justerad till den nedersta centrerade baslinjen i textrutan. |


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

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
