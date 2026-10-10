---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Drawing::LayoutFlow enum. Bestimmt den Fluss des Textlayouts in einem Textfeld in C++."
type: docs
weight: 30000
url: /de/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Bestimmt den Fluss des Textlayouts in einem Textfeld.

```cpp
enum class LayoutFlow
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Horizontal | 0 | Text wird horizontal angezeigt. |
| TopToBottomIdeographic | 1 | Ideografischer Text wird vertikal angezeigt. |
| BottomToTop | 2 | Text wird vertikal angezeigt. |
| TopToBottom | 3 | Text wird vertikal angezeigt. |
| HorizontalIdeographic | 4 | Ideografischer Text wird horizontal angezeigt. |
| Vertikal | 5 | Text wird vertikal angezeigt. |


## Beispiele



Zeigt, wie man Text zu einem Textfeld hinzufügt und dessen Ausrichtung ändert.
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

## Siehe auch

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
