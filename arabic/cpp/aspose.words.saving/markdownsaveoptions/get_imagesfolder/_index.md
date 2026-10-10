---
title: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder"
linktitle: "get_ImagesFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder. يحدد المجلد الفعلي حيث تُحفظ الصور عند تصدير مستند إلى تنسيق Markdown. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/markdownsaveoptions/get_imagesfolder/
---
## MarkdownSaveOptions::get_ImagesFolder method


يحدد المجلد الفعلي حيث تُحفظ الصور عند تصدير مستند إلى تنسيق [Markdown](../../../aspose.words/saveformat/). القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::MarkdownSaveOptions::get_ImagesFolder() const
```

## ملاحظات


عند حفظك لـ [المستند](../../../aspose.words/document/) بتنسيق [Markdown](../../../aspose.words/saveformat/)، تحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. يتيح لك [ImagesFolder](./) تحديد مكان حفظ الصور.

إذا حفظت مستندًا في ملف وقدمت اسم ملف، يقوم Aspose.Words، بشكل افتراضي، بحفظ الصور في نفس المجلد الذي يُحفظ فيه ملف المستند. استخدم [ImagesFolder](./) لتجاوز هذا السلوك.

إذا حفظت مستندًا في تدفق، لا تملك Aspose.Words مجلدًا لحفظ الصور، لكنها لا تزال تحتاج إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في خاصية [ImagesFolder](./).

إذا كان المجلد المحدد بواسطة [ImagesFolder](./) غير موجود، سيتم إنشاؤه تلقائيًا.

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
