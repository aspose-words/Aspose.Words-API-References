---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution طريقة"
linktitle: "get_ImageResolution"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution طريقة. يحدد دقة الإخراج للصور عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي %96 dpi في C++."
type: docs
weight: 36000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_imageresolution/
---
## HtmlSaveOptions::get_ImageResolution method


يحدد دقة الإخراج للصور عند التصدير إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **%96 dpi**.

```cpp
int32_t Aspose::Words::Saving::HtmlSaveOptions::get_ImageResolution() const
```

## ملاحظات


تؤثر هذه الخاصية على الصور النقطية عندما يكون [ScaleImageToShapeSize](../get_scaleimagetoshapesize/) **true** وتؤثر على ملفات الميتا المصدرة كصور نقطية. بعض خصائص الصورة مثل القص أو الدوران تتطلب حفظ الصور المحوّلة وفي هذه الحالة تُنشأ الصور المحوّلة بالدقة المحددة.

## أمثلة



يوضح كيفية تعيين المجلدات وأسماء المستعارة للمجلدات للموارد المحفوظة خارجيًا التي سيقوم Aspose.Words بإنشائها عند حفظ المستند إلى HTML.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_CssStyleSheetType(Aspose::Words::Saving::CssStyleSheetType::External);
options->set_ExportFontResources(true);
options->set_ImageResolution(72);
options->set_FontResourcesSubsettingSizeThreshold(0);
options->set_FontsFolder(get_ArtifactsDir() + u"Fonts");
options->set_ImagesFolder(get_ArtifactsDir() + u"Images");
options->set_ResourceFolder(get_ArtifactsDir() + u"Resources");
options->set_FontsFolderAlias(u"http://example.com/fonts");
options->set_ImagesFolderAlias(u"http://example.com/images");
options->set_ResourceFolderAlias(u"http://example.com/resources");
options->set_ExportOriginalUrlForLinkedImages(true);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.FolderAlias.html", options);
```

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
