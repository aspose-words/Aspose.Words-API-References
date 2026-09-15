---
title: "Aspose::Words::Font::get_Hidden طريقة"
linktitle: "get_Hidden"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Font::get_Hidden طريقة. صحيح إذا كان الخط مُنسقًا كنص مخفي في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words/font/get_hidden/
---
## Font::get_Hidden method


صحيح إذا كان الخط مُنسقًا كنص مخفي.

```cpp
bool Aspose::Words::Font::get_Hidden()
```


## أمثلة



يظهر كيفية إنشاء مقطع نص مخفي.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// مع تعيين علامة Hidden إلى true، أي نص نقوم بإنشائه باستخدام كائن الخط هذا سيكون غير مرئي في المستند.
// لن نرى أو نُبرز النص المخفي إلا إذا فعلنا خيار "Hidden text"
// موجود في Microsoft Word عبر "File" -> "Options" -> "Display". سيظل النص موجودًا هناك،
// وسنتمكن من الوصول إلى هذا النص برمجيًا.
// لا يُنصح باستخدام هذه الطريقة لإخفاء المعلومات الحساسة.
builder->get_Font()->set_Hidden(true);
builder->get_Font()->set_Size(36);

builder->Writeln(u"This text will not be visible in the document.");

doc->Save(get_ArtifactsDir() + u"Font.Hidden.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
