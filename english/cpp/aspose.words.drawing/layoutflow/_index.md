---
title: Aspose::Words::Drawing::LayoutFlow enum
linktitle: LayoutFlow
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Drawing::LayoutFlow enum. Determines the flow of the text layout in a textbox in C++.'
type: docs
weight: 30000
url: /cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Determines the flow of the text layout in a textbox.

```cpp
enum class LayoutFlow : int
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| BottomToTop | 2 | Text is displayed vertically. |
| Horizontal | 0 | Text is displayed horizontally. |
| HorizontalIdeographic | 4 | Ideographic text is displayed horizontally. |
| TopToBottom | 3 | Text is displayed vertically. |
| TopToBottomIdeographic | 1 | Ideographic text is displayed vertically. |
| Vertical | 5 | Text is displayed vertically. |

## Examples


Shows how to add text to a text box, and change its orientation

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

auto textbox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, ShapeType::TextBox);
textbox->set_Width(100);
textbox->set_Height(100);
textbox->get_TextBox()->set_LayoutFlow(LayoutFlow::BottomToTop);

textbox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
builder->InsertNode(textbox);

builder->MoveTo(textbox->get_FirstParagraph());
builder->Write(u"This text is flipped 90 degrees to the left.");

doc->Save(get_ArtifactsDir() + u"Drawing.TextBox.docx");
```
## See Also

* [LayoutFlow](../textbox/get_layoutflow/)

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
