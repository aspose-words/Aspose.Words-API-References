---
title: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow طريقة"
linktitle: "get_OpenHyperlinksInNewWindow"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow طريقة. يحصل أو يضبط قيمة تحدد ما إذا كان سيتم إجبار الروابط التشعبية في مستند Pdf الناتج على الفتح في نافذة جديدة (أو علامة تبويب) في المتصفح في C++."
type: docs
weight: 24000
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_openhyperlinksinnewwindow/
---
## PdfSaveOptions::get_OpenHyperlinksInNewWindow method


يحصل أو يضبط قيمة تحدد ما إذا كانت الروابط التشعبية في مستند Pdf الناتج تُجبر على الفتح في نافذة جديدة (أو تبويب) في المتصفح.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_OpenHyperlinksInNewWindow() const
```

## ملاحظات


القيمة الافتراضية هي **false**. عندما يتم تعيين هذه القيمة إلى **true** يتم حفظ الروابط باستخدام كود JavaScript. كود JavaScript هو **app.launchURL(\"URL\", true);**, حيث **URL** هو رابط.

لاحظ أنه إذا تم تعيين هذا الخيار إلى **true** لا يمكن للروابط العمل في بعض قارئات PDF مثل Chrome و Firefox.

إجراءات JavaScript محظورة وفقًا لمتطلبات PDF/A-1 و PDF/A-2 و PDF/A-3. سيتم استخدام القيمة **false** تلقائيًا في هذه الحالة.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
