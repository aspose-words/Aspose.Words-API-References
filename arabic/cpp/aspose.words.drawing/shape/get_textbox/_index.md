---
title: "طريقة Aspose::Words::Drawing::Shape::get_TextBox"
linktitle: "get_TextBox"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Shape::get_TextBox. يحدد الخصائص التي تُحدد كيفية عرض النص في الشكل في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words.drawing/shape/get_textbox/
---
## Shape::get_TextBox method


يحدد السمات التي تحدد كيفية عرض النص في الشكل.

```cpp
System::SharedPtr<Aspose::Words::Drawing::TextBox> Aspose::Words::Drawing::Shape::get_TextBox()
```


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

* Class [TextBox](../../textbox/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
