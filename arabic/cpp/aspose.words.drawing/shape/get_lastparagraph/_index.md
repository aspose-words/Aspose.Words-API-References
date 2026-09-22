---
title: "طريقة Aspose::Words::Drawing::Shape::get_LastParagraph"
linktitle: "get_LastParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::Shape::get_LastParagraph. يحصل على الفقرة الأخيرة في الشكل في C++."
type: docs
weight: 14000
url: /ar/cpp/aspose.words.drawing/shape/get_lastparagraph/
---
## Shape::get_LastParagraph method


يحصل على الفقرة الأخيرة في الشكل.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Drawing::Shape::get_LastParagraph()
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

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
