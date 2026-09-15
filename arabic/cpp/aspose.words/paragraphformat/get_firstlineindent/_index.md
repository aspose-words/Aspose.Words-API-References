---
title: "طريقة Aspose::Words::ParagraphFormat::get_FirstLineIndent"
linktitle: "get_FirstLineIndent"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::ParagraphFormat::get_FirstLineIndent. يحصل على أو يضبط القيمة (بالنقاط) للمسافة البادئة للسطر الأول أو المعلقة. استخدم القيم الموجبة لتعيين المسافة البادئة للسطر الأول، والقيم السالبة لتعيين المسافة المعلقة في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/paragraphformat/get_firstlineindent/
---
## ParagraphFormat::get_FirstLineIndent method


يحصل أو يضبط القيمة (بالنقاط) للمسافة البادئة للسطر الأول أو المعلقة. استخدم القيم الموجبة لضبط مسافة البادئة للسطر الأول، والقيم السالبة لضبط المسافة المعلقة.

```cpp
double Aspose::Words::ParagraphFormat::get_FirstLineIndent()
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

* Class [ParagraphFormat](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
