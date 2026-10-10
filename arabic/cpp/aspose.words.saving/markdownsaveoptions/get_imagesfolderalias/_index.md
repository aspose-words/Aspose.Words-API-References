---
title: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias"
linktitle: "get_ImagesFolderAlias"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias. تحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في المستند. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 5500
url: /ar/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolderalias/
---
## MarkdownSaveOptions::get_ImagesFolderAlias method


يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في المستند. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolderAlias() const
```

## ملاحظات


عند حفظك لـ [Document](../../../aspose.words/document/) بتنسيق [Markdown](../../../aspose.words/saveformat/)، تحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. يتيح لك [ImagesFolder](../get_imagesfolder/) تحديد مكان حفظ الصور و[ImagesFolderAlias](./) لتحديد كيفية إنشاء عناوين URI للصور.

إذا لم يكن [ImagesFolderAlias](./) سلسلة فارغة، فستكون عنوان URI للصورة المكتوبة في Markdown هو *ImagesFolderAlias + <image file name>*.

إذا كان [ImagesFolderAlias](./) سلسلة فارغة، فستكون عنوان URI للصورة المكتوبة في Markdown هو *ImagesFolder + <image file name>*.

إذا تم تعيين [ImagesFolderAlias](./) إلى '.' (نقطة)، فسيتم كتابة اسم ملف الصورة في Markdown بدون مسار بغض النظر عن الخيارات الأخرى.

## أمثلة



يوضح كيفية تحديد اسم المجلد المستخدم لإنشاء عناوين URI للصور.
```cpp
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>();

builder->Writeln(u"Some image below:");
builder->InsertImage(get_ImageDir() + u"Logo.jpg");

System::String imagesFolder = System::IO::Path::Combine(get_ArtifactsDir(), u"ImagesDir");
auto saveOptions = System::MakeObject<Aspose::Words::Saving::MarkdownSaveOptions>();
// استخدم خاصية "ImagesFolder" لتعيين مجلد في نظام الملفات المحلي إلى حيث
// ستقوم Aspose.Words بحفظ جميع الصور المرتبطة بالمستند.
saveOptions->set_ImagesFolder(imagesFolder);
// استخدم خاصية "ImagesFolderAlias" لاستخدام هذا المجلد
// عند إنشاء عناوين URI للصور بدلاً من اسم مجلد الصور.
saveOptions->set_ImagesFolderAlias(u"http://example.com/images");

builder->get_Document()->Save(get_ArtifactsDir() + u"MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

## انظر أيضًا

* Class [MarkdownSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
