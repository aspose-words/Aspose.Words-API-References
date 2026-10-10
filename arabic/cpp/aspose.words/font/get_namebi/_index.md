---
title: "طريقة Aspose::Words::Font::get_NameBi"
linktitle: "get_NameBi"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_NameBi. يرجع أو يضبط اسم الخط في مستند بلغة من اليمين إلى اليسار في C++."
type: docs
weight: 27000
url: /ar/cpp/aspose.words/font/get_namebi/
---
## Font::get_NameBi method


يعيد أو يضبط اسم الخط في مستند بلغة من اليمين إلى اليسار.

```cpp
System::String Aspose::Words::Font::get_NameBi()
```


## أمثلة



يوضح كيفية تعريف مجموعات منفصلة من إعدادات الخط للنص من اليمين إلى اليسار، والنص من اليمين إلى اليسار.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// حدد مجموعة من إعدادات الخط للنص من اليسار إلى اليمين.
builder->get_Font()->set_Name(u"Courier New");
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Italic(false);
builder->get_Font()->set_Bold(false);
builder->get_Font()->set_LocaleId(System::MakeObject<System::Globalization::CultureInfo>(u"en-US", false)->get_LCID());

// حدد مجموعة أخرى من إعدادات الخط للنص من اليمين إلى اليسار.
builder->get_Font()->set_NameBi(u"Andalus");
builder->get_Font()->set_SizeBi(24);
builder->get_Font()->set_ItalicBi(true);
builder->get_Font()->set_BoldBi(true);
builder->get_Font()->set_LocaleIdBi(System::MakeObject<System::Globalization::CultureInfo>(u"ar-AR", false)->get_LCID());

// يمكننا استخدام علم Bidi لتحديد ما إذا كان النص الذي نحن على وشك إضافته
// مع مُنشئ المستند هو من اليمين إلى اليسار. عندما نضيف نصًا مع تعيين هذا العلم إلى true،
// سيتم تنسيقه باستخدام مجموعة إعدادات الخط من اليمين إلى اليسار.
builder->get_Font()->set_Bidi(true);
builder->Write(u"مرحبًا");

// عيّن العلم إلى false، ثم أضف نصًا من اليسار إلى اليمين.
// سوف يقوم مُنشئ المستند بتنسيق هذه باستخدام مجموعة إعدادات الخط من اليسار إلى اليمين.
builder->get_Font()->set_Bidi(false);
builder->Write(u" Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Bidi.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
