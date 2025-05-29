---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words لـ .NET
description: تحكم بجودة صورك النقطية المُصدّرة باستخدام خيار SvgSaveOptions MaxImageResolution. اضبط كثافة البكسل للحصول على أفضل النتائج. القيمة الافتراضية هي 0.
type: docs
weight: 50
url: /ar/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

يحصل على قيمة بالبكسل لكل بوصة، أو يضبطها، لتحديد دقة الصور النقطية المُصدَّرة. القيمة الافتراضية هي صفر.

```csharp
public int MaxImageResolution { get; set; }
```

## ملاحظات

إذا كانت قيمة هذه الخاصية غير صفرية، فإنها تحد من دقة الصور النقطية المصدرة. وهذا يعني أن الصور ذات الدقة الأعلى تتم إعادة أخذ العينات منها إلى الحد الأقصى ويتم تصدير الصور ذات الدقة الأقل كما هي.

إذا كانت قيمة هذه الخاصية صفرًا، فسيتم تصدير جميع صور الراستر دون إعادة أخذ العينات.

## أمثلة

يوضح كيفية تعيين حد لدقة الصورة.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### أنظر أيضا

* class [SvgSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
