---
title: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting method"
linktitle: "get_ExportUnderlineFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting method. يحصل أو يضبط قيمة منطقية تشير إلى ما إذا كان يجب تصدير تنسيق النص المسطر كسلسلة من حرفين زائد \"++\". القيمة الافتراضية هي false في C++."
type: docs
weight: 3500
url: /ar/cpp/aspose.words.saving/markdownsaveoptions/get_exportunderlineformatting/
---
## MarkdownSaveOptions::get_ExportUnderlineFormatting method


يحصل أو يعيّن قيمة منطقية تشير إلى ما إذا كان سيتم تصدير تنسيق النص المسطر كسلسلة من حرفي زائد "++". القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportUnderlineFormatting() const
```


## أمثلة



يوضح كيفية تصدير تنسيق الخط المسطر ك ++.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->set_Underline(Aspose::Words::Underline::Single);
builder->Write(u"Lorem ipsum. Dolor sit amet.");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportUnderlineFormatting(true);
doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportUnderlineFormatting.md", saveOptions);
```

## انظر أيضًا

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
