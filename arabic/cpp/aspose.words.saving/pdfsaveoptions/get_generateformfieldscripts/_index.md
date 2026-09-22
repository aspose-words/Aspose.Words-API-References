---
title: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts"
linktitle: "get_GenerateFormFieldScripts"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts. تحدد ما إذا كان سيتم إنشاء سكريبتات تحاكي سلوك حقول النماذج المحددة في Microsoft Word داخل ملف PDF. القيمة الافتراضية هي false في C++."
type: docs
weight: 18500
url: /ar/cpp/aspose.words.saving/pdfsaveoptions/get_generateformfieldscripts/
---
## PdfSaveOptions::get_GenerateFormFieldScripts method


يحدد ما إذا كان يجب إنشاء سكريبتات تحاكي سلوك حقول النماذج الخاصة بـ Microsoft Word في PDF. القيمة الافتراضية هي **false**.

```cpp
bool Aspose::Words::Saving::PdfSaveOptions::get_GenerateFormFieldScripts() const
```

## ملاحظات


عند تمكين هذا الخيار، يقوم المُصدّر بإنشاء إجراءات JavaScript في PDF لمحاكاة سلوك حقول نماذج Microsoft Word، مثل حقول التاريخ والوقت مع التنسيق وقواعد التحقق.

عند ضبطه على **true**، سيتم تصدير السلوك المدعوم كإجراءات JavaScript في PDF. وعند ضبطه على **false**، لن يتم إنشاء أي سكريبتات لحقول النماذج.

تعتمد تنفيذ السكريبتات على عارض PDF. قد يتجاهل بعض عارضات PDF السكريبتات، أو يقيد تنفيذها، أو يتطلب من المستخدم تمكين JavaScript.

إجراءات JavaScript محظورة وفقًا لمتطلبات PDF/A-1 و PDF/A-2 و PDF/A-3. سيتم استخدام القيمة **false** تلقائيًا في هذه الحالة.
## انظر أيضًا

* Class [PdfSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
