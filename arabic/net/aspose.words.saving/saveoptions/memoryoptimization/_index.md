---
title: SaveOptions.MemoryOptimization
second_title: Aspose.Words لمراجع .NET API
description: SaveOptions ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي خاطئة .
type: docs
weight: 110
url: /ar/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي **خاطئة** .

```csharp
public bool MemoryOptimization { get; set; }
```

### ملاحظات

يمكن أن يؤدي تعيين هذا الخيار على القيمة الحقيقية إلى تقليل استهلاك الذاكرة بشكل كبير مع حفظ المستندات الكبيرة على حساب توفير الوقت البطيء .

### أمثلة

يعرض خيارًا لتحسين استهلاك الذاكرة عند تقديم مستندات كبيرة إلى PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PdfSaveOptions" يمكننا تمريره إلى طريقة "Save" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة المستند إلى PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// اضبط خاصية "MemoryOptimization" على "true" لتقليل أثر الذاكرة لعمليات حفظ المستندات الكبيرة
// بتكلفة زيادة مدة العملية.
// قم بتعيين خاصية "MemoryOptimization" على "خطأ" لحفظ المستند بتنسيق PDF بشكل طبيعي.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../saveoptions/)
* المجسم [Aspose.Words](../../../)


