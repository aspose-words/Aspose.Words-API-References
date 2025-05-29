---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Saving.PageRange لتحديد نطاقات الصفحات المتصلة بسهولة. حسّن معالجة مستنداتك بدقة وكفاءة.
type: docs
weight: 6150
url: /ar/net/aspose.words.saving/pagerange/
---
## PageRange class

يمثل نطاقًا مستمرًا من الصفحات.

لمعرفة المزيد، قم بزيارة[البرمجة باستخدام المستندات](https://docs.aspose.com/words/net/programming-with-documents/) مقالة توثيقية.

```csharp
public sealed class PageRange
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | ينشئ كائن نطاق صفحة جديد. |

## أمثلة

يوضح كيفية استخراج الصفحات استنادًا إلى نطاقات الصفحات الدقيقة.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
