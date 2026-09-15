---
title: "طريقة Aspose::Words::DocumentBuilder::InsertParagraph"
linktitle: "InsertParagraph"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::InsertParagraph. تُدرج فاصل فقرة في المستند في C++."
type: docs
weight: 44000
url: /ar/cpp/aspose.words/documentbuilder/insertparagraph/
---
## DocumentBuilder::InsertParagraph method


يقوم بإدراج فاصل فقرة في المستند.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::DocumentBuilder::InsertParagraph()
```


### ReturnValue

عقدة الفقرة التي تم إدراجها للتو. إنها نفس العقدة كما في [CurrentParagraph](../get_currentparagraph/).
## ملاحظات


يتم استخدام تنسيق الفقرة الحالي المحدد بواسطة الخاصية [ParagraphFormat](../get_paragraphformat/).

يقسم الفقرة الحالية إلى جزأين. بعد إدراج الفقرة، يُوضع المؤشر في بداية الفقرة الجديدة.

يتم إلقاء استثناء إذا لم يكن من الممكن إدراج فاصل فقرة في موضع المؤشر الحالي.

## أمثلة



يظهر كيفية إدراج فقرة في المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Arial");
font->set_Underline(Aspose::Words::Underline::Dash);

System::SharedPtr<Aspose::Words::ParagraphFormat> paragraphFormat = builder->get_ParagraphFormat();
paragraphFormat->set_FirstLineIndent(8);
paragraphFormat->set_Alignment(Aspose::Words::ParagraphAlignment::Justify);
paragraphFormat->set_AddSpaceBetweenFarEastAndAlpha(true);
paragraphFormat->set_AddSpaceBetweenFarEastAndDigit(true);
paragraphFormat->set_KeepTogether(true);

// طريقة "Writeln" تنهي الفقرة بعد إلحاق النص
// ثم تبدأ سطرًا جديدًا، مضيفة فقرة جديدة.
builder->Writeln(u"Hello world!");

ASSERT_TRUE(builder->get_CurrentParagraph()->get_IsEndOfDocument());
```

## انظر أيضًا

* Class [Paragraph](../../paragraph/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
