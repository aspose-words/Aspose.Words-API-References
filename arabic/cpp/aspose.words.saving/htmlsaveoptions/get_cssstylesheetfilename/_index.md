---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method"
linktitle: "get_CssStyleSheetFileName"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName method. يحدد المسار واسم ملف ورقة الأنماط المتتالية (CSS) الذي يُكتب عند تصدير المستند إلى HTML. القيمة الافتراضية هي سلسلة فارغة في C++."
type: docs
weight: 6000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_cssstylesheetfilename/
---
## HtmlSaveOptions::get_CssStyleSheetFileName method


يحدد المسار واسم ملف ورقة الأنماط المتتالية [Style](../../../aspose.words/style/) (CSS) الذي يُكتب عند تصدير المستند إلى HTML. القيمة الافتراضية هي سلسلة فارغة.

```cpp
System::String Aspose::Words::Saving::HtmlSaveOptions::get_CssStyleSheetFileName() const
```

## ملاحظات


هذه الخاصية لها تأثير فقط عند حفظ مستند بتنسيق HTML ويتم طلب ورقة أنماط CSS خارجية باستخدام [CssStyleSheetType](../get_cssstylesheettype/).

إذا كانت هذه الخاصية فارغة، سيتم حفظ ملف CSS في نفس المجلد وبنفس اسم مستند HTML ولكن بامتداد ".css".

إذا تم تحديد المسار فقط دون اسم ملف في هذه الخاصية، سيتم حفظ ملف CSS في المجلد المحدد وسيحمل نفس اسم مستند HTML ولكن بامتداد ".css".

إذا كان المجلد المحدد بهذه الخاصية غير موجود، فسيتم إنشاؤه تلقائيًا قبل حفظ ملف CSS.

طريقة أخرى لتحديد مجلد يتم فيه حفظ ملف CSS الخارجي هي استخدام [ResourceFolder](../get_resourcefolder/).

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
