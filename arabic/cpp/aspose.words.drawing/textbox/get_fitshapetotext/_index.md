---
title: "طريقة Aspose::Words::Drawing::TextBox::get_FitShapeToText"
linktitle: "get_FitShapeToText"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Drawing::TextBox::get_FitShapeToText. تحدد ما إذا كان Microsoft Word سيزيد حجم الشكل لتناسب النص في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.drawing/textbox/get_fitshapetotext/
---
## TextBox::get_FitShapeToText method


يحدد ما إذا كان Microsoft Word سيزيد حجم الشكل ليتناسب مع النص.

```cpp
bool Aspose::Words::Drawing::TextBox::get_FitShapeToText()
```

## ملاحظات


القيمة الافتراضية هي **false**.

## أمثلة



يوضح كيفية جعل مربع النص يغير حجمه ليتناسب بإحكام مع محتوياته.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Drawing::Shape> textBoxShape = builder->InsertShape(Aspose::Words::Drawing::ShapeType::TextBox, 150, 100);
System::SharedPtr<Aspose::Words::Drawing::TextBox> textBox = textBoxShape->get_TextBox();

// طبق هذه القيم على كلا العضوين لجعل الشكل الأب يتناسب
// إحكامًا حول محتوى النص، متجاهلًا الأبعاد التي حددناها.
textBox->set_FitShapeToText(true);
textBox->set_TextBoxWrapMode(Aspose::Words::Drawing::TextBoxWrapMode::None);

builder->MoveTo(textBoxShape->get_LastParagraph());
builder->Write(u"Text fit tightly inside textbox.");

doc->Save(get_ArtifactsDir() + u"Shape.TextBoxFitShapeToText.docx");
```

## انظر أيضًا

* Class [TextBox](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
