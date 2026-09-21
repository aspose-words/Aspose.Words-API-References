---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Drawing::LayoutFlow enum. Bestämmer flödet för textlayout i en textruta i C++."
type: docs
weight: 30000
url: /sv/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Bestämmer flödet av textlayouten i en textruta.

```cpp
enum class LayoutFlow
```

### Värden

| Namn | Värde | Beskrivning |
| --- | --- | --- |
| Horisontell | 0 | Text visas horisontellt. |
| TopToBottomIdeographic | 1 | Ideografisk text visas vertikalt. |
| BottomToTop | 2 | Text visas vertikalt. |
| TopToBottom | 3 | Text visas vertikalt. |
| HorizontalIdeographic | 4 | Ideografisk text visas horisontellt. |
| Vertikal | 5 | Text visas vertikalt. |


## Exempel



Visar hur man lägger till text i en textruta och ändrar dess orientering
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto textbox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textbox->set_Width(100);
textbox->set_Height(100);
textbox->get_TextBox()->set_LayoutFlow(Aspose::Words::Drawing::LayoutFlow::BottomToTop);

textbox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
builder->InsertNode(textbox);

builder->MoveTo(textbox->get_FirstParagraph());
builder->Write(u"This text is flipped 90 degrees to the left.");

doc->Save(get_ArtifactsDir() + u"Drawing.TextBox.docx");
```

## Se även

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
