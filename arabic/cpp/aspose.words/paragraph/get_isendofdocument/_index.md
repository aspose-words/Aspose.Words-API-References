---
title: "Aspose::Words::Paragraph::get_IsEndOfDocument طريقة"
linktitle: "get_IsEndOfDocument"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Paragraph::get_IsEndOfDocument طريقة. صحيح إذا كان هذا الفقرة هي الفقرة الأخيرة في آخر قسم من المستند في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/paragraph/get_isendofdocument/
---
## Paragraph::get_IsEndOfDocument method


صحيح إذا كانت هذه الفقرة هي الفقرة الأخيرة في القسم الأخير من المستند.

```cpp
bool Aspose::Words::Paragraph::get_IsEndOfDocument()
```


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

* Class [Paragraph](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
