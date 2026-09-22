---
title: "تعداد Aspose::Words::Underline"
linktitle: "تسطير"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "تعداد Aspose::Words::Underline. يشير إلى نوع التسطير المطبق على الخط في C++."
type: docs
weight: 126000
url: /ar/cpp/aspose.words/underline/
---
## Underline enum


يشير إلى نوع الخط السفلي المطبق على الخط.

```cpp
enum class Underline
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 |  |
| Single | 1 |  |
| Words | 2 |  |
| Double | 3 |  |
| Dotted | 4 |  |
| Thick | 6 |  |
| Dash | 7 |  |
| DashLong | 39 |  |
| DotDash | 9 |  |
| DotDotDash | 10 |  |
| Wavy | 11 |  |
| DottedHeavy | 20 |  |
| DashHeavy | 23 |  |
| DashLongHeavy | 55 |  |
| DotDashHeavy | 25 |  |
| DotDotDashHeavy | 26 |  |
| WavyHeavy | 27 |  |
| WavyDouble | 43 |  |


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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
