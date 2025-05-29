---
title: PclSaveOptions.RasterizeTransformedElements
linktitle: RasterizeTransformedElements
articleTitle: RasterizeTransformedElements
second_title: Aspose.Words لـ .NET
description: تحكّم في تحويل العناصر المعقدة إلى صور نقطية في مستندات PCL باستخدام PclSaveOptions. تمكّن من إدارة جودة الصورة وحجم الملف بسهولة لتحقيق أفضل النتائج.
type: docs
weight: 30
url: /ar/net/aspose.words.saving/pclsaveoptions/rasterizetransformedelements/
---
## PclSaveOptions.RasterizeTransformedElements property

يحصل على قيمة أو يعينها لتحديد ما إذا كان يجب تحويل العناصر المعقدة المحولة إلى نقطية أم لا قبل الحفظ في مستند PCL. الافتراضي هو`حقيقي` .

```csharp
public bool RasterizeTransformedElements { get; set; }
```

## ملاحظات

لا يدعم PCL بعض أنواع التحويلات التي يستخدمها Aspose Words. مثل الصور المُدارة والمائلة وفرش الملمس. لعرض هذه العناصر بشكل صحيح، تُستخدم عملية التنقيط، أي الحفظ في صورة والقص. قد تستغرق هذه العملية وقتًا وذاكرة إضافيين. إذا تم ضبط العلامة على`خطأ شنيع` قد يكون بعض المحتوى في الإخراج مختلفًا مقارنة بالمستند المصدر.

## أمثلة

يوضح كيفية تحويل العناصر المعقدة إلى صور نقطية أثناء حفظ مستند في PCL.

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
