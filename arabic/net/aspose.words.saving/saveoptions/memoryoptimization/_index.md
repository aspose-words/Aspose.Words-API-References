---
title: SaveOptions.MemoryOptimization
linktitle: MemoryOptimization
articleTitle: MemoryOptimization
second_title: Aspose.Words لـ .NET
description: حسّن أداء المستندات باستخدام خاصية "تحسين الذاكرة" في "خيارات الحفظ". تحكّم في استخدام الذاكرة قبل الحفظ، مما يزيد من الكفاءة والسرعة.
type: docs
weight: 100
url: /ar/net/aspose.words.saving/saveoptions/memoryoptimization/
---
## SaveOptions.MemoryOptimization property

يحصل على القيمة أو يعينها لتحديد ما إذا كان يجب إجراء تحسين الذاكرة قبل حفظ المستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool MemoryOptimization { get; set; }
```

## ملاحظات

ضبط هذا الخيار على`حقيقي` يمكن أن يقلل بشكل كبير من استهلاك الذاكرة مع حفظ مستندات كبيرة على حساب توفير الوقت الأبطأ.

## أمثلة

يُظهر خيارًا لتحسين استهلاك الذاكرة عند تحويل المستندات الكبيرة إلى PDF.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// قم بإنشاء كائن "PdfSaveOptions" الذي يمكننا تمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .PDF.
SaveOptions saveOptions = SaveOptions.CreateSaveOptions(SaveFormat.Pdf);

// اضبط خاصية "MemoryOptimization" على "true" لتقليل حجم الذاكرة لعمليات حفظ المستندات الكبيرة
// على حساب زيادة مدة العملية.
// اضبط خاصية "MemoryOptimization" على "false" لحفظ المستند بتنسيق PDF بشكل طبيعي.
saveOptions.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "PdfSaveOptions.MemoryOptimization.pdf", saveOptions);
```

### أنظر أيضا

* class [SaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
