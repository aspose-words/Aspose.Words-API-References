---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources طريقة"
linktitle: "get_ExportFontResources"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources. تحدد ما إذا كان يجب تصدير موارد الخط إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي false في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.saving/htmlsaveoptions/get_exportfontresources/
---
## HtmlSaveOptions::get_ExportFontResources method


يحدد ما إذا كان يجب تصدير موارد الخط إلى HTML أو MHTML أو EPUB. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ExportFontResources() const
```

## ملاحظات


تصدير موارد الخط يسمح بعرض مستند متسق مستقل عن الخطوط المتاحة في بيئة المستخدم المعينة.

إذا تم تعيين [ExportFontResources](./) إلى **true**، سيشير المستند HTML الرئيسي إلى كل خط عبر قاعدة at-rule **%@font-face** في CSS 3 وسيتم إخراج الخطوط كملفات منفصلة. عند التصدير إلى صيغ IDPF EPUB أو MHTML، سيتم تضمين الخطوط في الحزمة المقابلة إلى جانب الملفات الفرعية الأخرى.

إذا تم تعيين [ExportFontsAsBase64](../get_exportfontsasbase64/) إلى **true**، لن يتم حفظ الخطوط كملفات منفصلة. بدلاً من ذلك، سيتم تضمينها في قواعد **%@font-face** بتشفير Base64.

**Important!** When exporting font resources, font licensing issues should be considered. Authors who want to use specific fonts via a downloadable font mechanism must always carefully verify that their intended use is within the scope of the font license. Many commercial fonts presently do not allow web downloading of their fonts in any form. [License](../../../aspose.words/license/) agreements that cover some fonts specifically note that usage via **%@font-face** rules in CSS style sheets is not allowed. [Font](../../../aspose.words/font/) subsetting can also violate license terms.

## انظر أيضًا

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
