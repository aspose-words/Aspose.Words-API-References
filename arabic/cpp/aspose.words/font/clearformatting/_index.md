---
title: "طريقة Aspose::Words::Font::ClearFormatting method"
linktitle: "ClearFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::ClearFormatting method. يعيد الضبط إلى تنسيق الخط الافتراضي في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/font/clearformatting/
---
## Font::ClearFormatting method


يعيد الضبط إلى تنسيق الخط الافتراضي.

```cpp
void Aspose::Words::Font::ClearFormatting()
```

## ملاحظات


يزيل جميع تنسيقات الخط المحددة صراحةً على الكائن الذي تم الحصول على [Font](../) منه بحيث يتم وراثة تنسيق الخط من الوالد المناسب.

## أمثلة



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
