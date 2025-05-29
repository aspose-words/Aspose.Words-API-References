---
title: FixedPageSaveOptions.OptimizeOutput
linktitle: OptimizeOutput
articleTitle: OptimizeOutput
second_title: Aspose.Words لـ .NET
description: حسّن إخراج مستندك باستخدام خاصية OptimizeOutput في FixedPageSaveOptions. أزل التكرارات وحسّن التنسيق لعرض أوضح.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/fixedpagesaveoptions/optimizeoutput/
---
## FixedPageSaveOptions.OptimizeOutput property

يشير العلم إلى ما إذا كان مطلوبًا لتحسين الإخراج. إذا تم تعيين هذا العلم، تتم إزالة اللوحات المتداخلة الزائدة واللوحات الفارغة، أيضًا يتم ربط الحروف المجاورة بنفس التنسيق. ملاحظة: قد تتأثر دقة عرض المحتوى إذا تم تعيين هذه الخاصية على`حقيقي` . الافتراضي هو`خطأ شنيع` .

```csharp
public virtual bool OptimizeOutput { get; set; }
```

## أمثلة

يوضح كيفية تحسين كائنات المستند أثناء الحفظ في XPS.

```csharp
Document doc = new Document(MyDir + "Unoptimized document.docx");

// قم بإنشاء كائن "XpsSaveOptions" لتمريره إلى طريقة "حفظ" الخاصة بالمستند
// لتعديل كيفية تحويل هذه الطريقة للمستند إلى .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();
// اضبط خاصية "OptimizeOutput" على "true" لاتخاذ إجراءات مثل إزالة اللوحات القماشية المتداخلة أو الفارغة
// وربط التشغيلات المتجاورة بنفس التنسيق لتحسين محتوى المستند الناتج.
//قد يؤثر هذا على مظهر المستند.
// قم بضبط خاصية "OptimizeOutput" على "false" لحفظ المستند بشكل طبيعي.
saveOptions.OptimizeOutput = optimizeOutput;

doc.Save(ArtifactsDir + "XpsSaveOptions.OptimizeOutput.xps", saveOptions);
```

### أنظر أيضا

* class [FixedPageSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
