---
title: "Aspose::Words::Font::get_Italic طريقة"
linktitle: "get_Italic"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_Italic. True إذا كان الخط مُنسقًا كمائل في C++."
type: docs
weight: 18000
url: /ar/cpp/aspose.words/font/get_italic/
---
## Font::get_Italic method


صحيح إذا كان الخط منسقًا كإيطالي.

```cpp
bool Aspose::Words::Font::get_Italic()
```


## أمثلة



يوضح كيفية كتابة نص مائل باستخدام مُنشئ المستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->set_Size(36);
builder->get_Font()->set_Italic(true);
builder->Writeln(u"Hello world!");

doc->Save(get_ArtifactsDir() + u"Font.Italic.docx");
```

## انظر أيضًا

* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
