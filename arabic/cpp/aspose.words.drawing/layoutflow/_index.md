---
title: "Aspose::Words::Drawing::LayoutFlow enum"
linktitle: "LayoutFlow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::LayoutFlow enum. يحدد تدفق تخطيط النص في مربع النص في C++."
type: docs
weight: 30000
url: /ar/cpp/aspose.words.drawing/layoutflow/
---
## LayoutFlow enum


يحدد تدفق تخطيط النص داخل مربع النص.

```cpp
enum class LayoutFlow
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| أفقي | 0 | يتم عرض النص أفقيًا. |
| TopToBottomIdeographic | 1 | يتم عرض النص الإيديغرافي عموديًا. |
| BottomToTop | 2 | يتم عرض النص عموديًا. |
| TopToBottom | 3 | يتم عرض النص عموديًا. |
| HorizontalIdeographic | 4 | يتم عرض النص الإيديغرافي أفقيًا. |
| عمودي | 5 | يتم عرض النص عموديًا. |


## أمثلة



يوضح كيفية إضافة نص إلى مربع نص وتغيير اتجاهه
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

## انظر أيضًا

* Namespace [Aspose::Words::Drawing](../)
* Library [Aspose.Words for C++](../../)
