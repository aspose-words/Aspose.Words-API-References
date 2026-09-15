---
title: "منشئ Aspose::Words::Drawing::Shape::Shape"
linktitle: "Shape"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "منشئ Aspose::Words::Drawing::Shape::Shape. ينشئ كائن شكل جديد في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words.drawing/shape/shape/
---
## Shape::Shape constructor


ينشئ كائن شكل جديد.

```cpp
Aspose::Words::Drawing::Shape::Shape(const System::SharedPtr<Aspose::Words::DocumentBase> &doc, Aspose::Words::Drawing::ShapeType shapeType)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| doc | const System::SharedPtr\<Aspose::Words::DocumentBase\>\& | المستند المالك. |
| shapeType | Aspose::Words::Drawing::ShapeType | نوع الشكل الذي سيتم إنشاؤه. |
## ملاحظات


يجب عليك تحديد خصائص الشكل المطلوبة بعد إنشاء الشكل.

## أمثلة



يعرض كيفية إدراج شكل مع صورة من نظام الملفات المحلي في مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// المُنشئ العام لفئة "Shape" سيُنشئ شكلاً بنوع الترميز "ShapeMarkupLanguage.Vml".
// إذا كنت بحاجة إلى إنشاء شكل من نوع غير أولي، مثل SingleCornerSnipped، TopCornersSnipped، DiagonalCornersSnipped،
// TopCornersOneRoundedOneSnipped، SingleCornerRounded، TopCornersRounded، أو DiagonalCornersRounded،
// يرجى استخدام DocumentBuilder.InsertShape.
auto shape = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::Image);
shape->get_ImageData()->SetImage(get_ImageDir() + u"Windows MetaFile.wmf");
shape->set_Width(100);
shape->set_Height(100);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(shape);

doc->Save(get_ArtifactsDir() + u"Image.FromFile.docx");
```


يظهر كيفية إنشاء وتنسيق مربع نص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// إنشاء مربع نص عائم.
auto textBox = System::MakeObject<Aspose::Words::Drawing::Shape>(doc, Aspose::Words::Drawing::ShapeType::TextBox);
textBox->set_WrapType(Aspose::Words::Drawing::WrapType::None);
textBox->set_Height(50);
textBox->set_Width(200);

// تعيين المحاذاة الأفقية والعمودية للنص داخل الشكل.
textBox->set_HorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Center);
textBox->set_VerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Top);

// إضافة فقرة إلى مربع النص وإضافة سلسلة نصية سيعرضها مربع النص.
textBox->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc));
System::SharedPtr<Aspose::Words::Paragraph> para = textBox->get_FirstParagraph();
para->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
auto run = System::MakeObject<Aspose::Words::Run>(doc);
run->set_Text(u"Hello world!");
para->AppendChild<System::SharedPtr<Aspose::Words::Run>>(run);

doc->get_FirstSection()->get_Body()->get_FirstParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Drawing::Shape>>(textBox);

doc->Save(get_ArtifactsDir() + u"Shape.CreateTextBox.docx");
```

## انظر أيضًا

* Class [DocumentBase](../../../aspose.words/documentbase/)
* Enum [ShapeType](../../shapetype/)
* Class [Shape](../)
* Namespace [Aspose::Words::Drawing](../../)
* Library [Aspose.Words for C++](../../../)
