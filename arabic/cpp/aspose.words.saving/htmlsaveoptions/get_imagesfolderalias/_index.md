---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias طريقة"
linktitle: "get_ImagesFolderAlias"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias. تحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند HTML. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 39000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_imagesfolderalias/
---
## HtmlSaveOptions::get_ImagesFolderAlias method


يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند HTML. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_ImagesFolderAlias() const
```

## ملاحظات


عند حفظ [Document](../../../aspose.words/document/) بصيغة HTML، تحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. يتيح لك [ImagesFolder](../get_imagesfolder/) تحديد مكان حفظ الصور و[ImagesFolderAlias](./) لتحديد كيفية إنشاء عناوين URI للصور.

إذا كان [ImagesFolderAlias](./) ليس سلسلة فارغة، فإن عنوان URI للصورة المكتوب في HTML سيكون *ImagesFolderAlias + <image file name>*.

إذا كان [ImagesFolderAlias](./) سلسلة فارغة، فإن عنوان URI للصورة المكتوب في HTML سيكون *ImagesFolder + <image file name>*.

إذا تم تعيين [ImagesFolderAlias](./) إلى '.' (نقطة)، فسيتم كتابة اسم ملف الصورة في HTML بدون مسار بغض النظر عن الخيارات الأخرى.

طريقة بديلة لتحديد اسم المجلد لإنشاء عناوين URI للصور هي استخدام [ResourceFolderAlias](../get_resourcefolderalias/).

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
