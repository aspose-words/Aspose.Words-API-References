---
title: "طريقة Aspose::Words::Font::get_LocaleId method"
linktitle: "get_LocaleId"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_LocaleId method. يحصل أو يضبط معرف الإعداد الإقليمي (اللغة) للأحرف المُنسقة في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words/font/get_localeid/
---
## Font::get_LocaleId method


يحصل على أو يضبط معرف الإعداد المحلي (اللغة) للأحرف المُنسقة.

```cpp
int32_t Aspose::Words::Font::get_LocaleId()
```


## أمثلة



يظهر كيفية ضبط الإعداد الإقليمي للنص الذي نضيفه باستخدام منشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إذا قمنا بضبط الإعداد الإقليمي للخط إلى الإنجليزية وأدخلنا بعض النص الروسي،
// فلن يتعرف مدقق الإملاء للإنجليزية على النص وسيُصنّفه كخطأ إملائي.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());
builder->Writeln(u"Привет!");

// اضبط إعدادًا إقليميًا مطابقًا للنص الذي نحن على وشك إضافته لتطبيق مدقق الإملاء المناسب.
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"ru-RU", false)->get_LCID());
builder->Writeln(u"Привет!");

doc->Save(get_ArtifactsDir() + u"Font.LocaleId.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
