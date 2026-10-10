---
title: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder"
linktitle: "get_ResourcesFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder. تحدد المجلد الفعلي حيث تُحفظ الموارد (الصور) عند تصدير مستند إلى تنسيق Svg. القيمة الافتراضية هي null في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/svgsaveoptions/get_resourcesfolder/
---
## SvgSaveOptions::get_ResourcesFolder method


يحدد المجلد الفعلي حيث يتم حفظ الموارد (الصور) عند تصدير مستند إلى تنسيق Svg. القيمة الافتراضية هي **null**.

```cpp
System::String Aspose::Words::Saving::SvgSaveOptions::get_ResourcesFolder() const
```

## ملاحظات


يكون له تأثير فقط إذا كانت الخاصية [ExportEmbeddedImages](../get_exportembeddedimages/) **false**.

عند حفظ [Document](../../../aspose.words/document/) بتنسيق SVG، تحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. يتيح لك [ResourcesFolder](./) تحديد مكان حفظ الصور و[ResourcesFolderAlias](../get_resourcesfolderalias/) لتحديد كيفية إنشاء عناوين URI للصور.

إذا حفظت مستندًا في ملف وقدمت اسم ملف، فإن Aspose.Words، بشكل افتراضي، يحفظ الصور في نفس المجلد الذي يُحفظ فيه ملف المستند. استخدم [ResourcesFolder](./) لتجاوز هذا السلوك.

إذا قمت بحفظ مستند إلى تدفق، لا تمتلك Aspose.Words مجلدًا لحفظ الصور، لكنها لا تزال تحتاج إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه في خاصية [ResourcesFolder](./).

## انظر أيضًا

* Class [SvgSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
