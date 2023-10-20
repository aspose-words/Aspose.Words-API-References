---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words لـ .NET
description: PclSaveOptions RasterizeTransformedElements ملكية. الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تنقيط العناصر المحولة المعقدة أم لا. قبل الحفظ في مستند PCL. الافتراضي هوحقيقي  في C#.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

الحصول على قيمة أو تعيينها لتحديد ما إذا كان يجب تنقيط العناصر المحولة المعقدة أم لا. قبل الحفظ في مستند PCL. الافتراضي هو`حقيقي` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## ملاحظات

لا يدعم PCL بعض أنواع التحويلات التي تستخدمها Aspose Words. على سبيل المثال، الصور المدورة والمائلة وفرش الملمس. لعرض هذه العناصر بشكل صحيح يتم استخدام عملية التنقيط، أي الحفظ في الصورة والقصاصة. يمكن أن تستغرق هذه العملية وقتًا وذاكرة إضافية. إذا تم تعيين العلامة على`خطأ شنيع` ، قد يكون بعض المحتوى في الإخراج مختلفًا مقارنة بالمستند المصدر.

## أمثلة

يوضح كيفية تنقيط العناصر المعقدة أثناء حفظ مستند في PCL.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

PclSaveOptions saveOptions = new PclSaveOptions
{
    SaveFormat = SaveFormat.Pcl,
    RasterizeTransformedElements = true
};

doc.Save(ArtifactsDir + "PclSaveOptions.RasterizeElements.pcl", saveOptions);
```

### أنظر أيضا

* class [PclSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
