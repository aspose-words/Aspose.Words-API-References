---
title: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder"
linktitle: "get_ResourcesFolder"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder. يحدد المجلد الفعلي حيث تُحفظ الموارد (الصور، الخطوط، css) عند تصدير مستند إلى تنسيق Html. القيمة الافتراضية هي null في C++."
type: docs
weight: 15000
url: /ar/cpp/aspose.words.saving/htmlfixedsaveoptions/get_resourcesfolder/
---
## HtmlFixedSaveOptions::get_ResourcesFolder method


يحدد المجلد الفعلي حيث تُحفظ الموارد (الصور، الخطوط، css) عند تصدير مستند إلى تنسيق Html. القيمة الافتراضية هي **null**.

```cpp
System::String Aspose::Words::Saving::HtmlFixedSaveOptions::get_ResourcesFolder() const
```

## ملاحظات


يكون له تأثير فقط إذا كانت الخاصية [ExportEmbeddedImages](../get_exportembeddedimages/) **false**.

عند حفظك لـ [Document](../../../aspose.words/document/) بصيغة Html، تحتاج Aspose.Words إلى حفظ جميع الصور المضمنة في المستند كملفات مستقلة. يتيح لك [ResourcesFolder](./) تحديد مكان حفظ الصور و[ResourcesFolderAlias](../get_resourcesfolderalias/) يتيح تحديد كيفية إنشاء عناوين URI للصور.

إذا حفظت مستندًا في ملف وقدمت اسم ملف، فإن Aspose.Words، بشكل افتراضي، يحفظ الصور في نفس المجلد الذي يُحفظ فيه ملف المستند. استخدم [ResourcesFolder](./) لتجاوز هذا السلوك.

إذا حفظت مستندًا في تدفق، لا تملك Aspose.Words مجلدًا لحفظ الصور، ولكن لا يزال بحاجة إلى حفظ الصور في مكان ما. في هذه الحالة، تحتاج إلى تحديد مجلد يمكن الوصول إليه باستخدام خاصية [ResourcesFolder](./).

## انظر أيضًا

* Class [HtmlFixedSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
