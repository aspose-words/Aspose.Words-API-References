---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64"
linktitle: "get_ExportImagesAsBase64"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64. تحدد ما إذا كانت الصور تُحفظ بتنسيق Base64 إلى ملف HTML أو MHTML أو EPUB الناتج. القيمة الافتراضية هي false في C++."
type: docs
weight: 19000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportimagesasbase64/
---
## HtmlSaveOptions::get_ExportImagesAsBase64 method


يحدد ما إذا كانت الصور تُحفظ بتنسيق Base64 في HTML أو MHTML أو EPUB الناتج. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportImagesAsBase64() const
```

## ملاحظات


عند ضبط هذه الخاصية على **true** يتم تصدير بيانات الصور مباشرةً إلى عناصر **img** ولا يتم إنشاء ملفات منفصلة.

## أمثلة



يوضح كيفية حفظ مستند .html مع تضمين الصور داخله.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportImagesAsBase64(exportImagesAsBase64);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html", options);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ExportImagesAsBase64.html");

ASSERT_TRUE(exportImagesAsBase64 ? outDocContents.Contains(u"<img src=\"data:image/png;base64") : outDocContents.Contains(u"<img src=\"HtmlSaveOptions.ExportImagesAsBase64.001.png\""));
```


يوضح كيفية تضمين الخطوط داخل مستند HTML محفوظ.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_ExportFontsAsBase64(true);
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::Embedded);
options->set_PrettyFormat(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ExportFontsAsBase64.html", options);
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
