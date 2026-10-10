---
title: "Aspose::Words::ParagraphFormat::get_LeftIndent طريقة"
linktitle: "get_LeftIndent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ParagraphFormat::get_LeftIndent طريقة. يحصل أو يضبط القيمة (بالنقاط) التي تمثل المسافة البادئة اليسرى للفقرة في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words/paragraphformat/get_leftindent/
---
## ParagraphFormat::get_LeftIndent method


يحصل أو يضبط القيمة (بالنقاط) التي تمثل المسافة البادئة اليسرى للفقرة.

```cpp
double Aspose::Words::ParagraphFormat::get_LeftIndent()
```


## أمثلة



يظهر كيفية تكوين تنسيق الفقرة لإنشاء نص غير مركزي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتمركز جميع النصوص التي يكتبها منشئ المستند، واضبط الهوامش.
// ستنشئ إعدادات الهوامش أدناه جسمًا من النص سيجلس بشكل غير متماثل على الصفحة.
// سيكون "center" الذي نُحاذِر النص إليه هو منتصف جسم النص، وليس منتصف الصفحة.
System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
paragraphFormat->set_LeftIndent(100);
paragraphFormat->set_RightIndent(50);
paragraphFormat->set_SpaceAfter(25);

builder->Writeln(u"This paragraph demonstrates how left and right indentation affects word wrapping.");
builder->Writeln(u"The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetParagraphFormatting.docx");
```

## انظر أيضًا

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
