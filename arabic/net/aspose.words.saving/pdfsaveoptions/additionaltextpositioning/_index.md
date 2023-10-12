---
title: PdfSaveOptions.AdditionalTextPositioning
second_title: Aspose.Words لمراجع .NET API
description: PdfSaveOptions ملكية. علامة تحدد ما إذا كان سيتم كتابة عوامل إضافية لتحديد موضع النص أم لا.
type: docs
weight: 20
url: /ar/net/aspose.words.saving/pdfsaveoptions/additionaltextpositioning/
---
## PdfSaveOptions.AdditionalTextPositioning property

علامة تحدد ما إذا كان سيتم كتابة عوامل إضافية لتحديد موضع النص أم لا.

```csharp
public bool AdditionalTextPositioning { get; set; }
```

### ملاحظات

إذا`حقيقي` ، تتم كتابة عوامل تشغيل إضافية لتحديد موضع النص في ملف PDF الناتج. قد يساعد هذا في التغلب على مشكلات تحديد موضع النص غير الدقيق في بعض الطابعات. الجانب السلبي هو زيادة حجم مستند PDF.

القيمة الافتراضية هي`خطأ شنيع`.

### أمثلة

أظهر كيفية كتابة عوامل تشغيل إضافية لتحديد موضع النص.

```csharp
Document doc = new Document(MyDir + "Text positioning operators.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
PdfSaveOptions saveOptions = new PdfSaveOptions
{
    TextCompression = PdfTextCompression.None,

    // قم بتعيين خاصية "AdditionalTextPositioning" على "صحيح" لمحاولة إصلاح الخطأ
    // تحديد موضع العناصر في ملف PDF الناتج، في حالة وجوده، على حساب زيادة حجم الملف.
    // قم بتعيين خاصية "AdditionalTextPositioning" على "خطأ" لعرض المستند كالمعتاد.
    AdditionalTextPositioning = applyAdditionalTextPositioning
};

doc.Save(ArtifactsDir + "PdfSaveOptions.AdditionalTextPositioning.pdf", saveOptions);
```

### أنظر أيضا

* class [PdfSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../pdfsaveoptions/)
* المجسم [Aspose.Words](../../../)


