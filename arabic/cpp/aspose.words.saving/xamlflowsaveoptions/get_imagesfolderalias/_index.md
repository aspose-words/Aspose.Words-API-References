---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias طريقة"
linktitle: "get_ImagesFolderAlias"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias طريقة. يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند XAML. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 5000
url: /ar/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolderalias/
---
## XamlFlowSaveOptions::get_ImagesFolderAlias method


يحدد اسم المجلد المستخدم لإنشاء عناوين URI للصور المكتوبة في مستند XAML. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolderAlias() const
```

## ملاحظات


عند حفظ [Document](../../../aspose.words/document/) بتنسيق XAML، تحتاج Aspose.Words إلى حفظ جميع الصور المدمجة في المستند كملفات مستقلة. يسمح لك [ImagesFolder](../get_imagesfolder/) بتحديد مكان حفظ الصور و[ImagesFolderAlias](./) بتحديد كيفية إنشاء عناوين URI للصور.

إذا لم يكن [ImagesFolderAlias](./) سلسلة فارغة، فستكون عنوان URI للصورة المكتوبة في XAML هو *ImagesFolderAlias + <image file name>*.

إذا كان [ImagesFolderAlias](./) سلسلة فارغة، فستكون عنوان URI للصورة المكتوبة في XAML هو *ImagesFolder + <image file name>*.

إذا تم تعيين [ImagesFolderAlias](./) إلى '.' (نقطة)، فسيتم كتابة اسم ملف الصورة إلى XAML دون مسار بغض النظر عن الخيارات الأخرى.

## انظر أيضًا

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
