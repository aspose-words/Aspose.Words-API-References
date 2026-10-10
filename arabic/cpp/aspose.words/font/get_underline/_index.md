---
title: "Aspose::Words::Font::get_Underline طريقة"
linktitle: "get_Underline"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_Underline طريقة. يسترجع أو يعيّن نوع التسطير المطبّق على الخط في C++."
type: docs
weight: 55000
url: /ar/cpp/aspose.words/font/get_underline/
---
## Font::get_Underline method


يحصل أو يضبط نوع الخط السفلي المطبق على الخط.

```cpp
Aspose::Words::Underline Aspose::Words::Font::get_Underline()
```


## أمثلة



يوضح كيفية إدراج نص منسق باستخدام [DocumentBuilder](../../documentbuilder/).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد تنسيق الخط، ثم أضف النص.
System::SharedPtr<Aspose::Words::Font> font = builder->get_Font();
font->set_Size(16);
font->set_Bold(true);
font->set_Color(System::Drawing::Color::get_Blue());
font->set_Name(u"Courier New");
font->set_Underline(Aspose::Words::Underline::Dash);

builder->Write(u"Hello world!");
```


يظهر كيفية إدراج حقل ارتباط تشعبي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->Write(u"For more information, please visit the ");

// أدرج ارتباطًا تشعبيًا وأبرزه بتنسيق مخصص.
// سيكون الارتباط التشعبي قطعة نصية قابلة للنقر ستنقلنا إلى الموقع المحدد في عنوان URL.
builder->get_Font()->set_Color(System::Drawing::Color::get_Blue());
builder->get_Font()->set_Underline(Aspose::Words::Underline::Single);
builder->InsertHyperlink(u"Google website", u"https://www.google.com", false);
builder->get_Font()->ClearFormatting();
builder->Writeln(u".");

// ستؤدي عملية الضغط على Ctrl + النقر الأيسر على الرابط في النص داخل Microsoft Word إلى الانتقال إلى عنوان URL عبر نافذة متصفح ويب جديدة.
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertHyperlink.docx");
```


يظهر كيفية تكوين نمط ولون الخط السفلي للنص.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Underline(Aspose::Words::Underline::Dotted);
builder->get_Font()->set_UnderlineColor(System::Drawing::Color::get_Red());

builder->Writeln(u"Underlined text.");

doc->Save(get_ArtifactsDir() + u"Font.Underlines.docx");
```

## انظر أيضًا

* Enum [Underline](../../underline/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
