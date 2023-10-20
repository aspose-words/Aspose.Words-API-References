---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words لـ .NET
description: SaveOptions MemoryOptimization ملكية. الحصول على أو تحديد القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هيخطأ شنيع  في C#.
type: docs
weight: 100
url: /ar/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

الحصول على أو تحديد القيمة التي تحدد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool MemoryOptimization { get; set; }
```

## ملاحظات

ضبط هذا الخيار على`حقيقي` يمكن أن يقلل بشكل كبير من استهلاك الذاكرة مع حفظ المستندات الكبيرة على حساب توفير الوقت بشكل أبطأ.

## أمثلة

يعرض خيارًا لتحسين استهلاك الذاكرة عند تحويل مستندات كبيرة إلى PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// اضبط خاصية "تحسين الذاكرة" على "صحيح" لتقليل مساحة الذاكرة لعمليات حفظ المستندات الكبيرة
// على حساب زيادة مدة العملية.
// اضبط خاصية "تحسين الذاكرة" على "خطأ" لحفظ المستند كملف PDF بشكل طبيعي.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
