---
title: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64"
linktitle: "get_ExportImagesAsBase64"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64. يحدد ما إذا كانت الصور تُحفظ بتنسيق Base64 في ملف الإخراج. القيمة الافتراضية هي false في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.saving/markdownsaveoptions/get_exportimagesasbase64/
---
## MarkdownSaveOptions::get_ExportImagesAsBase64 method


يحدد ما إذا كانت الصور تُحفظ بتنسيق Base64 في ملف الإخراج. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::MarkdownSaveOptions::get_ExportImagesAsBase64() const
```

## ملاحظات


عند ضبط هذه الخاصية على **true** يتم تصدير بيانات الصور مباشرةً إلى عناصر **img** ولا يتم إنشاء ملفات منفصلة.

## أمثلة



يوضح كيفية حفظ مستند .md مع تضمين الصور داخله.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Images.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
saveOptions->set_ExportImagesAsBase64(exportImagesAsBase64);

doc->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"MarkdownSaveOptions.ExportImagesAsBase64.md");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"data:image/jpeg;base64") : outDocContents.Contains(u"MarkdownSaveOptions.ExportImagesAsBase64.001.jpeg"));
```

## انظر أيضًا

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
