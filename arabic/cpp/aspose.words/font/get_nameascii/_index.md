---
title: "Aspose::Words::Font::get_NameAscii طريقة"
linktitle: "get_NameAscii"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_NameAscii طريقة. تُرجع أو تُعيّن الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الحروف من 0 (صفر) إلى 127) في C++."
type: docs
weight: 26000
url: /ar/cpp/aspose.words/font/get_nameascii/
---
## Font::get_NameAscii method


يعيد أو يضبط الخط المستخدم للنص اللاتيني (الأحرف ذات رموز الأحرف من 0 (صفر) إلى 127).

```cpp
System::String Aspose::Words::Font::get_NameAscii()
```


## أمثلة



يظهر كيف يمكن لبرنامج Microsoft Word دمج خطين مختلفين في مقطع واحد.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// افترض وجود مقطع نستخدم المُنشئ لإدراجه مع تكوين الخط هذا.
// يحتوي على أحرف ضمن نطاق أحرف ASCII. في هذه الحالة،
// سيتم عرض تلك الأحرف باستخدام هذا الخط.
builder->get_Font()->set_NameAscii(u"Calibri");

// بدون تحديد خط آخر، سيطبق المُنشئ هذا الخط أيضًا على جميع الأحرف التي يُدخلها.
ASSERT_EQ(u"Calibri", builder->get_Font()->get_Name());

// حدد خطًا لاستخدامه لجميع الأحرف خارج نطاق ASCII.
// من الناحية المثالية، يجب أن يحتوي هذا الخط على رموز لكل رمز حرف غير ASCII مطلوب.
builder->get_Font()->set_NameOther(u"Courier New");

// أدرج مقطعًا بكلمة واحدة تتكون من أحرف ASCII، وكلمة أخرى تحتوي على جميع الأحرف خارج ذلك النطاق.
// سيتم عرض كل حرف باستخدام أحد الخطين، حسب.
builder->Writeln(u"Hello, Привет");

doc->Save(get_ArtifactsDir() + u"Font.NameAscii.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
