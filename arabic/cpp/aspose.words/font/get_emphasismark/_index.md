---
title: "طريقة Aspose::Words::Font::get_EmphasisMark"
linktitle: "get_EmphasisMark"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Font::get_EmphasisMark. يحصل على أو يضبط علامة التأكيد المطبقة على هذا التنسيق في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/font/get_emphasismark/
---
## Font::get_EmphasisMark method


يحصل على أو يضبط علامة التأكيد المطبقة على هذا التنسيق.

```cpp
Aspose::Words::EmphasisMark Aspose::Words::Font::get_EmphasisMark()
```


## أمثلة



يظهر كيفية إضافة حرف إضافي يُعرض فوق/تحت حرف الشكل.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

// الأنواع الممكنة لعلامة التأكيد:
// https://apireference.aspose.com/words/net/aspose.words/emphasismark
builder->get_Font()->set_EmphasisMark(emphasisMark);

builder->Write(u"Emphasis text");
builder->Writeln();
builder->get_Font()->ClearFormatting();
builder->Write(u"Simple text");

builder->get_Document()->Save(get_ArtifactsDir() + u"Fonts.SetEmphasisMark.docx");
```

## انظر أيضًا

* Enum [EmphasisMark](../../emphasismark/)
* Class [Font](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
