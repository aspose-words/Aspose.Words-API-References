---
title: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder طريقة"
linktitle: "get_ImagesFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder طريقة. يحدد المجلد الفعلي حيث يتم حفظ الصور عند تصدير مستند إلى تنسيق XAML. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words.saving/xamlflowsaveoptions/get_imagesfolder/
---
## XamlFlowSaveOptions::get_ImagesFolder method


يحدد المجلد الفعلي حيث تُحفظ الصور عند تصدير مستند إلى تنسيق XAML. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::XamlFlowSaveOptions::get_ImagesFolder() const
```

## ملاحظات


عند حفظ [Document](../../../aspose.words/document/) بتنسيق XAML، تحتاج Aspose.Words إلى حفظ جميع الصور المدمجة في المستند كملفات مستقلة. يسمح لك [ImagesFolder](./) بتحديد مكان حفظ الصور و[ImagesFolderAlias](../get_imagesfolderalias/) بتحديد كيفية إنشاء عناوين URI للصور.

إذا حفظت مستندًا في ملف وقدمت اسم ملف، يقوم Aspose.Words، بشكل افتراضي، بحفظ الصور في نفس المجلد الذي يُحفظ فيه ملف المستند. استخدم [ImagesFolder](./) لتجاوز هذا السلوك.

إذا حفظت مستندًا في تدفق، لا يمتلك Aspose.Words مجلدًا لحفظ الصور، لكنه لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في خاصية [ImagesFolder](./) أو توفير تدفقات مخصصة عبر معالج الحدث [ImageSavingCallback](../get_imagesavingcallback/).

## انظر أيضًا

* Class [XamlFlowSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
