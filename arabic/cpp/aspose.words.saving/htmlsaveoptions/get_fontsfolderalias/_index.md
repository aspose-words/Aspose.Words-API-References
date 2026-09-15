---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias"
linktitle: "get_FontsFolderAlias"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias. تحدد اسم المجلد المستخدم لإنشاء عناوين URI للخطوط المكتوبة في مستند HTML. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 34000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolderalias/
---
## HtmlSaveOptions::get_FontsFolderAlias method


يحدد اسم المجلد المستخدم لإنشاء عناوين URI للخطوط المكتوبة في مستند HTML. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolderAlias() const
```

## ملاحظات


عند حفظك لـ [Document](../../../aspose.words/document/) بتنسيق HTML وتعيين [ExportFontResources](../get_exportfontresources/) إلى **true**، تحتاج Aspose.Words إلى حفظ الخطوط المستخدمة في المستند كملفات مستقلة. يتيح لك [FontsFolder](../get_fontsfolder/) تحديد مكان حفظ الخطوط ويتيح [FontsFolderAlias](./) تحديد كيفية إنشاء عناوين URI للخطوط.

إذا لم يكن [FontsFolderAlias](./) سلسلة فارغة، فستكون عناوين URI للخط المكتوبة في HTML هي *FontsFolderAlias + <font file name>*.

إذا كان [FontsFolderAlias](./) سلسلة فارغة، فستكون عناوين URI للخط المكتوبة في HTML هي *FontsFolder + <font file name>*.

إذا تم تعيين [FontsFolderAlias](./) إلى '.' (نقطة)، فسيتم كتابة اسم ملف الخط في HTML بدون مسار بغض النظر عن الخيارات الأخرى.

طريقة بديلة لتحديد اسم المجلد لإنشاء عناوين URI للخطوط هي استخدام [ResourceFolderAlias](../get_resourcefolderalias/).

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
