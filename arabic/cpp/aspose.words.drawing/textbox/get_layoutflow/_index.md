---
title: "Aspose::Words::Drawing::TextBox::get_LayoutFlow طريقة"
linktitle: "get_LayoutFlow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Drawing::TextBox::get_LayoutFlow طريقة. يحدد تدفق تخطيط النص داخل الشكل في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words.drawing/textbox/get_layoutflow/
---
## TextBox::get_LayoutFlow method


يحدد تدفق تخطيط النص داخل الشكل.

```cpp
Aspose::Words::Drawing::LayoutFlow Aspose::Words::Drawing::TextBox::get_LayoutFlow()
```

## ملاحظات


القيمة الافتراضية هي [Horizontal](../../layoutflow/).

## أمثلة



يوضح كيفية تعيين اتجاه النص داخل مربع النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// انقل مُنشئ المستند إلى داخل مربع النص وأضف نصًا.
builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Writeln(u"Hello world!");
builder->Write(u"Hello again!");

// قم بتعيين خاصية "LayoutFlow" لتحديد اتجاه محتوى النص في هذا مربع النص.
textBox->set_LayoutFlow(layoutFlow);

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxLayoutFlow.docx");
```

## انظر أيضًا

* Enum [LayoutFlow](../../layoutflow/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
