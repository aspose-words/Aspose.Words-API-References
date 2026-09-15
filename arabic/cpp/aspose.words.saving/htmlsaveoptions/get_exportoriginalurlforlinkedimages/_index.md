---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages طريقة"
linktitle: "get_ExportOriginalUrlForLinkedImages"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages طريقة. يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هي false في C++."
type: docs
weight: 22000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages method


يحدد ما إذا كان يجب استخدام عنوان URL الأصلي كعنوان URL للصور المرتبطة. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportOriginalUrlForLinkedImages() const
```

## ملاحظات


إذا تم تعيين القيمة إلى **true**[SourceFullName](../../../aspose.words.drawing/imagedata/get_sourcefullname/) تُستخدم القيمة كعنوان URL للصور المرتبطة ولا يتم تحميل الصور المرتبطة إلى مجلد المستند أو إلى [ImagesFolder](../get_imagesfolder/).

إذا تم تعيين القيمة إلى **false** تُحمَّل الصور المرتبطة إلى مجلد المستند أو إلى [ImagesFolder](../get_imagesfolder/) ويتم إنشاء عنوان URL لكل صورة مرتبطة بناءً على مجلد المستند، و[ImagesFolder](../get_imagesfolder/) و[ImagesFolderAlias](../get_imagesfolderalias/) الخاصيات.

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
