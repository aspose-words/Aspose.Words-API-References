---
title: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution"
linktitle: "get_ImageResolution"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution. تحدد دقة الإخراج للصور عند التصدير إلى Markdown. القيمة الافتراضية هي %96 dpi في C++."
type: docs
weight: 3750
url: /ar/cpp/aspose.words.saving/markdownsaveoptions/get_imageresolution/
---
## MarkdownSaveOptions::get_ImageResolution method


يحدد دقة الإخراج للصور عند التصدير إلى Markdown. القيمة الافتراضية هي **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::MarkdownSaveOptions::get_ImageResolution() const
```


## أمثلة



يوضح كيفية تعيين دقة الإخراج للصور.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ImageResolution(300);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImageResolution.md", saveOptions);
```

## انظر أيضًا

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
