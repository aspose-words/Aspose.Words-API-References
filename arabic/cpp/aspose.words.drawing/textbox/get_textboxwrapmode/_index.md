---
title: "طريقة Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode"
linktitle: "get_TextBoxWrapMode"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode. يحدد كيفية التفاف النص داخل الشكل في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words.drawing/textbox/get_textboxwrapmode/
---
## TextBox::get_TextBoxWrapMode method


يحدد كيفية التفاف النص داخل الشكل.

```cpp
Aspose::Words::Drawing::TextBoxWrapMode Aspose::Words::Drawing::TextBox::get_TextBoxWrapMode()
```

## ملاحظات


القيمة الافتراضية هي [Square](../../textboxwrapmode/).

## أمثلة



يعرض كيفية تعيين وضع الالتفاف لمحتويات مربع النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 300, 300);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// قم بتعيين الخاصية "TextBoxWrapMode" إلى "TextBoxWrapMode.None" لزيادة عرض مربع النص
// لتستوعب النص، يجب أن يكون كبيرًا بما فيه الكفاية.
// قم بتعيين الخاصية "TextBoxWrapMode" إلى "TextBoxWrapMode.Square" لـ
// لف كل النص داخل مربع النص مع الحفاظ على أبعاده.
textBox->set_TextBoxWrapMode(textBoxWrapMode);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->get_Font()->set_Size(32);
builder->Write(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxContentsWrapMode.docx");
```

## انظر أيضًا

* Enum [TextBoxWrapMode](../../textboxwrapmode/)
* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
