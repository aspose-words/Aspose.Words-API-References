---
title: "طريقة Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes"
linktitle: "get_RenderNonImageShapes"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes. يحصل على قيمة أو يحددها لتشير إلى ما إذا كان يجب عرض الأشكال غير الصورية وكتابتها إلى مستند Docling JSON الناتج في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/doclingsaveoptions/get_rendernonimageshapes/
---
## DoclingSaveOptions::get_RenderNonImageShapes method


يحصل أو يحدد قيمة تشير إلى ما إذا كان يجب عرض الأشكال غير الصورية وكتابتها إلى مستند Docling JSON الناتج.

```cpp
bool Aspose::Words::Saving::DoclingSaveOptions::get_RenderNonImageShapes() const
```


## أمثلة



يوضح كيفية حفظ مستند بتنسيق Docling JSON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::DoclingSaveOptions>();
saveOptions->set_SaveFormat(Aspose::Words::SaveFormat::Docling);
// اضبطه على true لعرض الأشكال غير الصورية وتضمينها في الناتج.
// اضبطه على false (الافتراضي) لاستبعاد الأشكال غير الصورية من الناتج.
saveOptions->set_RenderNonImageShapes(true);

doc->Save(get_ArtifactsDir() + u"Document.DoclingJson.json", saveOptions);
```

## انظر أيضًا

* Class [DoclingSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
