---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words لـ .NET
description: FixedPageSaveOptions OptimizeOutput ملكية. تشير العلامة إلى ما إذا كان مطلوبًا تحسين الإخراج. إذا تم تعيين هذه العلامة للوحات القماشية المتداخلة الزائدة وتمت إزالة اللوحات الفارغة يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق. ملاحظة قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية علىحقيقي . الافتراضي هوخطأ شنيع  في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

تشير العلامة إلى ما إذا كان مطلوبًا تحسين الإخراج. إذا تم تعيين هذه العلامة للوحات القماشية المتداخلة الزائدة وتمت إزالة اللوحات الفارغة، يتم أيضًا ربط الحروف الرسومية المجاورة بنفس التنسيق. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على`حقيقي` . الافتراضي هو`خطأ شنيع` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## أمثلة

يوضح كيفية تحسين كائنات المستند أثناء الحفظ بتنسيق XPS.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// قم بإنشاء كائن "XpsSaveOptions" لتمريره إلى طريقة "حفظ" المستند
// لتعديل كيفية تحويل هذا الأسلوب للمستند إلى .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

// اضبط خاصية "OptimizeOutput" على "true" لاتخاذ إجراءات مثل إزالة اللوحات المتداخلة أو الفارغة
// وتسلسل عمليات التشغيل المتجاورة بتنسيق مماثل لتحسين محتوى مستند الإخراج.
// قد يؤثر هذا على مظهر المستند.
// اضبط خاصية "OptimizeOutput" على "خطأ" لحفظ المستند بشكل طبيعي.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### أنظر أيضا

* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
