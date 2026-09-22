---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Drawing::LayoutFlow enum. Bir metin kutusundaki metin düzeninin akışını C++'da belirler."
type: docs
weight: 30000
url: /tr/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


Bir metin kutusundaki metin düzeninin akışını belirler.

```cpp
enum class LayoutFlow
```

### Değerler

| Ad | Değer | Açıklama |
| --- | --- | --- |
| Yatay | 0 | Metin yatay olarak görüntülenir. |
| TopToBottomIdeographic | 1 | İdeografik metin dikey olarak görüntülenir. |
| BottomToTop | 2 | Metin dikey olarak görüntülenir. |
| TopToBottom | 3 | Metin dikey olarak görüntülenir. |
| HorizontalIdeographic | 4 | İdeografik metin yatay olarak görüntülenir. |
| Dikey | 5 | Metin dikey olarak görüntülenir. |


## Örnekler



Bir metin kutusuna metin eklemeyi ve yönünü değiştirmeyi gösterir
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

## Ayrıca Bakınız

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
