---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 طريقة"
linktitle: "get_ExportFontsAsBase64"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64 طريقة. يحدد ما إذا كان يجب تضمين موارد الخطوط إلى HTML بترميز Base64. القيمة الافتراضية هي false في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontsasbase64/
---
## HtmlSaveOptions::get_ExportFontsAsBase64 method


يحدد ما إذا كان يجب تضمين موارد الخطوط في HTML بترميز Base64. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontsAsBase64() const
```

## ملاحظات


بشكل افتراضي، تُكتب الخطوط إلى ملفات منفصلة. إذا تم تعيين هذا الخيار إلى **true**، سيتم تضمين الخطوط في CSS الخاص بالمستند بترميز Base64.

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
