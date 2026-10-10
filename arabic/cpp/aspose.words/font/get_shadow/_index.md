---
title: "طريقة Aspose::Words::Font::get_Shadow"
linktitle: "get_Shadow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Shadow. صحيح إذا كان الخط مُنسقًا كظل في C++."
type: docs
weight: 35000
url: /ar/cpp/aspose.words/font/get_shadow/
---
## Font::get_Shadow method


صحيح إذا كان الخط منسقًا كظل.

```cpp
bool Aspose::Words::Font::get_Shadow()
```


## أمثلة



يظهر كيفية إنشاء مقطع نصي مُنسق بظل.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// قم بتعيين علامة Shadow لتطبيق تأثير ظل مُزاح،
// مما يجعل الحروف تبدو كأنها تطفو فوق الصفحة.
builder->get_Font()->set_Shadow(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text has a shadow.");

doc->Save(get_ArtifactsDir() + u"Font.Shadow.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
