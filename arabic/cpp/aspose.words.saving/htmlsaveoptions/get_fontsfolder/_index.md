---
title: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder"
linktitle: "get_FontsFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder. تحدد المجلد الفعلي حيث يتم حفظ الخطوط عند تصدير مستند إلى HTML. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 33000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_fontsfolder/
---
## HtmlSaveOptions::get_FontsFolder method


يحدد المجلد الفعلي حيث تُحفظ الخطوط عند تصدير مستند إلى HTML. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_FontsFolder() const
```

## ملاحظات


عند حفظك لـ [Document](../../../aspose.words/document/) بتنسيق HTML وتعيين [ExportFontResources](../get_exportfontresources/) إلى **true**، تحتاج Aspose.Words إلى حفظ الخطوط المستخدمة في المستند كملفات مستقلة. يتيح لك [FontsFolder](./) تحديد مكان حفظ الخطوط ويتيح [FontsFolderAlias](../get_fontsfolderalias/) تحديد كيفية إنشاء عناوين URI للخطوط.

إذا حفظت مستندًا في ملف وقدمت اسم ملف، فإن Aspose.Words، بشكل افتراضي، يحفظ الخطوط في نفس المجلد الذي يُحفظ فيه ملف المستند. استخدم [FontsFolder](./) لتجاوز هذا السلوك.

إذا حفظت مستندًا في تدفق، لا تملك Aspose.Words مجلدًا لحفظ الخطوط، ولكن لا يزال يحتاج إلى حفظ الخطوط في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في خاصية [FontsFolder](./) أو توفير تدفقات مخصصة عبر معالج الحدث [FontSavingCallback](../get_fontsavingcallback/).

إذا كان المجلد المحدد بواسطة [FontsFolder](./) غير موجود، فسيتم إنشاؤه تلقائيًا.

[ResourceFolder](../get_resourcefolder/) is another way to specify a folder where fonts should be saved.

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
