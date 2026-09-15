---
title: "طريقة Aspose::Words::Drawing::TextBox::get_InternalMarginBottom"
linktitle: "get_InternalMarginBottom"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::TextBox::get_InternalMarginBottom. يحدد الهامش السفلي الداخلي بالنقاط لشكل في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.drawing/textbox/get_internalmarginbottom/
---
## TextBox::get_InternalMarginBottom method


يحدد الهامش الداخلي السفلي بالنقاط للشكل.

```cpp
double Aspose::Words::Drawing::TextBox::get_InternalMarginBottom()
```

## ملاحظات


القيمة الافتراضية هي 1/20 بوصة.

## أمثلة



يوضح كيفية تعيين الهوامش الداخلية لمربع النص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أدرج مربع نص آخر بهوامش محددة.
System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 100, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();
textBox->set_InternalMarginTop(15);
textBox->set_InternalMarginBottom(15);
textBox->set_InternalMarginLeft(15);
textBox->set_InternalMarginRight(15);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text placed according to textbox margins.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxMargins.docx");
```

## انظر أيضًا

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
