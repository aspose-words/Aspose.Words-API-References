---
title: PdfSaveOptions.AdditionalTextPositioning
linktitle: AdditionalTextPositioning
articleTitle: AdditionalTextPositioning
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PdfSaveOptions FurtherTextPositioning للتحكم في موضع النص في ملفات PDF. حسّن تصميم مستندك بسهولة!
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

علم يحدد ما إذا كان سيتم كتابة عوامل تحديد موضع نص إضافية أم لا.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

## ملاحظات

إذا`حقيقي` تتم كتابة عوامل إضافية لتحديد موضع النص في ملف PDF الناتج. قد يساعد هذا في التغلب على مشاكل تحديد موضع النص غير الدقيق في بعض الطابعات. الجانب السلبي هو زيادة حجم ملف PDF.

القيمة الافتراضية هي`خطأ شنيع`.

## أمثلة

إظهار كيفية كتابة عوامل تحديد موضع النص الإضافية.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // اضبط خاصية "AdditionalTextPositioning" على "true" لمحاولة إصلاح الأخطاء
    // تحديد موضع العناصر في ملف PDF الناتج، إن وجد، على حساب زيادة حجم الملف.
    // قم بضبط خاصية "AdditionalTextPositioning" على "false" لعرض المستند كالمعتاد.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
