---
title: "طريقة Aspose::Words::Font::get_Color"
linktitle: "get_Color"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Color. يحصل على أو يضبط لون الخط في C++."
type: docs
weight: 9000
url: /ar/cpp/aspose.words/font/get_color/
---
## Font::get_Color method


يحصل على أو يضبط لون الخط.

```cpp
System::Drawing::Color Aspose::Words::Font::get_Color()
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

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
