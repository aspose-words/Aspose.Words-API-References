---
title: "Aspose::Words::Font::get_LocaleIdFarEast طريقة"
linktitle: "get_LocaleIdFarEast"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_LocaleIdFarEast طريقة. يسترجع أو يعيّن معرف الإعداد الإقليمي (اللغة) للأحرف الآسيوية المُنسقة في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words/font/get_localeidfareast/
---
## Font::get_LocaleIdFarEast method


يحصل على أو يضبط معرف الإعداد المحلي (اللغة) للأحرف الآسيوية المُنسقة.

```cpp
int32_t Aspose::Words::Font::get_LocaleIdFarEast()
```


## أمثلة



يظهر كيفية إدراج وتنسيق النص بلغة الشرق الأقصى.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد إعدادات الخط التي سيطبقها منشئ المستند على أي نص يتم إدراجه.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// سمّ ما يعادل "FarEast" للخط والإعداد الإقليمي الخاص بنا.
// إذا كان المنشئ يُدرج أحرفًا آسيوية باستخدام تكوين الخط هذا، فكل مقطع يحتوي على
// ستعرض هذه الأحرف باستخدام الخط/الإعداد الإقليمي "FarEast" بدلاً من الافتراضي.
// قد يكون هذا مفيدًا عندما لا يمتلك الخط الغربي تمثيلات مثالية للأحرف الآسيوية.
builder->get_Font()->set_NameFarEast(u"SimSun");
builder->get_Font()->set_LocaleIdFarEast(System::MakeObject<System::Globalization::CultureInfo>(u"zh-CN", false)->get_LCID());

// سيتم عرض هذا النص بالخط/الإعداد الإقليمي الافتراضي.
builder->Writeln(u"Hello world!");

// نظرًا لأن هذه أحرف آسيوية، سيطبق هذا المقطع ما يعادل الخط/الإعداد الإقليمي "FarEast" الخاص بنا.
builder->Writeln(u"你好世界");

doc->Save(get_ArtifactsDir() + u"Font.FarEast.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
